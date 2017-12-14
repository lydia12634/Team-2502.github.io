---
layout: post
title: Building and Deploying Code
categories: deploy
---
# Building Code

"Building and deploying" is the process where we programmers download code to the robot from our computers. Typically, "*building*" code implies that you are compiling it __making sure there are no syntactical errors__, while "*deploying*" code implies that you are downloading it to a robot.

### There are 2 ways to build and deploy code to the robot (both of which will also try to *deploy*):

1. Standard Ant Build
2. Gradle Build

If you are *just building* your code to see if it compiles, run

`./gradlew build`

in the Terminal while inside the directory of the robot code for Gradle build, or select the "compile" target for the standard Ant build

# Deploying Code

To deploy (download) code to a robot:

0. (Gradle Only): Run `./gradlew resolveNativeDeps`. This will ensure that you have all the libraries prepared for deploying with Gradle. This will download updated versions of the libraries, so make sure that you're connected to the internet.

1. Turn on the robot. You will have to wait a while for electronics to start up.

2. Connect to the router. Each robot is equipped with a wireless network router that you can connect to via Wi-Fi, unless you are at competition, in which case an wired connection is required.

3a. To deploy with ant, select the 'deploy' target.

3b. To deploy with gradle, open the Terminal, use `cd` to get to the directory that your software is locally stored, then run `./gradlew build deploy --offline`

## Help! It gave me an error about something with "auth" inside it!

See [this article](https://github.com/Team-2502/TeamWiki/wiki/Deploying-to-a-roboRIO-with-a-password) for a fix

## Help! It broke the pipe!

Try again

## Help! I tried 3 times and I can't deploy

If it gives you errors pointing to files that are definitely ours, then there is a bug in our code.

If it doesn't try

* Powercycling the robot

* Connecting via a different way

## Help! I can't SFTP PUT

If you are using Gradle and it says something like `Failed SFTP PUT: %PATH_TO_PROJECT%/build/libs/%JAR_NAME%.jar -> Remote3:/home/lvuser`, then check [this](https://github.com/Open-RIO/GradleRIO/issues/36).

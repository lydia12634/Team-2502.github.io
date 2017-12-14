---
layout: post
title: Gradle
categories: deploy
---# Gradle
[Gradle](http://gradle.org/) is a build assistant which has the ability to streamline the build process by running multiple tasks on build (e.g. Compiling the Code, Creating JavaDoc, Pushing Jars to Download Page. All in one command) as well as interfacing with maven to easily download dependencies.

We use a custom version of gradle called GradleRIO, it can be acquired [here](https://github.com/Open-RIO/GradleRIO/releases).

## Gradle info
If you have not [Setup Java](https://github.com/Team-2502/RobotCode2017/wiki/Java) do that now.  
Whenever you see `gradlew` it is a reference to a different command, the definitions are as follows:
* Windows:
  * `gradlew`
* OSX & Linux:
  * `./gradlew`
  * `bash gradlew`

Use the appropiate choice when executing these commands.  

Run `gradlew tasks` for information on the possible tasks to run with gradle.  

### Opening command line on windows

To access a directory through the command line on Windows open directory in explorer and `Shift + Right-Click` and select `Open command window here.

### Opening command line on Mac

Run `/Applications/Utilities/Terminal.app` and `cd` into the directory. 

### Opening command line on Linux

If you have linux, you should know how to do this for your particular distro.

## Setup

### Setup setup
Clone this project using either the `git` command line tool or [Github Desktop](https://desktop.github.com/).  

Open the directory of the robot code from the command line and run `gradlew eclipse` to prepare the project for the Eclipse environment or `gradlew idea` to prepare for the Intellij Idea environment.

### Importing into Eclipse
Open eclipse and import the project.

### Importing into IntelliJ Idea
Open the file called '<RepositoryName>.ipr'.

## Downloading natives
Connect to the internet then open the directory from the command line and run `gradlew resolveNativeDeps`

## Build
Open the directory from the command line and run `gradlew build`

## Deploy
Open the directory from the command line and run `gradlew deploy`

## Build & Deploy
Open the directory from the command line and run `gradlew build deploy`
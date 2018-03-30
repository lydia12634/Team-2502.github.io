---
layout: post
title: How to use the Pure Pursuit Point Planner
category: Pure Pursuit
---

Pure pursuit is a powerful tool to quickly get the robot to where you want it to be in autonomous. However, it is a non-trivial task to ensure that your waypoints are in the correct position for your robot to go to the right spot. To help with this, a JavaFX visualizer has been made to plot pure pursuit waypoints over an image of the field.

1. Navigate to `com.team2502.purepursuitvisualizer.Controller`

1. Change the field `Controller#path` to be the path you want to display

1. Run `com.team2502.purepursuitvisualizer.Main`

1. In the drop down at the bottom, select the starting position that your path is meant to be run from

1. The green line represents the waypoints. The orange line at the end of the green line indicates the expected trajectory of the robot when coasting.


`

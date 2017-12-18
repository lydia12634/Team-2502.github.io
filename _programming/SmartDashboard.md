---
layout: post
title: SmartDashboard
category: WPILib
---
# SmartDashboard

SmartDashboard shows us variables in our code. To put something onto SmartDashboard, add

`SmartDashboard.putNumber("What you want your number to be", aNumber)`

in `DashboardData.update()`

`aNumber` is usually a value returned by a method. For example, our line for displaying encoder values is\

`SmartDashboard.putNumber("What you want your number to be", ROBOT.DRIVE_TRAIN.getEncLeftPosition())`

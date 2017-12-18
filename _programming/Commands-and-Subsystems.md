---
layout: post
title: Commands and Subsystems
category: WPILib
---
# Commands
[`Commands`](http://first.wpi.edu/FRC/roborio/release/docs/java/) are used to control the robot. They activate [`Subsystems`](#Subsystems) when they get the proper input. The [`requires`](http://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/command/Command.html#requires-edu.wpi.first.wpilibj.command.Subsystem-) method makes sure that a subsystem is only accessed by 1 command at a time.

> [This class] is at the very core of the entire command framework. Every command can be started with a call to `start()`. Once a command is started it will call `initialize()`, and then will repeatedly call `execute()` until the `isFinished()` returns true. Once it does, `end()` will be called.

## Command Types

There are 4 types of commands: `InstantCommand`, `CommandGroup`, `TimedCommand`, and `Command`.
### InstantCommand

In an `InstantCommand`, the method `isFinished()` returns `true` by default so `execute()` will only run once. Since the `initialize` method _always_ runs once, the executeable code can be put there too.

#### Uses
 This command is useful for setting pneumatic, running motors for `Button.whileHeld`.

### TimedCommand

[`TimedCommand`](http://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/command/TimedCommand.html) runs a command for a specified time. The constructor for this class takes in the runtime in seconds of the command.

### CommandGroup

Simply put, a [`Command Group`](http://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/command/CommandGroup.html) is used to run multiple commands easily. This class allows to run commands one after another (sequentially) or simultaneously (in parallel). This class does not have any abstract methods but has the `addSequential()` and `addParallel()` methods. [Consult ScreenSteps for more info.](https://wpilib.screenstepslive.com/s/3120/m/7952/l/80210-creating-groups-of-commands)

These are very helpful for autonomous, where you can break all the subroutines into different commands that can be used in multiple autonomous command groups.

### Command (Generic)

Generic `Commands` give the ability to have more freedom in implementation. This is the most "bare bones" command with all other command implementations extending this.  

# Subsystems
> This class defines a major component of the robot.
A good example of a subsystem is the driveline, or a claw if the robot has one.

[`Subsystems`](http://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/command/Subsystem.html) get activated by [`Commands`](Commands). If you use the `setDefaultCommand` method inside a subsystem's `initDefaultCommand` method, then that command will run if the subsystem isn't used in any other command at the time (Note: this is only if `isFinished()` returns `false`). This is useful for subsystems such as drivetrains that require variable input.

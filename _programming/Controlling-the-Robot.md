---
layout: post
title: Controlling the Robot
categories: wpilib
---# Joysticks

These are the classes where you can get the info of the joystick

Some useful methods

* getRawButton(int)

* getX

* getY

* getZ

That last one will either return the rotation of the joystick (Function joystick) or the value of the slider (drive sticks).

# Buttons

## Creating Buttons

 One type of button is a joystick button which is any button on a joystick. You create one by telling it which joystick it's on and which button   number it is.


 `Joystick stick = new Joystick(port);`


 `Button button = new JoystickButton(stick, buttonNumber);`
    
There are a few additional built in buttons you can use. Additionally, by subclassing `Button` you can create custom triggers and bind those to commands the same as any other Button.
    

### Triggering Commands with Buttons


Once you have a button, it's trivial to bind it to a button in one of three ways:
   
Start the command when the button is pressed and let it run the command until it is finished as determined by it's `isFinished` method.


`button.whenPressed(new ExampleCommand());`

    
Run the command while the button is being held down and interrupt it once the button is released.


`button.whileHeld(new ExampleCommand());` 


Start the command when the button is released  and let it run the command until it is finished as determined by it's `isFinished` method.
     

`button.whenReleased(new ExampleCommand());`
---
layout: post
title: Formatting
category:
---
# Formatting
Formatting is an important thing to do to keep all code organized. The following formatting is what will be used for this year's robot.  


## Naming Conventions
CamelCase is a term used to define how to declare variable names, the important part of it are the `c`'s, the denote whether the first character of each word should be uppercase or lowercase, also note other characters like an underscore (`_`).  
Examples:
* `CamelCase`: `HelloWorld`
* `camelCase`: `helloWorld`
* `camel_case`: `hello_world`

`public fields`, `private fields` (`member variables`), `method variables` (`method parameters`), `static variables` (class variable) and `final variables` (**not static final variables**) should use `camelCase`.  
`static final` variables should use `CAMEL_CASE`.  

Classes should use `CamelCase`.  
Command classes (classes that extend `edu.wpi.first.wpilibj.command.Command`) should have their name suffixed with `Command`, command groups (classes that extend `edu.wpi.first.wpilibj.command.CommandGroup`) should have their name suffixed with `CommandG`.  
Subsystem Classes (classes that extend `edu.wpi.first.wpilibj.command.Subsystem`) should have their name suffixed with `Subsystem`.  

## Spacing
There should not be a space between a call and the opening parentheses (e.g. `a()`, `if()`, `else if()`, `switch()`, etc).  
Tabs should be converted to 4 spaces. **Never use the Tab Character.**

## Brackets
**Brackets will be below the line.**  
```java
// OK
if(x)
{
   //code
}
// NOT OK
if(x) {
   //code
}
```

Single line statements is allowed for simple statements.  
```java
// OK
if(x) {}
if(x) { }
if(x) { return; }
new AbstractObject() {};
new AbstractObject() { };

// NOT OK
if(x) { ++y; return; }
if(x) {return;}
new AbstractObject() { void test() {} };
```

## Line folding
Line folding is optional. Generally, it is preferred to not have line folding.  
1. Things that might be folded:
  * Arrays (can have their elements in any size grouping)
  * Implements or Extends
  * Parameters
  * Strings (If you do line wrap, remember to close each line and open each line with a `"` and to use the `+` character between the lines.)

## OI
OI contains only static variables. Reference them with `com.team2502.robot20XX.OI.VARIABLE_NAME`  
For numbers of any port (Joystick, Button, Sensor, Talon, etc) use `com.team2502.robot20XX.RobotMap`.

## Imports
The import order isn't important. Let your IDE handle it when formatting.  
Avoid using `static` imports. It causes confusion when trying to read code and trying to identify a method call.

## Other
If a method overrides a super method, annotate it with `@Override`.  
In general we will use pre-increment and pre-decrement. e.g. `++i` and `--i` instead of `i--` and `i++`, there are some special cases where you want to use post-increment and post-decrement.  
Whenever possible, ensure type safety.
We use methods, not functions. Get the name right.

__This part is now Deprecated__  
Whenever you do not want a variable or method to return `null`, annotate it with ~~`@org.jetbrains.annotations.NotNull`~~ `@javax.annotation.Nonnull` from `com.google.code.findbugs:jsr305`. When a variable or method can be null, you can annotate it with ~~`@org.jetbrains.annotations.Nullable`~~ `@javax.annotation.Nullable` from `com.google.code.findbugs:jsr305`.

***
_Formatting standards are subject to change_

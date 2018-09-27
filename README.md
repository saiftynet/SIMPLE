# The SIMPLE Integrated Modular Programming Language Experiment.

This is an attempt at writing a script interpreter in another interpreted
(perl) program. Is this really necessary? I don't know, probably not. Is
it foolish? Probably. But lack of a rationale and foolishness are rarely
obstacles for the irrational or the foolish.  Hence this Experiment

Programs are generated to perform specific functions, may involve some
interaction, and these actions may be customisable.  Programming languages
allow the developer to generate such applications and allow the creation of
a diverse set of applications.  But the ability to include user programmable
scripting in these applications may actually be useful.  So the objective to 
add scripting facility to scripted Perl applications, that is user customisable.

Perl appears to make this particularly easy in the way that easily handles
document parsing and its rather flexible handling of data variables and 
subroutines through hashes. This module can be merely included in any Perl
application, and adds a programmability feature to the application.

The goals would be to have a script interpreting system that

1. Handles comments
2. Handles code blocks and program flow control
4. Allows user defined variables
5. Allows user defined subroutines
6. Extended using external modules
7. Remains customisable.

## Scenarios
The main initial goal was that of Robotic control.  The  scripting would allow
quick generation of scripts that define robotic sensor and motor
programmatically, abstracting out internal functions and interface code.  In
fact the program is based on GPIO scripting application made a few years ago
called piGears in one of a [series of projects for the Rasberry Pi](http://www.windon.themoon.co.uk).
This had allowed quick and easy scripting of the IO of the device which could
be configured in a number of different ways, depending on the project.


This is essentially a custom scripting tool for one specific device (the rPi)
and a narrow domain (the IO).  But such a tool may have a wider application
if it could be customised easily. Hence this simple, integratable, modular
programming language experiment...a module that allows end-user scripting,
adaptable to diverse roles. 

## So what's so special?
So how is this different from any other programming language?
Firstly it is an integrated into an application as an end-user facing language
rather than a development language.  Secondly it is modular and customisable
offering functions specific to the application itself.  Thirdly it isolates
and abstracts system functions rather than allowing direct access to these,
both for security, and also to reduce complexity for the end-user.

## First extension
As a skeleton of a language, there is little to demonstrate what it can do, and 
less to discover what it needs to make it useful.  For this reason, and because 
one of the main applications I hope to use it in is robotics, the first extension
will involve the archetypal virtual robot...the Turtle (AKA Logo).

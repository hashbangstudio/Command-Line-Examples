Command-Line-Examples
=====================

Example usage of the command line in Linux.

The command line can at first seem quite intimidating but once you get used to the way it works you will see it is not that scary.
It is very flexible and powerful allowing you to do all sorts of tasks very quickly.

Once you have got the hang of using the commands here you can combine them in scripts to perform more complex actions. This is known as shell scripting.

Where a key combination is given as `ctrl+c` it means to hold down the `control` key and press the `c` key

Commands to be typed and key combinations will be in `this style`

Typed commands will be shown following a prompt like so:

`$ ls`

In this case the $ symbol represents the prompt and only the `ls` should be typed.
On the Raspberry Pi the prompt will probably be in green and look like:

`pi@raspi`

These instructions assume you are using the Raspbian distribution of Linux on a Raspberry Pi

Open LXTerminal by double clicking on the Icon on the Desktop.

This opens a command line, instructions can be typed here and then executed by pressing `enter`.

To jump to the beginning of a line hit the `home` key or `ctrl+a`

To jump to the end of a line hit the `end` key or `ctrl+e`

Have fun!


The Command Line
================

The command line is just a method of sending text instructions to the computer. Other names for this are the console, terminal or shell.

To run commands on the command line you type the command you want and press enter. 

`$ program`

Commands can have options and parameters (also known as arguments). Options are usually preceded by a `-` or `--`. The double dash is usually reserved foir whole word options or options with a dash within them. For example, it is common for programs to have a help text from one of the following options:

1. `-h`
2. `-help`
3. `--help`

Example: 

`$ program -h`

A double dash option containing a dash itself might look like `--full-test`. Options can also have their own arguments following them such as:

1. `-o myOutput`
2. `-n 12`

A command with all these might look like:

`$ program -k optionArg --full-test param1 param2`


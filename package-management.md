Package Management
==================

The first thing to know when using a Raspbery Pi is how to update your distribution.

A distribution is a variant or flavour of Linux. It contains a number of pre-installed programs, applications and utilities and many other optional programs and utilities are available. These programs are all contained in packages. Packages come from repositories (servers on the internet usually).

Additional packages can be installed using a package manager. This is all done using a command `apt-get`. If you run the program with no options or arguments you will see that the usage for the program is printed.

`$ apt-get`

This help text can also be shown by using what are known as options. These are usually text preceded by a `-`, in this case `-h`

`$ apt-get -h`

This shows that `apt-get` can be run using various options and commands. Each line at the top shows a different usage of the program. In order to understand what these mean we need to know what the various symbols mean:

* `[name] `
  * Anything contained in square brackets is optional and can either be omitted or included
* `one|two|three`
  * Anything separated by a pipe character `|` is an either or set of commands or options where only a single command can be used
  * Here this means that __either__ `one` __or__ `two` __or__ `three` can be used
* `pkg1 ...`
  * The Ellipsis means that any number of simlar elements can be included here.
  * For example any number of packages in this case

Note that as `apt-get` changes the operating system and can install and remove packages, root or administrator privileges are required. On a Raspberry Pi you would just put `sudo` before the program to run it with root privileges.

`$ sudo apt-get`

1. apt-get [options] command
  * This shows that any number of options from 0 to the total number can be used
  * This is followed by a single mandatory command from the list of allowed commands given in the usage
  * Examples:
    1. `apt-get update`
      * This would perform a simulated install of sonic-pi
      * It tells you what it would do but does not do it
    2. `apt-get -s install sonic-pi`
      * Installs sonic-pi to the system 
2. apt-get [options] install|remove pkg1 [pkg2 ...]
  * This shows that any number of options from 0 to the total number can be used
  * This is followed by a single mandatory command which is either `install` or `remove`
  * This is followed by a minimum of one package name and can be followed by any number of packages
  * Examples:
    1. `apt-get -s `
The computer holds a local list of available packages in the repositories that have been set to be searched.
This list can be searched for various things but it can become updated if it is not updated regularly.

To get the latest list of available packages we run the following command:

`$ sudo apt-get update`

We want to make sure we have all the latest versions of our installed packages so we need to `upgrade` the system.

`$ sudo apt-get upgrade`

Once this has run and succeeded we have an up-to-date list of available packages and all the installed packages are up to date. We can now search the locally cached list of packages using `apt-cache` to look for packages we want to install.

For example to show any packages with the text __python-pi__ in theire name or description:

`$ apt-cache search python-pi`

If we then saw that the `python-picamera` package was available we can then see more information about the package using:

`$ apt-cache show python-picamera`

To install a package you need to run :

`$ sudo apt-get install python-picamera`

Or to remove a package:

`$ sudo apt-get remove python-picamera`

There are many other options and commands available for package management but we will leave it there.

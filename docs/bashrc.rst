.bashrc
========
The purpose of a .bashrc file is to provide a place where you can set up variables, functions and aliases, define your (PS1) prompt and define other settings.

Set environment variable
--------
Set a new variable, add a new line at the end of .bashrc and add 

:code:`export VARNAME="var_value"`

Add new value to a existing environment variable, such as **PATH**

:code:`export PATH="new_value":${PATH}`

Or define a new variable first, then use the new variable.

:code:`export VARNAME="var_value"`

:code:`export PATH=${VARNAME}:${PATH}`

Set alias
--------
alias examples

:code:`alias apt-get='sudo apt-get'`

:code:`alias ls='ls --color=auto'`

Take effect
--------
Make changes in .bashrc immediately effective.

:code:`$ source ~/.bashrc`


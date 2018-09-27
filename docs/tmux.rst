tmux
========
`tmux <https://github.com/tmux/tmux>`_ is a terminal multiplexer: it enables a number of terminals to be created, accessed, and controlled from a single screen. tmux may be detached from a screen and continue running in the background, then later reattached.

Installation
--------
:code:`$ sudo apt-get install tmux`

List available sessions
--------
:code:`$ tmux ls`

Start new session
--------
:code:`$ tmux new -s <session_name>`

Attach to session
--------
:code:`$ tmux a -t <session_name>`

Kill session
--------
:code:`$ tmux kill-session -t <session_name>`


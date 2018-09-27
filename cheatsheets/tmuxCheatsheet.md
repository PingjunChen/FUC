# tmux
[tmux](https://github.com/tmux/tmux) is a terminal multiplexer: it enables a number of terminals to be created, accessed, and controlled from a single screen. tmux may be detached from a screen and continue running in the background, then later reattached.

## Installation
```
$ sudo apt-get install tmux
```

## List available sessions
```
$ tmux ls
```

## Start new session
```
tmux new -s <session_name>
```

## Attach to sessioin
```
tmux a -t <session_name>
```

## Kill session
```
tmux kill-session  -t <session_name>
```

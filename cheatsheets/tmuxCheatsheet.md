## Install tmux
```
$ sudo apt-get install tmux
```

## List available sessions
```
$ tmux ls
```

## Start a new session
```
tmux new -s <session_name>
```

## Attach to a sessioin
```
tmux a -t <session_name>
```

## Kill a session
```
tmux kill-session  -t <session_name>
```

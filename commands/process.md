# Process
## Kill process with filtering conditions
```
ps -ef | grep <command> | awk '{print $2}' | xargs kill -9  
```

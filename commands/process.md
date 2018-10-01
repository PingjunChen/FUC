# Process

### Check process
View your system’s resource usage and see the processes that are taking up the most system resources.
```
$ top
```

Improved top
```
$ htop
```

### Kill process
By process id
```
$ kill -9 <pid>
```

By application name
```
$pkill <app>
```

By filtering conditions
```
ps -ef | grep <command> | awk '{print $<col_num>}' | xargs kill -9 
```

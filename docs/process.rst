process management
========

Check process
--------

View your system’s resource usage and see the processes that are taking up the
most system resources.

:code:`$ top`

Improved top

:code:`$ htop`


Kill process
--------
By process id

:code:`$ kill -9 <pid>`

By application name

:code:`$pkill <app>`

By filtering conditions

:code:`ps -ef | grep <command> | awk '{print $<col_num>}' | xargs kill -9`

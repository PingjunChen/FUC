ls
========

Count how many files
--------
:code:`$ ls -F |grep -v / | wc -l`

Grep user ID
--------
:code:`$ ps -o user= -p PID`

Grep current process
--------
:code:`$ ps -elf | grep python/sshfs`

Change bmp img to png ext
--------
:code:`$ for i in *.bmp; do sips -s format png -s formatOptions 70 "${i}" --out "${i%bmp}png"; done`
:code:`$ for f in *.bmp; do mv -- "$f" "${f%.bmp}.png"; done`


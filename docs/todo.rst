todo item

count how many files: ls -F |grep -v / | wc -l

find -type f '*.txt'  | wc -l

ps -o user= -p PID

ps -elf | grep python/sshfs

for i in *.bmp; do sips -s format png -s formatOptions 70 "${i}" --out "${i%bmp}png"; done   %change bmp to png
for f in *.bmp; do mv -- "$f" "${f%.bmp}.png"; done


mount ntfs disk to mac:
1. diskutil info /Volumes/YOUR_NTFS_DISK_NAME 
找到 Device Node
Device Node:              /dev/disk1s1
2. hdiutil eject /Volumes/YOUR_NTFS_DISK_NAME
"disk1" unmounted.
"disk1" ejected.
弹出你的硬盘
3. 创建一个目录，稍后将mount到这个目录 
sudo mkdir /Volumes/MYHD
4. 将NTFS硬盘 挂载 mount 到mac
sudo mount_ntfs -o rw,nobrowse /dev/disk2s2 /Volumes/MYHD/



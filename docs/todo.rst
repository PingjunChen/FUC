todo item:

count how many files: ls -F |grep -v / | wc -l

find -type f '*.txt'  | wc -l

ps -o user= -p PID

ps -elf | grep python/sshfs

for i in *.bmp; do sips -s format png -s formatOptions 70 "${i}" --out "${i%bmp}png"; done   %change bmp to png
for f in *.bmp; do mv -- "$f" "${f%.bmp}.png"; done




#!/bin/bash

mkdir output
cp main.sh output/
cd output
cat main.sh > read.txt
pwd > pwd.txt
ls > ls.txt
cp main.sh copy.txt
alias printdate="date"
printdate > date.txt
wc -w main.sh | awk '{print $1}' > textcount.txt
ps | head -n 5 > process.txt
ifconfig | head -n 5 > netstat.txt
mount | head -n 5 > mount.txt
touch permissions.txt
chmod a+rwx permissions.txt
TESTENV1="test"
grep -E '\b\w{3,}\b' main.sh > regex.txt
cd ..
git add .
git commit -m "Added output directory"
git push origin main


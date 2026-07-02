# Day 1 -- Linux Commands

## 1. Basic Navigation

``` bash
pwd
ls
ls -l
ls -la
ls -lh
cd
cd ..
cd ~
clear
```

## 2. Creating Files & Directories

``` bash
mkdir devops
mkdir -p project/src
touch file.txt
touch file1 file2 file3
```

## 3. Viewing Files

``` bash
cat file.txt
less file.txt
more file.txt
head file.txt
tail file.txt
tail -f logs.txt
```

## 4. Copy, Move & Delete

``` bash
cp file1 file2
cp -r folder1 folder2
mv old.txt new.txt
mv file folder/
rm file.txt
rm -r folder
rm -rf folder
```

## 5. Finding Files

``` bash
find . -name "*.txt"
find / -name docker
locate docker
which git
whereis git
```

## 6. File Permissions

``` bash
ls -l
chmod 777 file
chmod 755 script.sh
chmod +x script.sh
chown user file
chgrp group file
```

### Permission Values

  Permission     Value
  ------------ -------
  Read               4
  Write              2
  Execute            1

### Examples

``` bash
chmod 644 file.txt
chmod 755 app.sh
```

## 7. File Content Search

``` bash
grep hello file.txt
grep -i error logs.txt
grep -r docker .
```

## 8. Text Processing

``` bash
sort file.txt
uniq file.txt
wc file.txt
cut -d "," -f1 file.csv
```

## 9. Process Management

``` bash
ps
ps -ef
top
htop
kill PID
kill -9 PID
jobs
bg
fg
```

## 10. Disk Usage

``` bash
df -h
du -sh *
free -h
```

## 11. Networking

``` bash
ip addr
ifconfig
ping google.com
curl https://google.com
wget https://example.com/file.zip
netstat -tulpn
ss -tulpn
```

## 12. Package Management (Ubuntu)

``` bash
sudo apt update
sudo apt upgrade
sudo apt install git
sudo apt remove git
```

## 13. User Management

``` bash
whoami
id
passwd
sudo su
adduser user1
userdel user1
groups
```

## 14. Environment Variables

``` bash
env
printenv
echo $PATH
export NAME=Krishna
echo $NAME
```

## 15. Archives

``` bash
tar -cvf backup.tar folder
tar -xvf backup.tar
tar -czvf backup.tar.gz folder
unzip file.zip
zip archive.zip file.txt
```

## 16. Redirection

``` bash
echo Hello > file.txt
echo World >> file.txt
cat file.txt
cat file1 file2 > all.txt
```

## 17. Pipes

``` bash
cat file.txt | grep hello
ps -ef | grep java
history | grep git
```

## 18. History

``` bash
history
!!
!25
```

## 19. System Information

``` bash
hostname
hostnamectl
uptime
date
cal
uname
uname -a
```

## 20. Help Commands

``` bash
man ls
ls --help
info ls
```

------------------------------------------------------------------------

# Hands-on Exercise

Complete the following tasks:

``` bash
mkdir DevOps
cd DevOps

mkdir Linux Git Docker Kubernetes Terraform

touch notes.txt

echo "Welcome to DevOps" > notes.txt

cat notes.txt

cp notes.txt backup.txt

mv backup.txt backup_notes.txt

chmod 755 notes.txt

ls -la

find . -name "*.txt"

grep DevOps notes.txt

tar -czvf devops.tar.gz .

history
```

------------------------------------------------------------------------

## Summary

These commands cover approximately **90% of the Linux commands** that
DevOps engineers use regularly and provide a solid foundation before
introducing Git and GitHub.

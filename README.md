# Linux_Commands



<img src="https://github.com/tahirguluzade/Linux_Commands/blob/master/linux-logo-design-template-b04c5960543f942cbd64c81280a5a941_screen.jpg" width=25% height=25%>


- [x] `nslookup` ----> is a useful command for getting information from the DNS server
```
`nslookup <ipaddress/servername>`
```
- [x] If `nslookup` ---> command does't exist in your system (check by typing `which nslookup` then try to install it
```
yum whatprovides nslookup
yum install <result of first command>
```
- [x] `df` ----> command helps us to determine general information about disks (size, used/avail spaces, partitions)
`df -h`----> shows in human readable format

- [x]  `du`----> command gives size of the directories/ files in current directory or in specified directory

     `du -sh  <file/folderpath>` ---> gives size of specified file/folder

     <img src="https://github.com/tahirguluzade/Linux_Commands/blob/master/images/Screenshot%202023-01-30%20015645.png" width=50% height=50%>


- [x] `uname`----> which gives kernel name
    ```
        options:
            -a ----> shows all information
            -r ----> shows kernel version
    ```
- [x]  `find` ----> command helps to find specific file/folder 

     #EX: `find /etc/ | grep sshd_config` shows in which directory of etc `sshd_config` is located. 
    
    <img src="https://github.com/tahirguluzade/Linux_Commands/blob/master/images/Screenshot%202023-01-30%20014510.png" width=50% height=50%>

- [x]  `netstat -tulpn | grep LIST` ----> shows listening ports in Linux.


- [x]  to find specific line in file with the combination of tail and head command

    `head -n17 /etc/sshd_config | tail -n1`

- [x] `tar -cvf <new name of tar file> <name of file which you want to archive>` ---> archives files

    `tar -cvf /root/folder.tar  /root/folder`
 
- [x] `grep -nr <string> <file/folder path>` ----> to find specific strings under any diretory/file

    _incase sensitive_:

    EX: `grep -nr password /etc/ssh`

    _case sensitive_:

    EX: `grep -inr password /etc/ssh` -- will not care about uppercase/lowercase

- [x] **What is inode in Linux?**

    inode is a data structure in Linux which stores infromations about files.
    Inode does not cotain file name., it is caring about metadata (permissions, uid, gid, file zie, owner of file) of files. when we create a file, inode number and file name are gonna attach it.

    You can check inode number by typing `ll -i` command

- [x] `dd if=/dev/zero of=file name bs=size in Mb count=number` ----> To reate new empty file with specific size 

    EX: `dd if=/dev/zero of=apple bs=100M count=1` --> will create file apple with size of 100M
    
     or `dd if=/dev/zero of=apple bs=1M count=100`      
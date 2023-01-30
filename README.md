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



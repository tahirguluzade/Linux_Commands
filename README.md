# Linux_Commands
- [ ] <kbd>**nslookup**</kbd> ---- is a useful command for getting information from the DNS server
        <kbd>**nslookup**</kbd> _ipaddress/servername_

- [ ] If <kbd>**nslookup**</kbd> --- command does't exist in your system (check by typing "<kbd>**which nslookup**</kbd>") then try to install it
    1. yum whatprovides nslookup 
    2. yum install _"result of first command"_

- [ ] <kbd>**df**</kbd>----> command helps us to determine general information about disks (size, used/avail spaces, partitions)
        <kbd>**df -h**</kbd> shows in human readable format

- [ ] <kbd>**du**</kbd>----> command gives size of the directories/ files in current directory or in specified directory
         <kbd>**du -h**<file/folderpath></kbd> ---> gives size of specified file/folder

- [ ] <kbd>**uname**</kbd>----> which gives kernel name
        options:
            <kbd>**-a**</kbd> ----> shows all information
            <kbd>**-r**</kbd> ----> shows kernel version

- [ ]  <kbd>**find**</kbd> ----> command helps to find specific file/folder 
         <kbd>**find _folder name where to look for file/folder_ | grep _file/folder name_**</kbd>
            # EX: <kbd>**find /etc/ | grep sshd_config**</kbd>

- 

 
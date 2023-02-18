## What is repository in Linux?
A Linux Repository is basically a database of application installation packages and upgrade packages available for your choice of Linux distro. Think of it like an app store. You can search among hundreds, even thousands, of applications, and install them in minutes.

- [x]  **To access all files on your CD/DVD ROM**
- create new directory under /mnt or directly mount into it

```
mkdir /mnt/cdrom
mount /dev/sr0 /mnt
```
- when you mount your CD ROM , you will get following warning which is totally fine.

    <img src="images/Screenshot 2023-02-18 154239.png" width=50% height=50%>

- now after mounting CD/DVD ROM, you can see all files under /mnt/cdrom

    <img src="images/Screenshot 2023-02-18 153859.png" width=50% height=50%>
 
## How to create repository?

- [x] Go to /etc/yum.repos.d and create new file with name.repo and write followings in it.


    ```
    [label] label of repository like id of it , you can put anything.
    name= <name of repository>
    mirrorlist= <mirrorlist is there to increase availability in case the base can't be reached>
    baseurl= <url of repository>
    enabled=<if you set this value to 0 then it ignore this repo while you install software, else it doesn't (default =1)
    gpgcheck=<GNU privacy guard>
    gpgkey=<key url>

    ```
+
        gpgcheck stands for signature verification from its central database. 
        If signature verification is successful then you sure about the security. 
        If you set the value of gpgcheck is 1 then you need to put key as well and 
        it asks for signature varification else it doesn’t.

- [x] Example: repository for installing docker

        ```
		   [docker-ce-stable]
			name=Docker CE Stable - $basearch
			baseurl=https://download.docker.com/linux/centos/$releasever/$basearch/stable
			enabled=1
			gpgcheck=1
			gpgkey=https://download.docker.com/linux/centos/gpg

        ```
- [x] `yum install <package name>` <---> install the packages
- [x] `yum remove <package name>` <----> remove the packages
- [x] `yum search <package name>` <----> search for exact name of package
- [x] `yum whatprovides <package name>` <----> deep search, looks for specific files inside package
- [x] `yum update <package name>` <----> updating the packages
- [x] `yum clean all` <---->  clear all metadata
- [x] `yum info <package name>` <---->  getting information about packages

    ```
    yum info telnet
    ```

    <img src="images/Screenshot 2023-02-18 160501.png" width=50% height=50%>

- [x] `yum install --disablerepo=* --enablerepo=<repo name>` only activate specified repo and looks for it.
- [x] `yum group list hidden` <---> shows all avaliable group repos
- [x] `yum group info "group name` <---> shows all avaliable packages under specified group

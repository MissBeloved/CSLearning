**Linux**
Linux is heavily command-line based.
Cybersecurity professionals use Linux because:
- powerful
- customizable
- used on servers
- used in cloud systems
- security tools run well on Linux

**Why Linux?**
Almost every technology like security tools, web servers, cloud pentesting environment,..etc runs on linux

**What is an operating system**
Operating system acts as an interface between the software and the hardware components.
It sits between and manage the memory, cpu, files,..etc

**What is Linux Kernal**
Many Beginners think that linux is an operating system, but it is actually a kernal.
Since linux is free and open source, many linux distributions were developed from linux kernal like ubuntu, debian, fedora, arch.
- Linux distribution vs kernal
		Linux distribution were developed from linux kernal which is an open source. some of the linux distributions are ubuntu, debian, fedora, arch.
		kernal is the heart of the operating system that communicates directly with the hardware resources. without kernal ram, cpu, keyboard,..etc were not work.
- Ubuntu, debian, feroda, arch (high-level difference)
	- ubuntu - user friendly and high community
	- debian - stable and reliable
	- feroda - new technologies and mostly used by developers
	- arch - minimal, high customization and used by advanced users

**CLU vs GUI**
- CLU is command line interface that works on commands, faster and uses less memory
- GUI is graphical user interface that works on graphical elements like icons, menus,..etc, uses ram and cpu and require maintenance

**Why servers rarely have GUI's**
Servers don't need fancy graphics since GUI uses cpu and ram, it increases the attack surface and need more maintenance
- Why Linux is preferred in cloud environments
		The technologies in cloud mostly runs on linux. since linux is used in every technology of cloud environment linux is preferred around the world

**Absolute and relative path**
Absolute path: the path starts form root directory. it always points to the same place
- example: /home/missbeloved/CSjourney/linux/day1.txt  [this absolute path always points to the day1.txt]
Relative path: the path starts from current place. 
- example: if we are currnetly in linux then ../notex/ is the relative path to go to notes folder

**Principle of Least Privilege**
- Give users and applications only the permissions they need.
- This principle appears everywhere:
Linux
AWS IAM
Kubernetes RBAC
Databases
CI/CD pipelines

***Users and Groups***
**Why do Users Exist?**
- One username and one password for the entire company doesn't provide security
- It raises the problems like No accountability, anyone can delete files, No way to know who made changes, security would be impossible.
- Linux solves this by giving every process and every person an identity.

**What is a user?**
- A user is an identity recognized by linux
- users can:
		- Own files, Run programs, Log in, Have specific permissions
- Examples:
		- root - Superuser (administrator).
		- Your own account.
		- www-data - Runs web servers.
		- mysql - Runs database services.
Expert Insight: Many services create service accounts that are not meant for humans to log in. This limits what those services can access if they're compromised.

**What is a group?**
- A group is a collection of users who share permissions
- Instead granting permissions to each single user individually, you can grant them to the group
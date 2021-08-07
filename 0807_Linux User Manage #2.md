# Linux User Mangement #2

**The following  commands are equivalent to modify in those four files directly. **



### Add User

```shell
useradd [option] username

# Options:
# -u	set UID
# -d	set home directory
# -c	write a note for user
# ...	

# The default settings are at:
/etc/default/useradd
/etc/login.defs

# The "useradd" command does four things:
#1	write information in 	/etc/passwd
#2	write password in	 	/etc/shadow
#3	write information in 	/etc/group
#4 	write group password in /etc/gshadow 
#5	create home directory and mail
#6	copy configuration files in /etc/skel to home directory 
```



### Password 

```shell
passwd [option] username

# Options:
# -S	inquire the state of user's password (root only)
# -l	lock the user (root only)
# -u	unlock the user (root only)
# ...

# After seting a password, the newuser are finally created
```



### Change User's Information

```shell
usermod [option] username

# Options:
# -c 	change notes
# -d	change home directory
# -l	change username
# ...

```



### Change Passwd's State

```
chage [option] username
```



### Delete User 

```shell
userdel -r username	# root only

# -r means also delete home directory with user account

# User data are including:
#1	basic info, in 			/etc/passwd
#2	password info, in 		/etc/shadow
#3	group info, in 			/etc/group
#4	group password info, in /etc/password
#5	user's personal files,include:
#	home directory in 		/home/username/
#	mail directory in 		/var/spool/mail/username/
```




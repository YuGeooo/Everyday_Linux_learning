# Linux User Management #3 (Final)



### Swich User

```shell
su [option] username

# options:
# -l 	swich enviorment while swiching user
# -p	contrarily, do not swich enviorment 
# -c	swich with runing a command, then swich back
```



### Group Management

```shell
groupadd [option] groupname
# options:
# -g	set GID
# -r	create system group

groupmod [option] groupname
# options:
# -g	change GID
# -n	change groupname

groupdel [option] groupname
# can not delete user's default group

gpasswd [option] groupname
# group management
# options:
#			set group password (root only)
# -A user1	set user1 as group manager (root only)
# -r 		remove group's password (root only)
# -a user2	join user2 in group
# -d user2	remove user2 out of group
```



### Change User's Default Group

```shell
# For example:
groupadd group1
groupadd group2
groupadd group3

useradd -g group1 -G group2,group3 user1
# set group1 as default group of user1,
# group2, group3 as addtional group
```


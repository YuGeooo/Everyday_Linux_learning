# Linux User Management



### Concept: User / User group



### User

Linux know：Username × 	User ID √

Also，Groupname ×	Group ID √



### "*passwd*" file

```shell
/etc/passwd #path
```

***Passwd* file inculds user's basic information**, every user can read the file.

For example, in *passwd* file:

|   geyq   |    x     | 1000 | 1000 |  , , ,   |    /home/geyq    |   /bin/bash   |
| :------: | :------: | :--: | :--: | :------: | :--------------: | :-----------: |
| Username | Password | UID  | GID  | Describe | Home dictiontary | Default shell |

"*x*" only show that user has password. The turely password is in *shadow* file. 



### "*shadow*" file

```shell
/etc/shadow #path
```

***Shadow* file inculds user's password**, only root user can read the file.

For example, in shadow file:

|   geyq   |    $6$ly...BDO    |      18802       |          0          |    99999    |          7          |                      |              |                 |
| :------: | :---------------: | :--------------: | :-----------------: | :---------: | :-----------------: | :------------------: | :----------: | :-------------: |
| Username | Encryption passwd | Last change date | Min change interval | Useful life | Alert befor overdue | Extend after overdue | Invalid time | Ramain(useless) |

What does the last change date "*18802*" mean ? 

--- The date between 1970.1.1

```shell
date -d "1970 -01 -01 18802 days"
# Thu Jun 24 00:00:00 CST 2021
```


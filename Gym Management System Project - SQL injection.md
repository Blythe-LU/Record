## Gym Management System Project Login page has SQL injection

[College Attendance System (CAS)](https://www.sourcecodester.com/visual-basic-net/15538/college-attendance-system-cas.html) Released by SourceCodester Has SQL Injection

There is a SQL injection vulnerability in mygym/login.php. An attacker can obtain database information and modify the database content through this vulnerability, which is extremely harmful.

### There is a path for SQL injection

```
/mygym/login.php
```

### The login page is as follows

![image-20220808160137805](Gym%20Management%20System%20Project%20-%20SQL%20injection.assets/image-20220808160137805.png)

**Capture packets**

![image-20220808160315151](Gym%20Management%20System%20Project%20-%20SQL%20injection.assets/image-20220808160315151.png)





![image-20220808155830024](Gym%20Management%20System%20Project%20-%20SQL%20injection.assets/image-20220808155830024.png)



### There are 2 fields with injection points

```
user_email
user_pass
```



**Post injection via sqlmap**

injection point：user_email

![image-20220808154609073](Gym%20Management%20System%20Project%20-%20SQL%20injection.assets/image-20220808154609073.png)

injection point：user_pass

![image-20220808161031620](Gym%20Management%20System%20Project%20-%20SQL%20injection.assets/image-20220808161031620.png)



**The database name was successfully obtained**

![image-20220808154124749](Gym%20Management%20System%20Project%20-%20SQL%20injection.assets/image-20220808154124749.png)



## LINK

https://www.sourcecodester.com/php/15515/gym-management-system-project-php.html
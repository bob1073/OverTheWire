# Level 6 -> Level 7

Another finding task. This time the file is somewhere in the server and:
 - Is owned by user bandit7 (**-user**)
 - Is owned by group bandit6 (**-group**)
 - Has 33 bytes in size
 
 Now we must find in root directory / and specify all the options above. If we do, we'll get a lot of errors since some directories are owned by root user
 and we dont have permission. To avoid that error output, we can use **2>/dev/null** which means redirect error output to */dev/null*.[^note]
 
 ```console
 bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
```

In the file found is the password
```console
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

[^note]: */dev/null* is a virtual device in linux system which can be used to discard anything written to it.

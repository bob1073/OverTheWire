# Level 1 -> Level 2
If we do an **ls** the file called - is in the directory.

```console
bandit1@bandit:~$ ls
-
```

However, this time **cat -** is not going to work, because '-' in linux is used for Standard Input/ Standard Output (STDIN/ STDOUT). The solution is simple:

```console
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

Adding './' before '-' specifies the absolute path, where '.' means current directory. Is a way to scape the '-' character.

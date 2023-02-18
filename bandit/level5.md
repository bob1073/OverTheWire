# Level 5

Again, there is a *inhere* directory, but this is time is filled with several files.

```console
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
```

The goal here is to identify the human readable file. This can be done in several ways, but **file** command is handy enough. We could do **file ./-file00**,
**file ./-file01** and so one, that would tell us what type of file is each of them. But here is a smarter way:

```console
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```
As we can see, using '\*' list all the file types, as this applies the command file to each of them. The file named *-file07* is ASCII text so is the only one readable.
The other ones are binary data.

```console
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

Maybe the purpose of level is to use the **find** command, but don't worry, we'll use it in the next levels!

# Level 5 -> Level 6

OTW is asking for a very specific file, which has the following attributes:

 - human readable
 - 1033 bytes in size
 - not executable

If we take a look into *inhere* directory is not so easy to find files by hand, as there a lot of directories inside.

```console
bandit5@bandit:~$ ls inhere
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
```

Time to use our friend **find**!. Some options we are going to need:
 - **-type**: Especifies object type, **f** for file and **d** for directory.
 - **-readable**: Search just readable files
 - **-size**: Especifies file size, read **man file** for more info. 
 - **! -executable**: Search not executable files.

So the right command is:
```console
bandit5@bandit:~/inhere$ find . -type f -readable -size 1033c ! -executable
./maybehere07/.file2
```
And we found the password, note how the whitespaces are used to reach 1033 bytes.
```console
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU








                                              bandit5@bandit:~/inhere$
```

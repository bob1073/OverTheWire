# Level 8 -> Level 9

This one is a little tricky. The content of *data.txt* is a lot of random strings. There is only one line which occurs one. To find that line, the **uniq**
command may result useful. Let's try to use it! **-u** option is used to print only uniq lines, so that should do the job right?

```console
bandit8@bandit:~$ uniq -u data.txt
puP3nfQp5FCMNyLsdWASZ472scVSrUDJ
desthMrvBwFuSWkom7FP8ASJayNlfoRd
7XS0q7U1mnlcxKF8TqKmV0MTz3Nk2JLR
7Yw8BBU0dsNPIPGaqTrzCD1ui5ZUPC3W
bpGBMUddF6EGDkaXM8uguzsgQ9hVMX5x
WMPIYAeOF4iIKjo4ZC9ux57X5Tzukk5W
9g8tRRuUhXrOYgdQohBAvxas7CB939F4
i1F09GVEcOpA740WJJc1DELRUhfGCHl9
nzs4ijk2uOZItbx4Le3Zyugvp68xXkpp
p1dzDa5gJ8tpkgPW5hPHDRENabkbbYFV
HOqQ9Z3JVL1A05MoavjtZzng1CkauWGg
qwMRqzTYYCX2ztxsXTdlfdSBBlmMAmoK
. . .
```

Hum, maybe is not working. The problem is that **uniq** expects the lines to be orderer alphabetically in order to work and get unique lines. With **sort** we can order
the result first and the pipe into **uniq -u**:

```console
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

And there we go! Here is the password.

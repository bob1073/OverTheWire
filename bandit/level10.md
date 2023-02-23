# Level 9 -> Level 10

The *data.txt* file contains some garbage characters. We want to filter by humand readable strings and then find the password.

To do that, first lets introduce the **strings** command. It gives the humand readable strings of a file:

```console
bandit9@bandit:~$ strings data.txt
q99B
C:I5H
IkC_
r2Fx
#6j2
pjCkC
--\'
yjD<'`#
. . .
```

As we know the string is preceded by some '=' characters, let's filter with **grep**!

```console
bandit9@bandit:~$ strings data.txt | grep =======
f========== theM
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
Now we can proceed to the next level.

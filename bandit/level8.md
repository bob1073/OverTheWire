# Level 8 -> Level 9

If we **cat data.txt**, it contains a lot of lines. We need to find the line which contains the word *millionth*. The **grep** command will do for us.
The syntax is simple, we first specify the keyword and then the file.

```console
bandit7@bandit:~$ ls
data.txt
```

```console
bandit7@bandit:~$ grep millionth data.txt
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

Another approach to solve the level is using grep with a pipe |. This way we first output the whole content of *data.txt* and then filter by word *millionth*, as |
applies **grep** to output on the left side.

```console
bandit7@bandit:~$ cat data.txt | grep millionth
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

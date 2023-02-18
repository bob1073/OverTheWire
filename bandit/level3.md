# Level 3
Listing the directory content shows a file with spaces in the filename:

```console
bandit2@bandit:~$ ls
spaces in this filename
```

Trying **cat spaces in this filename** is not working, as linux thinks we are trying to read a file 4 different files, due to space caracter: 

```console
bandit2@bandit:~$ cat space in this filename
cat: space: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
```

A quick way to solve this is autocompletion. Starting by 'cat sp' and the pessing TAB key will autocomplete de filename, scaping space caracter with '\ ':

```console
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

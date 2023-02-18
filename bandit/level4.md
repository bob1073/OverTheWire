# Level 4

This time, we have a directory called *inhere*. To move there, just type **cd inhere**:

```console
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$
```

As we can see, in our linux shell now the route is '\~/inhere' instead of '~' which refers to the *home* directory of user *bandit3*. Doing an **ls** won't show
anything, cause the file is hidden. To show hidden files in linux option **-a** must be specified.

```console
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
```

Note that also '.' and '..' directories are shown. As we said in Level 2, '.' refers to current directory. The '..' guy refers to the parent directory.

Now is easy to read the content, as we know the filename:

```console
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```

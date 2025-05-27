# Übung 2

```
vboxuser@Vass:~$ cd docs
vboxuser@Vass:~/docs$ ls
file2  file3  file4  file5  file6  file7  file8  file9
vboxuser@Vass:~/docs$
```

```
vboxuser@Vass:~/docs$ rm file2 file4 file7
vboxuser@Vass:~/docs$ ls
file3  file5  file6  file8  file9
```
```
vboxuser@Vass:~/docs$ rm -r *
vboxuser@Vass:~/docs$ ls
```
```
vboxuser@Vass:~/docs$ cd ..
vboxuser@Vass:~$ mkdir Ordner
vboxuser@Vass:~$ cd Ordner
vboxuser@Vass:~/Ordner$ touch file1
vboxuser@Vass:~/Ordner$ touch file2
vboxuser@Vass:~/Ordner$ touch file3
vboxuser@Vass:~/Ordner$ touch file4
vboxuser@Vass:~/Ordner$ touch file5
vboxuser@Vass:~/Ordner$ touch file6
vboxuser@Vass:~/Ordner$ touch file7
vboxuser@Vass:~/Ordner$ touch file8
vboxuser@Vass:~/Ordner$ touch file9
vboxuser@Vass:~/Ordner$ touch file10
vboxuser@Vass:~/Ordner$ ls
file1  file10  file2  file3  file4  file5  file6  file7  file8  file9

```
```
vboxuser@Vass:~$ cp -r Ordner Ordner2
vboxuser@Vass:~$ cd Ordner2
vboxuser@Vass:~/Ordner2$ ls
file1  file10  file2  file3  file4  file5  file6  file7  file8  file9
```
```
vboxuser@Vass:~$ cp -r Ordner Ordner2/Ordner3
vboxuser@Vass:~$ mv Ordner Ordner1
vboxuser@Vass:~$ ls
Ordner1  Ordner2  docs
```
```
vboxuser@Vass:~$ rm -r Ordner1 Ordner2
vboxuser@Vass:~$ ls
docs
```

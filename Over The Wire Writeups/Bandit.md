# Bandit Writeup
#### [Link](http://overthewire.org/wargames/bandit/)

## Level 0
We need to login with ssh with uersname bandit0 and poasword bandit0
`ssh bandit0@bandit.labs.overthewire.org`
It asks for the password which is: `bandit0`.
And we're in!


### Level 0 → 1
Always start by looking at all that is in the directory with `ll`
```shell
drwxr-xr-x   2 root    root    4096 Nov 14  2014 ./
drwxr-xr-x 172 root    root    4096 Jul 10 14:12 ../
-rw-r--r--   1 root    root     220 Apr  9  2014 .bash_logout
-rw-r--r--   1 root    root    3637 Apr  9  2014 .bashrc
-rw-r--r--   1 root    root     675 Apr  9  2014 .profile
-rw-r-----   1 bandit1 bandit0   33 Nov 14  2014 readme
```
Looks like we need to take a look at readme file. To look at the contents we just enter
'cat readme'
**Password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1**


### Level 1 → 2
To enter this level we type
`ssh bandit1@localhost`
Password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Always start by looking at all that is in the directory with `ll`
```shell
-rw-r-----   1 bandit2 bandit1   33 Nov 14  2014 -
drwxr-xr-x   2 root    root    4096 Nov 14  2014 ./
drwxr-xr-x 172 root    root    4096 Jul 10 14:12 ../
-rw-r--r--   1 root    root     220 Apr  9  2014 .bash_logout
-rw-r--r--   1 root    root    3637 Apr  9  2014 .bashrc
-rw-r--r--   1 root    root     675 Apr  9  2014 .profile
```
We need some way of getting into the '-' file. Using `cat -` would put us into a input mode. We need to use a filename relative to our location.
`cat ./-`
**Password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9**


### Level 2 → 3
To enter this level we type
`ssh bandit1@localhost`
Password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Always start by looking at all that is in the directory with `ll`
```shell
drwxr-xr-x   2 root    root    4096 Nov 14  2014 ./
drwxr-xr-x 172 root    root    4096 Jul 10 14:12 ../
-rw-r--r--   1 root    root     220 Apr  9  2014 .bash_logout
-rw-r--r--   1 root    root    3637 Apr  9  2014 .bashrc
-rw-r--r--   1 root    root     675 Apr  9  2014 .profile
-rw-r-----   1 bandit3 bandit2   33 Nov 14  2014 spaces in this filename
```

Looks like we just need to get into the file with spaces.. If you just type 'cat s' and then press tab terminal will autocomplete the query with the correct format (using \). Double quotes ("") may also be used.

'cat spaces\ in\ this\ filename'
OR
'cat "spaces in this filename"'
**Password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK**

### Level 3 → 4
To enter this level we type
`ssh bandit3@localhost`
Password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Always start by looking at all that is in the directory with `ll`
```shell
drwxr-xr-x   3 root root 4096 Nov 14  2014 ./
drwxr-xr-x 172 root root 4096 Jul 10 14:12 ../
-rw-r--r--   1 root root  220 Apr  9  2014 .bash_logout
-rw-r--r--   1 root root 3637 Apr  9  2014 .bashrc
-rw-r--r--   1 root root  675 Apr  9  2014 .profile
drwxr-xr-x   2 root root 4096 Nov 14  2014 inhere/
```

inhere is a directory, you can tell in three ways, the *d* in drwxr-xr-x (its permission tag) or the / at the end of the name. If we try 'cat inhere/' the terminal responds: 'cat: inhere/: Is a directory'. To get into the directory we use the 'cd' command.
'cd inhere'
We list the files inside. `ll`
```shell
drwxr-xr-x 2 root    root    4096 Nov 14  2014 ./
drwxr-xr-x 3 root    root    4096 Nov 14  2014 ../
-rw-r----- 1 bandit4 bandit3   33 Nov 14  2014 .hidden
```

'cat .hidden'
**Password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB**


UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

### Level 8 → 9
cvX2JJa4CFALtqS87jk27qwqGhBM9plV

I need to find the line with a string that occurs only once.
cat data.txt | sort | uniq -u   


### Level 9 → 10
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR


# Bandit Writeup
#### [Link](http://overthewire.org/wargames/bandit/)

### Level 0
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

### Level 0 → 1
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

### Level 1 → 2
### Level 2 → 3
### Level 3 → 4
### Level 4 → 5
### Level 5 → 6
### Level 6 → 7
### Level 7 → 8
### Level 8 → 9
### Level 9 → 10

UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
cvX2JJa4CFALtqS87jk27qwqGhBM9plV

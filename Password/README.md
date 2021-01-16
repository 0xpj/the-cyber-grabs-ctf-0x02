# Password

## Description

```Description
We have suspected Mr.Wolf and for investigation purposes we have created a backup of his data. 
The task for you is to find the password of Mr.Wolf PC.

Format: cybergrabs{password}

Link: https://mega.nz/file/Lo90hAKK#saeLUPbgZPC5GIzMbjCWWVVeEBSi15t1f76h-WbbSeQ
```

## Solution

For this challenge we have to find Wolf-PC password if you notice there's some note saying `I dumped some process but i forgot it`

so `Mr.Wolf` dumped `lsass` process and whenever you dump a process it goes in `users/wolf-pc/Appdata/local/temp` visit that directory and you will find `lsass.dmp`.

Just export `lsass.DMP` and install `mimikatz` i suggest trying this on your virtual box.

After setting up `mimikatz` just use the below commands. 

```mimkatz
privilege::debug
sekurlsa::minidump lsass.DMP
sekurlsa::logonpasswords
```

now you we will get a hash just use [crackstation](https://crackstation.net/) or any other hash cracking tool of your choice.

## Flag

`cybergrabs{4hacking}`
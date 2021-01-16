# Secret

## Description

```Description
After further investigation we have found out that Mr.Wolf is hiding something on the internet can you find it?

Note: Use the Same file shared in First Challenge(Password) .
Format : Flag in flag format.
```

## Solution

According to description he's hiding something on the internet so time to checkout web history.

`C:\Users\wolf-pc\AppData\Roaming\Mozilla\Firefox\Profiles\<profile folder>`

we can find it in the above path.

export `places.sqlite`

open it using `sqlite` 

now just read the history and we can find there's a 
`cryptobin.co`  link
`https://cryptobin.co/a1o8e8f7`
and if you analyzed the text files he mentioned that he uses the same password everywhere so let's use `4hacking` (which we cracked in first challenge) and we will get base64 let's convert it into a file we will get `gif` just use `exiftool` and we will get the flag.

## Flag

`cybergrabs{dammm_y0u_f0und_p3p3_h3cker}`
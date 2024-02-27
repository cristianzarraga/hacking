## Objetivo

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso
- Puerto: 2220
- Host: bandit.labs.overthewire.org
- Contraseña: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
- Usuario: **bandit15

## Solución

```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
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
MIIDCzCCAfOgAwIBAgIEIivS1jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC4
XC9dgne8ha9I/vXn4uTtObLhI/PPyLyl4jyDQPp61VtsEMcOb95KhXxdtQiDtzSD
3KXQVFLaPlVGKDWSR9nV+GoazSNPmNLH/IMVrUYxXjYikPxo1jjYKyuqfjV5bNm3
Hz6z4eDl7wNbPRaPAMPo0WU23m9M04bKQHLINfN7Abz3a+7ChLeICrWXiXp9mWfj
PY8cK7Vayz0eHU4Lg64q4jUaXQqZ/ta1RqZEwv7ZuTKctcazpK/u2+h4zvQCPyLh
uDjUXZTLlIuhfjyKUJLQsmYHAQprV6sY3ybFN32dW6MSE0/ApT6Th0LzKeaYxk5b
3NIeaYyPeKsjqFSwy+2zAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBQ
RXG1k+cB357X43fsiyaCQQh4RbWHOcg1jBes5eiC/H8MyC3ec1znXvOUfqJcWNQJ
9UJDMwbkpo+IcwJiOe9n/D3Zeypv1g+ta8KKLsQ+zcbp5RdltKy7GuO/s5WjVofE
/IHz/5g+IMoqqYLlquQ539CZykPMC9TB9uWfJj/i8faCox4gjtkSCri+27tUZuHi
eYR3zxY1ptsJti/pMaItC6Oc2/pSlotQ4fXdciLZYGXqlmSFBt8Y8/v1YkhME5gN
3HmBV/Zg1SghA57zYsbf3npvQwudr04f2iF493pe0VRN6DfiXTxWkJe1VKuyGHEr
Q4L4OdVlgMSeyYyKgFc7
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
    Session-ID: D360D37D45A99C6C0637D8C8A6C103024B7F53C0A9B400DF5EEEA34BDD948855
    Session-ID-ctx:
    Resumption PSK: DD1CDA1201A906E43EBB23CA8A3FB6F9AF254AED36E2195B7318023102FF0A9A2168ADB7A80EC2E71CAB4617D6F79451
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - f5 d9 be 4a 2a d3 38 40-37 2d 6c c7 8b 2a e8 51   ...J*.8@7-l..*.Q
    0020 - e7 4b 12 24 b9 f6 4e 3c-ff 27 23 70 7d 90 c1 27   .K.$..N<.'#p}..'
    0030 - eb 01 21 da de 21 04 dc-8e 84 98 95 7c 9c bd b2   ..!..!......|...
    0040 - a5 85 76 1b e4 72 60 82-7f 2e 77 ce 89 0b b5 20   ..v..r`...w....
    0050 - 2c c8 8e a4 0a 46 8f f9-5e 2b 48 1e 3a 16 86 db   ,....F..^+H.:...
    0060 - ea d8 32 b2 13 08 52 bf-c5 12 0a 17 0c 40 33 5a   ..2...R......@3Z
    0070 - 33 02 40 50 1d 68 ff f9-5d 7c 6e 8f 33 f1 32 5f   3.@P.h..]|n.3.2_
    0080 - 58 93 55 eb f2 5c 62 6e-52 89 9a f9 95 e8 b2 1f   X.U..\bnR.......
    0090 - 68 86 c7 26 f0 77 1b ee-58 43 3b b0 d8 12 84 14   h..&.w..XC;.....
    00a0 - 59 0d cb 4b 1f 06 08 d9-6c 00 c0 64 e1 88 d6 51   Y..K....l..d...Q
    00b0 - ee 9b 6e c3 95 7c db 72-fe 0a a6 0f ef c2 b3 e3   ..n..|.r........
    00c0 - 33 a6 55 2a 61 37 56 71-d4 ae 83 f6 61 58 7a 6f   3.U*a7Vq....aXzo

    Start Time: 1708484213
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
    Session-ID: C1C9A30E91A7C000721A562E2765B1677B0A3F0CAD428A52DFFE4CB20865EA5D
    Session-ID-ctx:
    Resumption PSK: FA8EC104FA176F10AB93940FFEA66BE6A2A337E985649E3258EAFF356BB2C55D6A9C604941627BE88E524CCBBD4F73EB
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - a4 06 27 97 b4 03 ef a2-eb 9a c6 6d ce 8f c8 9b   ..'........m....
    0020 - 7d e8 c5 c1 82 9f 29 13-a9 88 0e 80 f5 54 da 13   }.....)......T..
    0030 - f5 65 bf b9 0a aa 2b 62-22 88 fd ae 85 d3 fe e6   .e....+b".......
    0040 - 56 0b 78 df ef 83 56 da-a1 95 7e 95 2f c2 fc cc   V.x...V...~./...
    0050 - 27 fe f4 95 a3 ce aa 3e-81 9b cc 4c 92 08 e1 a2   '......>...L....
    0060 - 2c 31 75 06 c8 33 2c db-69 96 af 24 fc a5 29 7f   ,1u..3,.i..$..).
    0070 - b4 fb 1d 19 bd f8 15 54-34 40 f1 28 45 cf e6 ca   .......T4@.(E...
    0080 - a0 cb bb 5e a7 86 63 d5-c6 df 26 76 2b 09 35 08   ...^..c...&v+.5.
    0090 - f9 ea 67 d7 0c 46 8a c5-9f 10 8e 20 33 ed b5 11   ..g..F..... 3...
    00a0 - 9c e1 58 5d 71 57 0e 86-53 bd 51 68 5c 93 ea bc   ..X]qW..S.Qh\...
    00b0 - c8 89 df c7 1a 37 dd d2-1f 31 44 4e f4 67 ce fa   .....7...1DN.g..
    00c0 - 6d 1a 09 0c 71 18 c8 60-aa b0 30 fd 04 55 e2 99   m...q..`..0..U..

    Start Time: 1708484213
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```

## Notas adicionales


With public key authentication, the authenticating entity has a public key and a private key. Each key is a large number with special mathematical properties. The private key is kept on the computer you log in from, while the public key is stored on the **.ssh/authorized_keys** file on all the computers you want to log in to. When you log in to a computer, the SSH server uses the public key to "lock" messages in a way that can only be "unlocked" by your private key - this means that even the most resourceful attacker can't snoop on, or interfere with, your session. As an extra security measure, most SSH programs store the private key in a passphrase-protected format, so that if your computer is stolen or broken in to, you should have enough time to disable your old public key before they break the passphrase and start using your key. Wikipedia has a [more detailed explanation](http://en.wikipedia.org/wiki/Public-key_cryptography "WikiPedia") of how keys work.

```bash
<ssh-rsa or ssh-dss> <really long string of nonsense> <username>@<host>
```

## Referencias

[ls(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/ls.1.html)
[cat(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/cat.1.html)
[file(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/file.1.html)
[find(1) - Linux manual page (man7.org)](https://man7.org/linux/man-pages/man1/find.1.html)

[SSH/OpenSSH/Keys - Community Help Wiki (ubuntu.com)](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
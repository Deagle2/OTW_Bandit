Soln

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.
Commands you may need to solve this level

ssh, telnet, nc, ncat, socat, openssl, s_client, nmap, netstat, ss


ssh bandit15@bandit.labs.overthewire.org -p 2220

openssl s_client -connect localhost:30001

    openssl: For implementing SSL/TLS protocols.
    s_client: This sub-command establishes a connection to a secure server.
    -connect localhost:30001: This specifies the server address (localhost) and the port number (30001) to connect to.


Output 
```

CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
---
Certificate chain
 0 s:CN = SnakeOil
   i:CN = SnakeOil
   a:PKEY: rsaEncryption, 4096 (bit); sigalg: RSA-SHA256
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN = SnakeOil
issuer=CN = SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 2103 bytes and written 373 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 4096 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: B51F03014647DBA47DEF959692C6668CFB45C98B19D3275DF04CC19C66839771
    Session-ID-ctx: 
    Resumption PSK: 829C4C4AE098EE8CD7803B6B4D99964DCDFBF29F5C28EAF0A882806454A469AA4AB5B73CE3CBACE6D17BD17961CFE166
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - b9 0b d1 26 a0 8d 77 53-99 46 b3 da 57 31 b1 33   ...&..wS.F..W1.3
    0010 - 98 00 c9 ef 6a d7 7b 2d-06 fc 38 d6 69 6b a0 e5   ....j.{-..8.ik..
    0020 - dd 85 32 2c cc 3f 75 d7-8c f5 60 e2 13 39 f4 ca   ..2,.?u...`..9..
    0030 - 05 95 d5 c0 cf a8 14 7d-d4 99 ae bd 39 6a cc db   .......}....9j..
    0040 - 2c 2d 6f 27 54 e8 d2 c1-48 0d ac 8b d8 8d b2 51   ,-o'T...H......Q
    0050 - 43 f6 8f 0a da 4d 0b b5-52 45 d4 23 11 56 3e 59   C....M..RE.#.V>Y
    0060 - 41 85 26 cb ad ec eb 7d-f6 ee ce 75 be ba 49 24   A.&....}...u..I$
    0070 - 2d d5 e4 84 b2 9f 45 92-17 67 e8 14 4b 27 d7 7f   -.....E..g..K'..
    0080 - 40 68 88 e6 3a c7 21 b1-c6 cd 08 3b 04 d8 d5 9a   @h..:.!....;....
    0090 - c7 a7 e6 d4 3c f9 12 aa-9b f8 d2 c2 04 7a 73 99   ....<........zs.
    00a0 - 8f f8 81 13 32 cb 87 d9-30 0c 34 bd a4 78 f7 c1   ....2...0.4..x..
    00b0 - 46 05 7d 72 0d 11 8c 64-49 c7 63 81 18 30 7a 00   F.}r...dI.c..0z.
    00c0 - 2f 43 f7 86 02 a7 40 b1-cb 4c 58 a2 e3 ad a0 00   /C....@..LX.....
    00d0 - ab 6f 2b 9d 7e 55 92 88-e5 09 8d 51 3a 6a 8c 47   .o+.~U.....Q:j.G

    Start Time: 1730036844
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E0F7C6223F38DFAE4145AB729DE6355F089CD0C4A81C4EA72EA09CD1F5AAC56D
    Session-ID-ctx: 
    Resumption PSK: 2388F3A4361294EF1A4B6A507337B9D8B9D2A5F5B0DF6EA17339B6A973D0EAD8330ABE6BAAB8104F464E4940850A584D
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - b9 0b d1 26 a0 8d 77 53-99 46 b3 da 57 31 b1 33   ...&..wS.F..W1.3
    0010 - 16 de 0d 8c 89 34 36 da-df 68 21 1d fb c9 c9 0f   .....46..h!.....
    0020 - a9 18 1b ff a9 0f de 75-b3 c6 23 39 9c 77 9f 95   .......u..#9.w..
    0030 - 9b a9 16 10 c1 d8 2a d4-41 be b0 c5 95 ca c8 4c   ......*.A......L
    0040 - f5 a0 3c 20 09 ea 1c d2-b1 2b 77 0d f7 51 36 64   ..< .....+w..Q6d
    0050 - 56 07 93 d1 84 98 5f 1e-db 60 5f ee 41 61 2e 65   V....._..`_.Aa.e
    0060 - f6 d2 72 88 e6 b0 25 b0-df ee 06 4f 7f 75 c5 fe   ..r...%....O.u..
    0070 - bd df 76 99 3f df 0c 28-0d 28 b6 2d 73 36 5d c7   ..v.?..(.(.-s6].
    0080 - 4d 7d 3b 91 d9 30 7a 7f-ea 33 52 24 a4 65 fa 59   M};..0z..3R$.e.Y
    0090 - df bb d5 53 83 4d a3 d9-ef 3b dd c7 12 99 33 76   ...S.M...;....3v
    00a0 - 9b 32 6e 5a f9 ac 97 84-c3 9f e4 0c aa 53 7b 20   .2nZ.........S{ 
    00b0 - 99 d9 99 07 f3 e7 25 18-ee c6 44 b9 cb f5 c9 0f   ......%...D.....
    00c0 - c9 15 65 ad d5 8b ee 1e-67 3f 1b e6 a4 89 5d 22   ..e.....g?....]"
    00d0 - 20 35 31 2b e1 64 25 59-1e ba dc 16 c1 61 a7 6f    51+.d%Y.....a.o

    Start Time: 1730036844
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0

read R BLOCK

Here enter the same pwd we used to log into the bandit15

Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

closed

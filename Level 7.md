# Soln
Conditions - 

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

 ssh bandit6@bandit.labs.overthewire.org -p 2220

find / -type f -user bandit7 -group bandit6 -size 33c
gives an output that includes /var/lib/dpkg/info/bandit7.password


cat var/lib/dpkg/info/bandit7.password

 

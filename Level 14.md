# Soln 

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on
Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

#

`ssh bandit13@bandit.labs.overthewire.org -p 2220`

`ls` gives sshkey.private

`ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`

ssh : initiate an SSH session

-i sshkey.private: The -i option specifies the private key to use for authentication. In this case, sshkey.private is the private key to access the bandit14 account.


`cat /etc/bandit_pass/bandit14` as mentioned above

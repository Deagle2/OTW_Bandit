# Soln

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

cat data.txt | grep ======= didnt work

Human readable strings has a specific cmd in Linux `strings` 

strings data.txt | | grep =====
}========== the
3JprD========== passwordi
~fDV3========== is
D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
bandit9@bandit:~$ 

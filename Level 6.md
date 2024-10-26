# Description
Conditions-

    human-readable
    1033 bytes in size
    not executable

ssh bandit5@bandit.labs.overthewire.org -p 2220

ls

cd /inhere

find . -type f -size 1033c ! -executable
gives the output ./maybehere07/.file2

cat ./maybehere07/.file2

```
find : find cmd

. : current directory.

-type f: for type file only, excluding directories etc

-size 1033c: size of 1033
-c : bytes


! : not executable





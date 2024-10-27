# Soln

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

To retrieve the password from data.txt  where all lowercase and uppercase letters have been rotated by 13 positions (a ROT13 cipher) I used `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'`

tr is a Unix/Linux command used to translate or replace characters in text. It stands for "translate."

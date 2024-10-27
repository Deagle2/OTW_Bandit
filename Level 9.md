# Soln

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

cat data.txt gives a lot of random text, sort data.txt sorts but it is very hard to find the unique line of text


sort data.txt | uniq -u

Use sort data.txt | uniq -u when you want to find globally unique lines (lines that appear exactly once in the entire file).

Use cat data.txt | uniq -u if you only care about consecutively non-repeated lines (ignoring non-consecutive duplicates).

# Soln 

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc localhost 30000        
 
Correct!

8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

(`MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS` is the previous flag)


`nc localhost 30000` uses netcat (nc) to connect to port 30000 on your local machine (localhost).
 nc command, also known as Netcat, is a versatile command-line utility for reading and writing data across network connections using the TCP or UDP protocols
 TCP & UDP are both transport layer protocols within the Internet Protocol Suite,

# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Developed by: Rougith D
Register No: 212225220087
##Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())


```
##Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUPUT
<img width="1730" height="295" alt="{119F9FCF-2DD7-4C6B-8835-74BDE7D156B0}" src="https://github.com/user-attachments/assets/655204ad-6585-4d8d-b500-df810c6c3895" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

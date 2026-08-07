# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name: Monika V
## Ref No: 212225100028
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
client:
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
```
server:
import socket
s=socket.socket() 
s.connect(('localhost',8000)) 
while True:
     msg=input("Client > ") 
     s.send(msg.encode()) 
     print("Server > ",s.recv(1024).decode()) 



```
## OUTPUT
<img width="1638" height="899" alt="image" src="https://github.com/user-attachments/assets/52cf8b41-ab02-4945-a0fd-da4aadb6fa53" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

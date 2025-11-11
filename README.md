# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

```
Developed by:G.Mithik jain
Reg no:212224240087
```
## PROGRAM
## Client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

```

## Server:
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
## OUTPUT

## Client:
<img width="847" height="248" alt="image" src="https://github.com/user-attachments/assets/c2697786-f355-4c39-beba-6441b5d6e907" />

## Server:
<img width="848" height="359" alt="image" src="https://github.com/user-attachments/assets/92910cab-caa8-41d5-b3d6-2e2ad62c81d5" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM

client:

import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

msg=input("Client > ")

s.send(msg.encode())

print("Server > ",s.recv(1024).decode())

server:

import socket

s=socket.socket()

s.bind(('localhost',8000))

s.listen(5)

c,addr=s.accept()

while True:

ClientMessage=c.recv(1024).decode()

c.send(ClientMessage.encode())


## OUPUT

CLIENT:

![image](https://github.com/user-attachments/assets/1a13f9cb-132c-4e18-a109-36cddce70fb3)

SERVER:

![image](https://github.com/user-attachments/assets/73a1d009-3876-45f4-b125-80c88f8440b8)



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

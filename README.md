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
 c.send(ClientMessage.encode())
```

## OUPUT
## Client:
![image](https://github.com/vthaanesh22/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139373686/34c75e32-a486-4eb9-b505-8ff65eaa9300)
## Server:
![Screenshot 2024-04-27 170429](https://github.com/vthaanesh22/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139373686/058cce02-4a99-4ca2-8a54-7298e3038846)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.

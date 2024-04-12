## name: S.VENGADA KRISHNAN

## reg. no: 212223110061
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

## server:
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## client:
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
## OUPUT
# server:
![EXP3BCLIENT](https://github.com/SVENGADAKRISHNAN/3b_CHAT_USING_TCP_SOCKETS/assets/147473084/3247286f-243e-4f2e-a9e0-ecfc9c1a24a0)

# client:

![EXP3BSERVER](https://github.com/SVENGADAKRISHNAN/3b_CHAT_USING_TCP_SOCKETS/assets/147473084/b972e254-7e28-4d38-8b0b-51ac5d00ae04)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.




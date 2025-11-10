# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
CLIENT: 
import socket                                                              
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
i=input("Enter a data: ") 
c.send(i.encode()) 
ack=c.recv(1024).decode() 
if ack: 
print(ack) 
continue 
else: 
c.close() 
break
SERVER: 
 
import socket                                                              
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
print(s.recv(1024).decode()) 
s.send("Acknowledgement Recived".encode())
```
## OUTPUT
## Client
<img width="861" height="223" alt="324228529-23a81fd4-fcf6-487b-87d5-191a2935043e" src="https://github.com/user-attachments/assets/c8869b1a-e7b4-425c-a264-04dd48b478df" />

## Server
<img width="860" height="182" alt="324228562-7bd712e4-7bde-4364-bef7-94e4d830f697" src="https://github.com/user-attachments/assets/22e42ae8-6fe1-4be2-9462-0dab97e66a5b" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

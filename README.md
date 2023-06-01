# APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

# EXP : 9

# DATE : 03-05-2023

# AIM :
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM :
# Client :
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server
4. Send and receive the message using the send function in socket.
# PROGRAM :
# CLIENT :
```python3
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
  ```
# SERVER :
```python3
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
   
# CLIENT OUTPUT :
![client](https://github.com/Skanthasishanth/EX-9/assets/118298456/f633cc25-f004-47f6-8664-9501fa09bcde)




# SERVER OUTPUT :



![server](https://github.com/Skanthasishanth/EX-9/assets/118298456/476148d9-be4a-40f7-8bcb-d4280f1f98ea)

# RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.

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
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data:")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
```
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT

<img width="1920" height="829" alt="433029280-a1684d85-cdcf-4096-bf36-95e30647f456" src="https://github.com/user-attachments/assets/b62834fc-f81a-4524-bb66-9f5a975f5ae7" />
<img width="1920" height="707" alt="433029313-54c4bdea-6211-43b7-9274-ec3b1db9dfea" src="https://github.com/user-attachments/assets/f553cc8c-9497-4704-ab47-d7009162b135" />


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

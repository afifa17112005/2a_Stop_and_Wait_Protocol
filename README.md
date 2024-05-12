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
Name:A.Afifa Reg.no:212223040008
## client:
``` import socket
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
```
## server :
```import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```

## OUTPUT:
## client:
![311126652-c442b81a-fa59-474c-a5ef-952b9b2a7017](https://github.com/afifa17112005/2a_Stop_and_Wait_Protocol/assets/147080931/893c42a9-0e4b-49fe-aab3-2d9acb7b1469)
## server :
![311126730-bd434e24-c491-4dda-aaa5-2cd6b4812004](https://github.com/afifa17112005/2a_Stop_and_Wait_Protocol/assets/147080931/4b5f4f56-f06b-489f-ae70-fccbaa2e5932)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

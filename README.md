### README.md

### IMPLEMENTATION OF SLIDING WINDOW PROTOCOL EXP: 3 DATE:22-03-2023 AIM : To write a python program to perform sliding window protocol ALGORITHM :

## 1.Start the program.

## 2.Get the frame size from the user

## 3.To create the frame based on the user request.

## 4.To send frames to server from the client side.

## 5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.

## 6.Stop the program CLIENT PROGRAM : import socket s=socket.socket() s.bind(('localhost',8000)) s.listen(5) c,addr=s.accept() size=int(input("Enter number of frames to send:")) l=list(range(size)) s=int(input("Enter Window Size:")) st=0 i=0 while

True:

while(i<len(l)):
```
 st+=s
 c.send(str(l[i:st]).encode())
 ack=c.recv(1024).decode()
 if ack:
 	print(ack)
 	i+=s
  ```
  
###  SERVER PROGRAM : import socket s=socket.socket() s.connect(('localhost',8000)) while True: print(s.recv(1024).decode()) s.send("acknowledgement recieved from the server".encode())

### SERVER OUTPUT :
![image](https://github.com/tsanjaithirumal/EX-3/assets/119393916/ce586974-985b-4541-a575-22aa352b48fd)
### CLIENT OUTPUT :
![image](https://github.com/tsanjaithirumal/EX-3/assets/119393916/6a932d1f-1fec-41e9-a5a9-2939dead31e1)
### RESULT : Thus, python program to perform stop and wait protocol was successfully executed.

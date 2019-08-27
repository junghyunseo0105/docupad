---
title: "파이썬(Server) 자바(Client) tcp 통신"
layout: single
categories:
  - python
toc: true
toc_label: "목차"
toc_icon: "cog"
---

## 파이썬 서버
```python
import socket

soc = socket.socket()
host = "192.168.0.5"
port = 2005
soc.bind((host, port))
soc.listen(5)

conn, addr = soc.accept()
print("Got connection from",addr)

while True:
    
    length_of_message = int.from_bytes(conn.recv(2), byteorder='big')
    msg = conn.recv(length_of_message).decode("UTF-8")
    print(msg)
    print(length_of_message) #메세지의 길이 보내기

    # Note the corrected indentation below
    if "client writeUTF"in msg:  #만약 msg가 "client writeUTF" 일시
        message_to_send = "bye".encode("UTF-8")  #"bye" 라는 메세지 보내기
        conn.send(len(message_to_send).to_bytes(2, byteorder='big'))
        conn.send(message_to_send)
    else:
        print("no message")
        
        while True:
            pass
```

## 자바 클라이언트
```java
import java.io.*;  
import java.net.*; 

public class Main {
	
	Main() {
		try {
			Socket socket=new Socket("192.168.0.5",2005);  

	        DataOutputStream dout=new DataOutputStream(socket.getOutputStream());  
	        DataInputStream din=new DataInputStream(socket.getInputStream());


	        dout.writeUTF("client writeUTF");
	        dout.flush();

	        System.out.println("send first mess");
	        String str = din.readUTF();    //in.readLine();

	        System.out.println("client readUTF "+str);


	        dout.close();  
	        din.close();
	        socket.close();
		} catch (IOException e) {
			e.printStackTrace();
		}  

	}
	
    public static void main(String[] args) {  
    	new Main();
    }
}
```

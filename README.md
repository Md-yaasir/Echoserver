# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

/*
Developed by: Y. MOHAMMED YAASIR 
RegisterNumber: 212224040196  
*/

### Client :
```python
# echo-client.py

import socket
HOST = "127.0.0.1"
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)
print(f"Received {data!r}")
```

### Server:
```python
# echo-server.py
import socket
HOST = "127.0.0.1"
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
## OUTPUT:
![WhatsApp Image 2025-03-07 at 10 39 43_2d6f0303](https://github.com/user-attachments/assets/72c9c9ce-0c9b-4b2e-afca-401af90ebf53)

## RESULT:
The program i
s executed successfully

# Echoserver
Echo server and client using python socket
# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
import socket
HOST , PORT = '127.0.0.1',65432
with socket.create_server((HOST,PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
```
import socket
HOST, PORT = '127.0.0.1',65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'vijay ,212223040236')
    print(f'Received: {s.recv(1024)!r}')
```
##  Architecture Diagram

```bash
+--------------------------+
|  User's Web Browser      |
|  (Client: Chrome/Firefox)|
+-----------+--------------+
            |
            |  HTTP Request (GET /)
            v
+-----------+--------------+
|   Python Web Server      |
| (http.server + Handler)  |
| - Listens on Port 8000   |
| - Handles GET Requests   |
| - Sends HTML Response    |
+-----------+--------------+
            |
            |  HTML Response
            v
+--------------------------+
|  User Sees Rendered Page |
|  <h1>Hello Web Server</h1>|
+--------------------------+
```


## OUTPUT:
<img width="1866" height="984" alt="image" src="https://github.com/user-attachments/assets/9386c952-84c7-4f1c-a391-503e211c7759" />



## RESULT:
The program is executed succesfully

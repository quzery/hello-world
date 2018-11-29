# hello-world
#just a test 

import socket

s = socket.socket()

host = socket.gethostname()
port = 8000
s.bind((host,port))

s.listen(5)
while True:
    c, addr = s.accept()
    print("got connection from",addr)
    data = 'Thank you for connecting'
    c.send(data.encode())
    c.close()



import socket

s = socket.socket()

host = socket.gethostname()
port = 8000

s.connect((host, port))
print(s.recv(1024).decode())

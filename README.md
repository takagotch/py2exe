### py2exe
---
https://github.com/albertosottile/py2exe

http://www.py2exe.org/

```py
// tests/functional/ssl_test/ssl_test.py

packat = b"GET / HTTP/1.1\r\nHost: www.google.com\r\n\r\n"
HOST, PORT = 'www.google.com', 443

sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
sock.settimeout(10)

wrappedSocket = ssl.wrap_socket(sock=sock)

wrappedSocket.connect((HOST, PORT))
wrappedSocket.send(packet)
rec = wrappedSocket.recv(15)

wrapedSocket.close()

out = rec.decode('utf-8')
print("SSL test output: {}".format(out))
assert out == 'HTTP/1.1 200 OK'
```

```
```

```
```


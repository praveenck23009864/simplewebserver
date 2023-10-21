# EX01 Developing a Simple Webserver
## Date: 21/09/2023

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<!DOCTYPE html>
<html>
<head>
<title>Praveen (23009864) </title>
</head>
<body>
<h1><u>Revenue generating companies</u><h1>

<ul>
<li>Amazon</li>
<li>Apple</li>
<li>Microsoft</li>
<li>Google</li>
</ul>

Done by Praveen (23009864)

</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:
![Screenshot 2023-10-21 084059](https://github.com/praveenck23009864/simplewebserver/assets/141472050/ca5868ef-d311-46c1-82ad-e5826a8e8040)

## RESULT:
The program for implementing simple webserver is executed successfully.

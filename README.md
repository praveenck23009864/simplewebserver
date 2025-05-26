# EX01 Developing a Simple Webserver
## Date:23-05-2025

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
Nmae:Punniyakotti.M
Regno:212224240122
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<head>
    <title>Time Table</title>
</head>
<body>

    <h2>Weekly Timetable </h2>
    <table border="1">
        <tr>
            <th>Day</th>
            <th>Monday</th>
            <th>Tuesday</th>
            <th>Wednesday</th>
            <th>Thursday</th>
            <th>Friday</th>
        </tr>
        <tr>
            <td>8:00-10:00</td>
            <td>Web Development</td>
            <td>Data Science</td>
            <td>Artificial Intelligence</td>
            <td>Quantitative Ability</td>
            <td>Linear Algebra</td>
        </tr>
        <tr>
            <td>10:00-12:00</td>
            <td>Advance C programming</td>
            <td>Maths for AI</td>
            <td>Artificial Intelligence</td>
            <td>Reasoning Ability</td>
            <td>Linear Algebra</td>
        </tr>
        <tr>
            <td>1:00-3:00</td>
            <td>Web Development</td>
            <td>Data Science</td>
            <td>Machine Learning</td>
            <td>Probability</td>
            <td>Physics</td>
        </tr>
    </table>

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
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![exp1](https://github.com/user-attachments/assets/379ca99b-580c-43fe-bea8-131bac84d716)

![Screenshot 2025-05-16 142041](https://github.com/user-attachments/assets/350115bf-b70f-4cf1-a128-2fb1b4e65ec9)



## RESULT:
The program for implementing simple webserver is executed successfully.

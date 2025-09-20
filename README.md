# EX01 Developing a Simple Webserver

# Date:18-09-2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler
content ='''<!DOCTYPE html>
<html lang="en">
<head>from
  <meta charset="UTF-8">
  <title>TCP/IP Protocol Layers</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 40px;
    }
    table {
      width: 80%;
      border-collapse: collapse;
      margin: auto;
      text-align: center;
    }
    th, td {
      border: 1px solid #333;
      padding: 12px;
    }
    th {
      background-color: #4CAF50;
      color: white;
    }
    tr:nth-child(even) {
      background-color: #f2f2f2;
    }
    caption {
      font-size: 1.5em;
      margin-bottom: 15px;
font-weight: bold;
    }
  </style>
</head>
<body>
  <table>
    <caption>TCP/IP Protocol Layers</caption>
    <tr>
      <th>Layer</th>
      <th>Functions</th>
      <th>Examples</th>
    </tr>
    <tr>
      <td>Application Layer</td>
      <td>Provides network services to end-users, supports communication between applications</td>
      <td>HTTP, FTP, SMTP, DNS, SNMP</td>
    </tr>
    <tr>
      <td>Transport Layer</td>
      <td>Ensures reliable data transfer, error checking, and flow control</td>
      <td>TCP, UDP</td>
    </tr>
    <tr>
      <td>Internet Layer</td>
      <td>Handles logical addressing, routing, and packet forwarding</td>
      <td>IP, ICMP, ARP</td>
    </tr>
    <tr>
      <td>Network Access Layer</td>
      <td>Defines how data is physically sent over the network (hardware, cabling, signaling)</td>
      <td>Ethernet, Wi-Fi, PPP</td>
    </tr>
  </table>
</body>
</html>'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type", "text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.server_forever()
```

# OUTPUT:
![alt text](<Screenshot (16).png>)
![alt text](<Screenshot (17) - Copy.png>)


# RESULT:
The program for implementing simple webserver is executed successfully.

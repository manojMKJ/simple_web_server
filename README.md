

# Date:
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
content = """
<html>   
<title> Top Software Industries </title>
<body>
<table border="2" cellspacing="10"cellpadding="6"> 
<caption>Top 5 Revenue Generating Software Companies </caption>
<tr>    
<th>s.no</th>
<th>companies</th>
<th>revenue</th>
</tr>
<tr>  
<th>1</th>
<th>Microsoft</th>
<th>65 billion</th>
</tr>
<tr>  
<th>2</th>
<th>oracle</th>
<th>29.6 billion</th>
</tr>
<tr>
<th>3</th>
<th>IBM</th>
<th>29.1 billion</th>
</tr>
<tr>
<th>5</th>
<th>symentec</th>
<th>5.6 billion</th>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()

```
# OUTPUT:
![Screenshot (558) 1](https://github.com/user-attachments/assets/a7efae14-5ea2-4fb1-9bf8-0c1fa65eaee2)

![alt text](![FWAD image](https://github.com/user-attachments/assets/488be191-e720-4d99-967b-dbad2e7f2d5c)
)


# RESULT:
The program for implementing simple webserver is executed successfully.

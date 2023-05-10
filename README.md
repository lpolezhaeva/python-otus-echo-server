# Echo Server with Python Socket Library

This is an assignment to create an echo server using the Python socket library. The server should only use modules from the standard library. 

## Description
The server should accept requests from clients and send the following back:
- headers received in the request
- method used to make the request
- status specified by the client in the GET parameter 'status'. If the parameter is not present or invalid, return 200 OK.
- optionally, the server should continue listening for new connections after responding to the client.

Headers should be displayed on the page as text strings in the following format:
```
Request Method: GET
Request Source: ('127.0.0.1', 47296)
Response Status: 200 OK
header-name: header-value
header-name: header-value
```

## Requirements
- Python 3.x
- Only standard library modules can be used

## Usage
1. Start the server:
```
python http-server.py
```

2. Open a command line and send a request using `curl` to `http://localhost:40404/`, f.e. `curl -i localhost:40404/?status=512`. You should see the response headers displayed on the screen.

3. Optionally, you can specify the status parameter in the URL to change the response status:
```
localhost:40404/?status=404
```

4. The server will continue listening for new connections until you stop it manually.
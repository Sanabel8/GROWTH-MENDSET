Review: High-level HTTP
 The HTTP Request Lifecycle
- Step 1: Local Processing
* to understanding this request is being made by a browser.
* . An example is |http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|
* host (www.example.com)
* the browser has the intended hostname for the request, it needs to resolve an IP address1

- Step 2: Resolve an IP
* resolving an IP from a "DNS server" , the steps:
1. If the cache lookup fails (we will assume it does), your browser fires off a DNS request using UDP
*  UDP : is a lightweight protocol, but the tradeoff is that it offers no guarantees in terms of delivery, and there is no acknowledgement other than a response being sent and received.
* the request search for  target DNS server.
* when it arrives the DNS ,the DNS search for the address associated with the requested hostname , and send aresponce .
* request is successful : the requesting client now has a target IP.

- Step 3: Establish a TCP Connection
* request is sent over TCP , so the client must open a TCP connection.
* TCP ensures delivery and ordered data transmission by as a sequence number for every byte sent.
*  TCP connections are opened using what’s known as a three-way handshake
* full duplex communication:  direction of communication (client->server, server->client), allowing for bidirectional, concurrent communication along the connection

- Step 4: Send an HTTP Request
* The request is made up of :1. "request line" 2. request header, 3. a body.
* "request line": simply a line that indicates the HTTP method, the resource being requested, and the protocol version
* The header of the request is made up of pairs in the form name:value <CR><LF>
* <CR><LF> pairs indicate the end of the header section.
* The only mandatory field in an HTTP request is HOST
* contains the domain and port (domain.com:8080)
*  common standard HTTP header fields include Origin, Accept, Accept-Encoding
* The body content of an HTTP request is completely optional, but often contains something like form data or JSON.
* An HTTP response has a similar structure to an HTTP request, containing a "status line", response header fields, and an optional body.
* The status line contains an HTTP status code indicating the success, failure, or error-state of the request

- Step 5: Tearing Down and Cleaning Up

Java HTTP Request example

1. Overview
 way of performing HTTP requests in Java 
2. HttpUrlConnection
is aclass allows us to perform basic HTTP requests without the use of any additional libraries , is part of the java.net package.
3. Creating a Request
 creates a connection object by create an HttpUrlConnection instance using the openConnection() method of the URL class
* example:
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");

4. Adding Request Parameters
we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream
5. Setting Request Headers
can be achieved by using the setRequestProperty() method
6. Configuring Timeouts
7. Handling Cookies
8. Handling Redirects
9. Reading the Response
10. Reading the Response on Failed Requests
11. Building the Full Response
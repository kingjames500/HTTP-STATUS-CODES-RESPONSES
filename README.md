## HTTP response status codes.
 - HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

We have five categories of HTTP response status codes which are summarised below;

# 1. Informational Responses 
This responses indicate that the client  should continue the request or ignore the response if the request is already finished.

### <ins> Types of informational responses.</ins>

<h2 style = "color:yellowgreen">
   100 Continue
</h2>

- means that the initial part of the request  has been recieved by the server  and the client should proceed with the request.

<h2 style = "color:yellowgreen">
   101 Switching Protocols
</h2>

- means that the server understands the upgrade header field request and indicate which protocol is switching to.

<h2 style = "color:yellowgreen">
102 Processing
</h2>

- indicates to client that a full request has been received and the server is working on it

<h2 style = "color:yellowgreen">
103 Early Hints
</h2>

- may be sent by a server while it is still preparing a response, with hints about the sites and resources that the server expects the final response will link to.

# 2. Successful responses








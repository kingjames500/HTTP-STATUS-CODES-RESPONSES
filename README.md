## HTTP RESPONSE STATUS CODES.

- HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

We have five categories of HTTP response status codes which are summarised below;

# 1. Informational Responses

This responses indicate that the client should continue the request or ignore the response if the request is already finished.

### <ins> Types of informational responses.</ins>

<h2 style = "color:yellowgreen">
   100 Continue
</h2>

- means that the initial part of the request has been recieved by the server and the client should proceed with the request.

<h2 style = "color:yellowgreen">
   101 Switching Protocols
</h2>

- means that the server understands the upgrade header field request and indicate which protocol is switching to.

<h2 style = "color:yellowgreen">
102 Processing
</h2>

- Indicates to client that a full request has been received and the server is working on it

<h2 style = "color:yellowgreen">
103 Early Hints
</h2>

- may be sent by a server while it is still preparing a response, with hints about the sites and resources that the server expects the final response will link to.

# 2. Successful responses

The Success response is the confirmation used by Distributed Search to indicate that a message has been received and processed successfully.

### <ins> Types of successful responses.</ins>

<h2 style = "color:yellowgreen">
200 OK
</h2>

- The request succeeded. The result and meaning of "success" depends on the HTTP method:

  - GET: The resource has been fetched and transmitted in the message body.

  - PUT or POST: The resource describing the result of the action is transmitted in the message body.
  - TRACE: The message body contains the request as received by the server.

<h2 style = "color:yellowgreen">
201 Created
</h2>

- Indicates that the HTTP request has led to the creation of a resource. This status code is commonly sent as the result of a POST request.

<h2 style = "color:yellowgreen">
202 Accepted
</h2>

- Indicates that a request has been accepted for processing, but processing has not been completed or may not have started. The actual processing of the request is not guaranteed; a task or action may fail or be disallowed when a server tries to process it.

<h2 style = "color:yellowgreen">
203 Non-Authoritative Information
</h2>

- Indicates that the request was successful, but a transforming proxy has modified the headers or enclosed content from the origin server's 200 (OK) response.

<h2 style = "color:yellowgreen">
204 No Content
</h2>

- Indicates that a request has succeeded, but the client doesn't need to navigate away from its current page.

- A 204 No Content in response to these request methods has the following meaning and results:

  - DELETE: The action was successful, and no further information needs to be supplied.

  - PUT: The action was successful, and the ETag value contains the entity tag for the new representation of that target resource.

<h2 style = "color:yellowgreen">
205 Reset Content
</h2>

- indicates that the request has been successfully processed and the client should reset the document view.

<h2 style = "color:yellowgreen">
206 Partial Content
</h2>

- is sent in response to a range request. The response body contains the requested ranges of data as specified in the Range header of the request.

<h2 style = "color:yellowgreen">
207 Multi-Status
</h2>

- indicates a mixture of responses. This response is used exclusively in the context of Web Distributed Authoring and Versioning

<h2 style = "color:yellowgreen">
208 Already Reported
</h2>

- Is used in a 207 Multi-Status response to save space and avoid conflicts. This response is used exclusively in the context of Web Distributed Authoring and Versioning

<h2 style = "color:yellowgreen">
226 IM Used
</h2>

- indicates that the server is returning a delta in response to a GET request. It is used in the context of HTTP delta encodings.

# 3. Redirection messages

Redirection is triggered by a server sending a special redirect response to a request. Redirect responses have status codes that start with 3 , and a Location header holding the URL to redirect to.

### <ins> Types of redirection responses.</ins>

<h2 style = "color:yellowgreen">
300 Multiple Choices
</h2>

- indicates that the request has more than one possible response. The user-agent or the user should choose one of them.

 <h2 style = "color:yellowgreen">
301 Moved Permanently
</h2>

- indicates that the requested resource has been permanently moved to the URL in the Location header.

<h2 style = "color:yellowgreen">
302 Found
</h2>

- indicates that the requested resource has been temporarily moved to the URL in the Location header.

<h2 style = "color:yellowgreen">
303 See Other
</h2>

- indicates that the browser should redirect to the URL in the Location header instead of rendering the requested resource.

- This response code is often sent back as a result of PUT or POST methods so the client may retrieve a confirmation, or view a representation of a real-world object

 <h2 style = "color:yellowgreen">
304 Not Modified
</h2>
 - indicates that there is no need to retransmit the requested resources.
 - o the client can continue to use the same cached version of the response.

  <h2 style = "color:yellowgreen">
305 Use Proxy Deprecated
</h2>

- Indicate that a requested response must be accessed by a proxy. It has been deprecated due to security concerns regarding in-band configuration of a proxy.

 <h2 style = "color:yellowgreen">
306 unused
</h2>

- This response code is no longer used; but is reserved. It was used in a previous version of the HTTP/1.1 specification.

 <h2 style = "color:yellowgreen">
307 Temporary Redirect
</h2>

- indicates that the resource requested has been temporarily moved to the URL in the Location header.

<h2 style = "color:yellowgreen">
308 Permanent Redirect
</h2>

- indicates that the requested resource has been permanently moved to the URL given by the Location header.

<br>

# 4. Client error responses

These errors are typically displayed to the user as a message or code on the website, and they can indicate that there is a problem with the user's browser or device that needs to be addressed in order to access the website or web application properly.

### <ins> Types of client error responses.</ins>

<h2 style = "color:yellowgreen">
400 Bad Request
</h2>

- indicates that the server would not process the request due to something the server considered to be a client error. The reason for a 400 response is typically due to malformed request syntax, invalid request message framing, or deceptive request routing.

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

<h2 style = "color:yellowgreen">
401 Unauthorized
</h2>

- indicates that a request was not successful because it lacks valid authentication credentials for the requested resource.

 <h2 style = "color:yellowgreen">
402 Payment Required
</h2>

- is a nonstandard response status code reserved for future use.

- This status code was created to enable digital cash or (micro) payment systems and would indicate that requested content is not available until the client makes a payment.

 <h2 style = "color:yellowgreen">
403 Forbidden
</h2>

- indicates that the server understood the request but refused to process it. This status is similar to 401, except that for 403 Forbidden responses, authenticating or re-authenticating makes no difference. The request failure is tied to application logic, such as insufficient permissions to a resource or action.

 <h2 style = "color:yellowgreen">
404 Not Found
</h2>

- indicates that the server cannot find the requested resource.

 <h2 style = "color:yellowgreen">
405 Method Not Allowed
</h2>

- ndicates that the server knows the request method, but the target resource doesn't support this method.

 <h2 style = "color:yellowgreen">
406 Not Acceptable
</h2>

- indicates that the server could not produce a response matching the list of acceptable values defined in the request's proactive content negotiation headers and that the server was unwilling to supply a default representation.

 <h2 style = "color:yellowgreen">
407 Proxy Authentication Required
</h2>

- indicates that the request did not succeed because it lacks valid authentication credentials for the proxy server that sits between the client and the server with access to the requested resource.

 <h2 style = "color:yellowgreen">
408 Request Timeout
</h2>

- indicates that the server would like to shut down this unused connection. A 408 is sent on an idle connection by some servers, even without any previous request by the client.

<h2 style = "color:yellowgreen">
409 Conflict
</h2>

- indicates a request conflict with the current state of the target resource.

<h2 style = "color:yellowgreen">
410 Gone
</h2>

- indicates that the target resource is no longer available at the origin server and that this condition is likely to be permanent. A 410 response is cacheable by default.

<h2 style = "color:yellowgreen">
411 Length Required
</h2>

- status code indicates that the server refused to accept the request without a defined Content-Length header.

<h2 style = "color:yellowgreen">
412 Precondition Failed
</h2>

- ndicates that access to the target resource was denied.

<h2 style = "color:yellowgreen">
413 Content Too Large
</h2>

- indicates that the request entity was larger than limits defined by server. The server might close the connection or return a Retry-After header field.

<h2 style = "color:yellowgreen">
  414 URI Too Long
</h2>

- indicates that a URI requested by the client was longer than the server is willing to interpret.

<h2 style = "color:yellowgreen">
415 Unsupported Media Type
</h2>

- indicates that the server refused to accept the request because the message content format is not supported.

<h2 style = "color:yellowgreen">
   416 Range Not Satisfiable
</h2>

- Indicates that a server could not serve the requested ranges. The most likely reason for this response is that the document doesn't contain such ranges, or that the Range header value, though syntactically correct, doesn't make sense.

<h2 style = "color:yellowgreen">
417 Expectation Failed
</h2>

- Indicates that the expectation given in the request's Expect header could not be met. After receiving a 417 response, a client should repeat the request without an Expect request header, including the file in the request body without waiting for a 100 response.

<h2 style = "color:yellowgreen">
418 I'm a teapot
</h2>

- indicates that the server refuses to brew coffee because it is, permanently, a teapot.

<h2 style = "color:yellowgreen">
421 Misdirected Request
</h2>

- indicates that the request was directed to a server that is not able to produce a response.

<h2 style = "color:yellowgreen">
422 Unprocessable Content 
</h2>

- indicates that the server understood the content type of the request content, and the syntax of the request content was correct, but it was unable to process the contained instructions.

<h2 style = "color:yellowgreen">
423 Locked
</h2>

- indicates that a resource is locked, meaning it can't be accessed.

<h2 style = "color:yellowgreen">
424 Failed Dependency
</h2>

- indicates that the method could not be performed on the resource because the requested action depended on another action, and that action failed.

<h2 style = "color:yellowgreen">
425 Too Early
</h2>

- Idicates that the server was unwilling to risk processing a request that might be replayed to avoid potential replay attacks.

<h2 style = "color:yellowgreen">
426 Upgrade Required
</h2>
 
 - indicates that the server refused to perform the request using the current protocol but might be willing to do so after the client upgrades to a different protocol.

<h2 style = "color:yellowgreen">
428 Precondition Required
</h2>

- indicates that the server requires the request to be conditional.

<h2 style = "color:yellowgreen">
429 Too Many Requests
</h2>

- indicates the client has sent too many requests in a given amount of time. This mechanism of asking the client to slow down the rate of requests is commonly called "rate limiting".

<h2 style = "color:yellowgreen">
431 Request Header Fields Too Large
</h2>

- indicates that the server refuses to process the request because the request's HTTP headers are too long. The request may be resubmitted after reducing the size of the request headers.

 <h2 style = "color:yellowgreen">
451 Unavailable For Legal Reasons
</h2>

- indicates that the user requested a resource that is not available due to legal reasons, such as a web page for which a legal action has been issued.

<br>

# 5. Server error responses

A server's reply to a client in response to an HTTP request is known as an HTTP response. It includes the resource being requested, its status, and any additional pertinent data. The request-response model underlies all communications between your browser and a website.

### <ins> Types of Server error responses.</ins>

<h2 style = "color:yellowgreen">
500 Internal Server Error
</h2>

- indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.

 <h2 style = "color:yellowgreen">
501 Not Implemented
</h2>

- means that the server does not support the functionality required to fulfill the request.

  <h2 style = "color:yellowgreen">
502 Bad Gateway
</h2>

- indicates that a server was acting as a gateway or proxy and that it received an invalid response from the upstream server.

  <h2 style = "color:yellowgreen">
503 Service Unavailable
</h2>

- indicates that the server is not ready to handle the request.

  <h2 style = "color:yellowgreen">
504 Gateway Timeout
</h2>

- indicates that the server, while acting as a gateway or proxy, did not get a response in time from the upstream server in order to complete the request. This is similar to a 502 Bad Gateway, except that in a 504 status, the proxy or gateway did not receive any HTTP response from the origin within a certain time.

<h2 style = "color:yellowgreen">
505 HTTP Version Not Supported
</h2>

- indicates that the HTTP version used in the request is not supported by the server.

 <h2 style = "color:yellowgreen">
506 Variant Also Negotiates
</h2>

- is returned during content negotiation when there is recursive loop in the process of selecting a resource.

 <h2 style = "color:yellowgreen">
507 Insufficient Storage
</h2>

- indicates that an action could not be performed because the server does not have enough available storage to successfully complete the request.

<h2 style = "color:yellowgreen">
508 Loop Detected
</h2>

- indicates that the entire operation failed because it encountered an infinite loop while processing a request with Depth: infinity.

<h2 style = "color:yellowgreen">
510 Not Extended
</h2>

- is sent when the client request declares an HTTP Extension that should be used to process the request, but the extension is not supported.

<h2 style = "color:yellowgreen">
511 Network Authentication Required
</h2>

- indicates that the client needs to authenticate to gain network access. This status is not generated by origin servers, but by intercepting proxies that control access to a network.

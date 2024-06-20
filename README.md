<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [HTTP Response Status Codes](#http-response-status-codes)
  - [Responses are grouped in five classes:](#responses-are-grouped-in-five-classes)
  - [1. Informational Responses (100 – 199)](#1-informational-responses-100--199)
  - [2. Successful Responses (200 – 299)](#2-successful-responses-200--299)
  - [3. Redirection Messages (300 – 399)](#3-redirection-messages-300--399)
  - [4. Client Error Responses (400 – 499)](#4-client-error-responses-400--499)
  - [5. Server Error Responses (500 – 599)](#5-server-error-responses-500--599)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



- [HTTP Response Status Codes](#http-response-status-codes)
  - [Responses are grouped in five classes:](#responses-are-grouped-in-five-classes)
  - [1. Informational Responses (100 – 199)](#1-informational-responses-100--199)
  - [2. Successful Responses (200 – 299)](#2-successful-responses-200--299)
  - [3. Redirection Messages (300 – 399)](#3-redirection-messages-300--399)
  - [4. Client Error Responses (400 – 499)](#4-client-error-responses-400--499)
  - [5. Server Error Responses (500 – 599)](#5-server-error-responses-500--599)


# HTTP Response Status Codes
HTTP response status codes indicate whether a specific HTTP request has been successfully completed. 
## Responses are grouped in five classes:
1. Informational responses (100 – 199)

2. Successful responses (200 – 299)

3. Redirection messages (300 – 399)

4. Client error responses (400 – 499)

5. Server error responses (500 – 599)

## 1. Informational Responses (100 – 199)
**100 Continue:** 
 - The client should continue the request or ignore the response if the request is already finished.

**101 Switching Protocols:**
- Sent in response to an Upgrade request header, indicating the protocol the server is switching to.

**102 Processing (WebDAV):**
- The server has received and is processing the request, but no response is available yet.

**103 Early Hints:**
- Intended to be used with the Link header to let the user agent start preloading resources while the server prepares a response.

## 2. Successful Responses (200 – 299)

**200 OK:** 
- The request succeeded. The meaning of "success" depends on the HTTP method (e.g.,
  - GET: resource fetched,
  - POST: resource created).

**201 Created:** 
- The request succeeded, and a new resource was created as a result.

**202 Accepted:**
 - The request has been received but not yet acted upon; processing is not complete.

**203 Non-Authoritative Information:**
- The returned metadata is not exactly the same as available from the origin server, often used for mirrors or backups.

**204 No Content:** 
- No content to send for this request, but headers may be useful.

**205 Reset Content:**
-  Instructs the user agent to reset the document view (e.g., clear form data).

**206 Partial Content:**
- Sent when the client requests only part of a resource using the Range header.

**207 Multi-Status (WebDAV):**
- Conveys information about multiple resources.

**208 Already Reported (WebDAV):**
-  Avoids repeatedly enumerating the internal members of multiple bindings to the same collection.

**226 IM Used (HTTP Delta encoding):**
-  The server has fulfilled a GET request and the response represents the result of instance-manipulations.


## 3. Redirection Messages (300 – 399)
1. **300 Multiple Choices**: The request has more than one possible response; the user should choose one.
2. **301 Moved Permanently**: The URL of the requested resource has been permanently changed.
3. **302 Found**: The URI of the requested resource has been temporarily changed.
4. **303 See Other**: Directs the client to get the requested resource at another URI with a GET request.
5. **304 Not Modified**: Used for caching purposes, indicating the response has not been modified.
6. **307 Temporary Redirect**: Directs the client to get the requested resource at another URI using the same method.
7. **308 Permanent Redirect**: The resource is permanently located at another URI, with the same method required.

## 4. Client Error Responses (400 – 499)
1. **400 Bad Request**: The server cannot or will not process the request due to client error (e.g., malformed request syntax).
2. **401 Unauthorized**: Authentication is required and has failed or has not been provided.
3. **403 Forbidden**: The client does not have access rights to the content.
4. **404 Not Found**: The requested resource could not be found on the server.
5. **405 Method Not Allowed**: The request method is known by the server but not supported by the target resource.
6. **406 Not Acceptable**: The server does not find any content conforming to the criteria given by the user agent.
7. **407 Proxy Authentication Required**: Similar to 401 Unauthorized but requires authentication by a proxy.
8. **408 Request Timeout**: The server would like to shut down the unused connection.
9. **409 Conflict**: The request conflicts with the current state of the server.
10. **410 Gone**: The requested content has been permanently deleted from the server.
11. **411 Length Required**: The server requires the Content-Length header field.
12. **412 Precondition Failed**: The server does not meet the preconditions specified by the client.
13. **413 Payload Too Large**: The request entity is larger than the server is willing to process.
14. **414 URI Too Long**: The URI requested is longer than the server is willing to interpret.
15. **415 Unsupported Media Type**: The media format of the requested data is not supported by the server.
16. **416 Range Not Satisfiable**: The range specified by the Range header cannot be fulfilled.
17. **417 Expectation Failed**: The expectation given in the Expect request header cannot be met by the server.
18. **426 Upgrade Required**: The server refuses to perform the request using the current protocol, requiring an upgrade.
19. **429 Too Many Requests**: The user has sent too many requests in a given amount of time.
20. **431 Request Header Fields Too Large**: The server is unwilling to process the request because the header fields are too large.
21. **451 Unavailable For Legal Reasons**: The user agent requested a resource that cannot legally be provided.

## 5. Server Error Responses (500 – 599)
1. **500 Internal Server Error**: The server encountered an unexpected condition preventing it from fulfilling the request.
2. **501 Not Implemented**: The request method is not supported by the server.
3. **502 Bad Gateway**: The server, while acting as a gateway, received an invalid response from the upstream server.
4. **503 Service Unavailable**: The server is currently unable to handle the request due to temporary overloading or maintenance.
5. **504 Gateway Timeout**: The server, while acting as a gateway, did not receive a timely response from the upstream server.
6. **505 HTTP Version Not Supported**: The HTTP version used in the request is not supported by the server.
7. **507 Insufficient Storage (WebDAV)**: The server cannot store the representation needed to complete the request.

---
date:
  created: 2024-09-25
  updated: 2024-09-25
readtime: 10
pin: false
links:
  - Homepage: index.md#project-layout
  - Blog index: blog/index.md
  - External links:
    - Web Page: https://adnankaya.github.io
categories:
  - Junior
  - Interview
tags:
  - interview
  - junior
  - questions and answers
  - coding interview
  - programming interview
  - web development fundamentals
authors:
  - adnankaya
slug: interview-questions-and-answers-for-web-development-fundamentals
---

# 100 Web Development Fundamentals Interview Questions and Answers

Checkout our curated list of interview questions and answers for web development fundamentals

<!-- more -->

???+ question "1. What is the role of the HTTP protocol in web development?" 
    Answer: The HTTP protocol is responsible for communication between web browsers and web servers. It defines the rules and formats for requesting and receiving web resources like HTML, CSS, and JavaScript files.

??? question "2. What is a request and response in HTTP?"
    Answer: In HTTP, a request is sent by the client (browser) to the server to ask for resources, and a response is the server's reply with the requested data. For example, when you type a URL into your browser, it sends a request, and the server responds with the webpage.

??? question "3. What is the difference between GET and POST methods in HTTP?"
    Answer: GET requests retrieve data from the server, while POST requests send data to the server, often used for submitting forms. GET appends parameters in the URL, whereas POST sends data in the body, making it more secure for sensitive information.

??? question "4. What is a REST API?"
    Answer: A REST API is a web service that uses HTTP requests to perform CRUD (Create, Read, Update, Delete) operations on resources. It follows the principles of REST, such as statelessness and resource-based URLs.

??? question "5. What does statelessness mean in REST?"
    Answer: Statelessness means that each request in a REST API is independent, and the server does not store client context between requests. This makes REST APIs scalable, as no session data is retained on the server.

??? question "6. What are headers in an HTTP request?"
    Answer: Headers contain metadata about the request or response, such as content type, authentication tokens, and caching rules. They help control how the server and client interact with each other.

??? question "7. What is a status code in an HTTP response?"
    Answer: HTTP status codes are numerical responses from the server indicating the result of the request. For example, 200 means success, 404 means resource not found, and 500 indicates a server error.

??? question "8. What is the purpose of cookies in web development?"
    Answer: Cookies store small pieces of data in the user's browser to maintain state between requests, such as user authentication tokens or session identifiers. They help track user sessions in stateless HTTP communication.

??? question "9. What is the difference between HTTP and HTTPS?"
    Answer: HTTPS is the secure version of HTTP, where data is encrypted using SSL/TLS, ensuring secure transmission between the browser and server. It is crucial for protecting sensitive information like login credentials.

??? question "10. What is caching, and how does it improve web performance?"
    Answer: Caching stores copies of resources like images, scripts, or data on the client or server to avoid redundant data fetching. It improves web performance by reducing the need for repeated server requests, making pages load faster.

??? question "11. What is a browser cache?"
    Answer: A browser cache stores local copies of web resources (such as images, CSS, and JavaScript) to reduce load times for subsequent visits. This reduces the need to fetch resources from the server every time a page is loaded.

??? question "12. What is the purpose of the Content-Type header?"
    Answer: The Content-Type header tells the server or browser what type of data is being sent or received, such as "text/html" for HTML documents or "application/json" for JSON data. It ensures that data is processed correctly.

??? question "13. What is Cross-Origin Resource Sharing (CORS)?"
    Answer: CORS is a security feature that allows or restricts web pages from making requests to a different domain than the one that served the page. It prevents unauthorized data sharing between websites.

??? question "14. What are query parameters in an HTTP URL?"
    Answer: Query parameters are key-value pairs added to the end of a URL to pass data to the server, often used in GET requests. They follow a "?" and are separated by "&", like `example.com/page?name=value`.

??? question "15. What are RESTful resources?"
    Answer: In REST, resources are objects or data that can be accessed and manipulated through specific endpoints (URLs). Each resource is represented by a URL and is manipulated using standard HTTP methods (GET, POST, PUT, DELETE).

??? question "16. What are the advantages of using REST APIs?"
    Answer: REST APIs are simple, scalable, and stateless, making them easy to implement and maintain. They use HTTP methods and can be consumed by a wide range of clients like web browsers, mobile apps, or IoT devices.

??? question "17. What is JSON, and why is it commonly used in web development?"
    Answer: JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy to read and write. It is commonly used in APIs for exchanging data between a server and a client due to its simplicity and support in many languages.

??? question "18. What is the purpose of browser developer tools?"
    Answer: Browser developer tools help developers inspect and debug web pages, allowing them to view HTML structure, CSS styles, JavaScript errors, and network requests in real-time. It aids in troubleshooting issues during development.

??? question "19. What is DOM in web development?"
    Answer: The DOM (Document Object Model) is a programming interface that represents the structure of an HTML or XML document as a tree of objects. It allows developers to manipulate the content, structure, and style of a webpage dynamically using JavaScript.

??? question "20. What is accessibility in web development?"
    Answer: Accessibility ensures that websites can be used by people with disabilities, such as those with visual impairments. This includes using semantic HTML, ARIA roles, and proper contrast ratios, making web content accessible to screen readers and assistive technologies.

??? question "21. What is the difference between a client-side and server-side request?"
    Answer: Client-side requests are made by the browser to fetch resources (HTML, CSS, JavaScript) to render a webpage, while server-side requests are handled by the server to process or retrieve data, such as querying a database. Server-side requests often involve business logic, while client-side requests manage the user interface.

??? question "22. What is a RESTful endpoint?"
    Answer: A RESTful endpoint is a URL that points to a resource on a server and is used in REST APIs to perform actions like fetching or modifying data. Each endpoint corresponds to a specific resource or set of resources and uses HTTP methods like GET, POST, PUT, and DELETE to interact with those resources.

??? question "23. What is the difference between PUT and PATCH in REST APIs?"
    Answer: PUT is used to update an entire resource, while PATCH is used to modify only specific fields of a resource. For example, PUT replaces the entire object, whereas PATCH updates a part of the object without affecting other fields.

??? question "24. What is the purpose of the Accept header in an HTTP request?"
    Answer: The `Accept` header in an HTTP request specifies the media type(s) that the client is willing to receive from the server, such as `application/json` or `text/html`. It helps the server determine the format in which to send the response data.

??? question "25. What is a 301 redirect, and when should it be used?"
    Answer: A 301 redirect is a permanent redirection from one URL to another. It is used when a webpage has been moved permanently to a new URL, ensuring that users and search engines are directed to the correct location without losing SEO ranking.

??? question "26. What is the purpose of the 403 status code?"
    Answer: The 403 status code indicates that the server understands the request, but the client is not authorized to access the requested resource. It usually means that the client does not have sufficient permissions to view or manipulate the data.

??? question "27. What is lazy loading in web development?"
    Answer: Lazy loading is a performance optimization technique where resources such as images or scripts are only loaded when they are needed (e.g., when they appear in the viewport). This reduces the initial load time and improves performance for users.

??? question "28. What is a service worker, and how does it improve web performance?"
    Answer: A service worker is a script that runs in the background, separate from the main browser thread, and can cache resources, handle network requests, and enable offline functionality. It improves performance by serving cached content and reducing network dependency.

??? question "29. What is the difference between synchronous and asynchronous requests in web development?"
    Answer: Synchronous requests block the browser from performing any other operations until the request is complete, while asynchronous requests allow the browser to continue processing other tasks while waiting for the response. Asynchronous requests, such as those made with `fetch` or `XMLHttpRequest`, are commonly used in web development to avoid blocking the user interface.

??? question "30. What is a web form, and how is it used in web development?"
    Answer: A web form is an HTML element that collects user input and sends it to a server for processing, often using POST or GET requests. Web forms are used for tasks like submitting data, logging in, or registering for services.

??? question "31. What is the difference between a 404 and 410 status code?"
    Answer: A 404 status code indicates that the resource is not found and may be temporarily missing, while a 410 status code means that the resource is gone permanently and will not be available in the future. Use 410 when you know the resource has been deliberately removed.

??? question "32. What is Content Delivery Network (CDN), and how does it improve web performance?"
    Answer: A CDN is a network of servers distributed globally to deliver content to users based on their geographical location. It improves performance by reducing latency and bandwidth usage by serving cached resources from servers closer to the user.

??? question "33. What is the difference between server-side rendering and client-side rendering?"
    Answer: Server-side rendering (SSR) generates the HTML on the server and sends the fully-rendered page to the client, improving initial load times. Client-side rendering (CSR) sends an initial HTML shell, and the browser renders the page using JavaScript, often making the page interactive after loading additional data.

??? question "34. What is the role of the Cache-Control header in web development?"
    Answer: The `Cache-Control` header specifies caching policies for both the client and the server. It can define how long a resource should be cached, whether it can be stored by intermediaries, or if it needs to be revalidated before reuse. It optimizes performance by controlling cache behavior.

??? question "35. What is semantic HTML, and why is it important for accessibility?"
    Answer: Semantic HTML uses meaningful tags like `<header>`, `<article>`, and `<footer>` that describe the structure and content of a webpage. It improves accessibility by allowing assistive technologies to better understand and navigate the content, making the web more inclusive for all users.

??? question "36. What is a 500 Internal Server Error?"
    Answer: A 500 Internal Server Error is a generic status code indicating that something went wrong on the server, but the server could not provide more specific information. It usually signals server-side issues like a misconfigured script or database failure.

??? question "37. What is prefetching in web development?"
    Answer: Prefetching is a technique used to load resources or data before they are needed by the user. For example, when a user is likely to navigate to another page, prefetching can download assets for that page in the background to improve performance when the user clicks the link.

??? question "38. What is an API rate limit, and why is it important?"
    Answer: API rate limits control the number of requests a client can make to a server within a given timeframe, protecting the server from being overwhelmed. It is important to prevent abuse, ensure fair usage, and maintain the stability of the service.

??? question "39. What is the purpose of ARIA (Accessible Rich Internet Applications)?"
    Answer: ARIA is a set of attributes that help improve the accessibility of web content, especially for dynamic content and web applications. It enables assistive technologies like screen readers to better interpret and interact with custom UI elements by providing additional context or descriptions.

??? question "40. What is a web service, and how does it differ from a web API?"
    Answer: A web service is a software system designed to communicate over a network using standardized protocols like HTTP, often returning data in formats like XML or JSON. A web API is a subset of web services, typically designed to expose application functionality over HTTP using REST principles.

??? question "41. What is throttling in web development?"
    Answer: Throttling limits the number of times a function or event handler can be called over a given time period, often used in scrolling, resizing, or API requests. It helps improve performance by preventing resource-heavy operations from being triggered too frequently.

??? question "42. What is minification, and how does it improve web performance?"
    Answer: Minification removes unnecessary characters like whitespace, comments, and line breaks from code (JavaScript, CSS) to reduce file size without changing functionality. It improves performance by reducing the amount of data that needs to be transferred over the network.

??? question "43. What is a WebSocket, and how does it differ from HTTP?"
    Answer: WebSocket is a communication protocol that allows for real-time, bidirectional communication between the client and server. Unlike HTTP, which is request/response-based, WebSocket enables continuous data exchange without needing to re-establish connections for each request.

??? question "44. What is the purpose of `async` and `defer` attributes in `<script>` tags?"
    Answer: The `async` attribute loads the script asynchronously, allowing the page to continue loading while the script is fetched. The `defer` attribute delays script execution until the HTML document is fully parsed. Both improve page load performance by preventing blocking of other resources.

??? question "45. What is the difference between a 302 and 307 redirect?"
    Answer: A 302 redirect is a temporary redirection where the browser may change the HTTP method of the request (e.g., from POST to GET), while a 307 redirect is also temporary but ensures that the HTTP method remains unchanged. Use 307 when you want to retain the original method.

??? question "46. What is the role of cookies in HTTP?"
    Answer: Cookies store small amounts of data on the client-side, typically used to maintain sessions, track user preferences, or authenticate users. They are sent with HTTP requests and responses and allow the server to "remember" the user across different requests.

??? question "47. What is Cross-Origin Resource Sharing (CORS)?"
    Answer: CORS is a security feature implemented by browsers to prevent cross-origin requests unless explicitly allowed by the server. It controls how resources on one domain are requested by another domain, protecting against unauthorized access or data leaks.

??? question "48. What is the purpose of a `Content-Type` header in HTTP?"
    Answer: The `Content-Type` header in HTTP defines the media type of the resource being sent, such as `application/json` or `text/html`. It helps the browser or client understand how to interpret the data in the response or request.

??? question "49. What is a status code, and why is it important in HTTP?"
    Answer: A status code is a three-digit number sent by the server in response to an HTTP request, indicating the result of the request. For example, `200 OK` means success, while `404 Not Found` means the resource could not be found. They provide insights into the success or failure of a request.

??? question "50. What is JSON, and why is it widely used in web development?"
    Answer: JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for both humans and machines to read and write. It is widely used for APIs because of its simplicity, structure, and compatibility with many programming languages.

??? question "51. What is the difference between a GET and POST request in HTTP?"
    Answer: GET requests retrieve data from the server without changing its state, while POST requests are used to send data to the server, typically resulting in a change of state or side effects like creating a new resource. GET parameters are appended to the URL, while POST data is included in the request body.

??? question "52. What are web performance metrics, and why are they important?"
    Answer: Web performance metrics measure the speed and efficiency of loading and interacting with a website. Common metrics include Time to First Byte (TTFB), First Contentful Paint (FCP), and Largest Contentful Paint (LCP). Optimizing these metrics improves user experience and SEO rankings.

??? question "53. What is a user agent in HTTP?"
    Answer: A user agent is a string sent by the browser or client in an HTTP request to identify itself to the server. It typically includes details about the browser, operating system, and device. Servers can use this information to customize responses or optimize content delivery.

??? question "54. What is latency, and how does it affect web performance?"
    Answer: Latency refers to the delay between a user's request and the server's response. High latency can result in slower page load times and a poor user experience. Reducing latency through techniques like using a CDN or optimizing server-side code improves performance.

??? question "55. What is a resource hint in web development?"
    Answer: Resource hints are directives that inform the browser to proactively fetch or prioritize certain resources, such as DNS prefetching, preloading, or prerendering. These hints improve performance by reducing delays in loading critical resources.

??? question "56. What is the `OPTIONS` method in HTTP?"
    Answer: The `OPTIONS` method in HTTP is used to describe the communication options available for a specific URL or server. It is often used in preflight requests for CORS to determine which HTTP methods and headers are allowed by the server.

??? question "57. What is the difference between a session and a token in web authentication?"
    Answer: A session is typically stored on the server and associated with a unique session ID that is passed to the client via cookies. Tokens, like JSON Web Tokens (JWT), are stored client-side and sent with each request to authenticate users. Sessions are stateful, while tokens are stateless.

??? question "58. What is the difference between an HTTP and HTTPS request?"
    Answer: HTTP is an unencrypted protocol for transferring data, while HTTPS adds a layer of encryption using SSL/TLS to secure communication. HTTPS protects against man-in-the-middle attacks and ensures the confidentiality and integrity of data exchanged between clients and servers.

??? question "59. What is a network waterfall in browser developer tools?"
    Answer: A network waterfall is a visual representation in browser developer tools that shows the timeline and order of resources being requested and loaded on a webpage. It helps developers identify bottlenecks, slow-loading resources, and areas for optimization.

??? question "60. What is a CDN cache, and how does it benefit users?"
    Answer: A CDN cache stores copies of resources on edge servers closer to users. It reduces the distance data needs to travel, leading to faster load times, reduced bandwidth usage, and improved performance, especially for users far from the origin server.

??? question "61. What is HTTP/2, and how does it improve web performance?"
    Answer: HTTP/2 is a major revision of the HTTP protocol that improves performance through features like multiplexing, header compression, and server push. It allows multiple requests and responses to be sent simultaneously over a single connection, reducing latency and improving load times.

??? question "62. What is a 502 Bad Gateway error, and how is it typically resolved?"
    Answer: A 502 Bad Gateway error occurs when a server acting as a gateway or proxy receives an invalid response from an upstream server. It is typically resolved by checking the upstream server, fixing network connectivity, or ensuring proper server configurations.

??? question "63. What is the role of a `User-Agent` string in HTTP requests?"
    Answer: The `User-Agent` string identifies the browser, operating system, and device making the HTTP request. Servers use this information to optimize responses, adjust content formatting, or serve device-specific resources (e.g., mobile vs. desktop).

??? question "64. What is DNS, and why is DNS resolution important for web performance?"
    Answer: DNS (Domain Name System) translates domain names into IP addresses that browsers can use to locate web servers. DNS resolution time is important for web performance because slow DNS lookups can delay initial page loading.

??? question "65. What is HTTP pipelining, and why is it not widely used?"
    Answer: HTTP pipelining allows multiple HTTP requests to be sent on a single connection without waiting for each response. However, it is not widely used due to issues with head-of-line blocking and inconsistent support across browsers, which led to the adoption of multiplexing in HTTP/2.

??? question "66. What is the difference between a first-party and third-party cookie?"
    Answer: First-party cookies are set by the website the user is visiting, while third-party cookies are set by domains other than the one the user is visiting (e.g., ads, trackers). First-party cookies are used for user sessions, while third-party cookies often track user behavior across different sites.

??? question "67. What is an ETag in HTTP, and how does it improve performance?"
    Answer: An ETag (Entity Tag) is a unique identifier assigned to a specific version of a resource. It helps with caching by allowing the server to check if the resource has changed and only send updated data when necessary, reducing bandwidth and improving performance.

??? question "68. What is `defer` in HTML script tags, and when should it be used?"
    Answer: The `defer` attribute in HTML tells the browser to load and execute the script after the HTML document has been fully parsed. It is useful for improving performance, especially when dealing with non-essential scripts that should not block the rendering of the page.

??? question "69. What is TLS, and how does it relate to HTTPS?"
    Answer: TLS (Transport Layer Security) is a cryptographic protocol that ensures secure communication over a network by encrypting data between the client and server. HTTPS uses TLS to provide a secure version of HTTP, protecting data from being intercepted or tampered with.

??? question "70. What is a web accessibility audit, and why is it important?"
    Answer: A web accessibility audit is a review of a website to ensure it meets accessibility standards like WCAG (Web Content Accessibility Guidelines). It is important because it ensures that people with disabilities can access and use the website, improving inclusivity and user experience.

??? question "71. What is caching, and why is it important in web development?"
    Answer: Caching is the process of storing copies of resources, such as images or scripts, to reduce the need to fetch them repeatedly from the server. It improves performance by reducing load times, decreasing server load, and minimizing bandwidth usage.

??? question "72. What is a `Content-Security-Policy` header, and why is it used?"
    Answer: The `Content-Security-Policy` (CSP) header is a security feature that defines approved sources of content (scripts, styles, media) for a website. It helps prevent cross-site scripting (XSS) attacks by restricting the types of content that can be executed or loaded by the browser.

??? question "73. What is lazy loading, and how does it improve web performance?"
    Answer: Lazy loading is a technique that delays the loading of non-critical resources, such as images, until they are actually needed (e.g., when the user scrolls to them). This improves performance by reducing the initial page load time and conserving bandwidth.

??? question "74. What is the difference between inline and external CSS?"
    Answer: Inline CSS is written directly within an HTML element's `style` attribute, while external CSS is written in a separate `.css` file and linked to the HTML document. External CSS is preferred for maintainability and reusability, while inline CSS is sometimes used for small, immediate styling changes.

??? question "75. What is the difference between client-side and server-side rendering?"
    Answer: Client-side rendering happens in the browser, where JavaScript fetches content and updates the page dynamically, while server-side rendering generates the HTML content on the server before sending it to the client. Client-side rendering offers smoother interactions but can have longer initial load times, while server-side rendering typically loads faster but may be less dynamic.

??? question "76. What is the purpose of HTTP headers?"
    Answer: HTTP headers provide additional information about an HTTP request or response, such as content type, caching rules, and authentication tokens. They help the client and server communicate more effectively by conveying metadata alongside the actual data.

??? question "77. What is the difference between HTTP and WebSockets?"
    Answer: HTTP is a stateless, request-response protocol where the client initiates the request, and the server responds. WebSockets, on the other hand, provide full-duplex communication, allowing data to be sent and received by both client and server at any time, making it ideal for real-time applications like chat apps.

??? question "78. What is a critical rendering path in web development?"
    Answer: The critical rendering path refers to the sequence of steps a browser takes to convert HTML, CSS, and JavaScript into a visible webpage. Optimizing the critical rendering path by minimizing file sizes and deferring non-essential resources improves page load performance.

??? question "79. What is an HTTP `PATCH` request, and when would you use it?"
    Answer: An HTTP `PATCH` request is used to partially update a resource on the server. It differs from `PUT`, which replaces the entire resource, whereas `PATCH` only modifies specific fields or properties. It is used when small changes are needed without affecting the entire resource.

??? question "80. What is a media query, and how does it help in responsive design?"
    Answer: A media query is a CSS technique that allows the application of styles based on the characteristics of the user's device, such as screen size or resolution. Media queries are essential for building responsive websites that adjust layouts for different devices (e.g., desktops, tablets, mobile phones).

??? question "81. What is the purpose of a `viewport` meta tag in HTML?"
    Answer: The `viewport` meta tag controls the scaling and sizing of a webpage on different devices. It is crucial for responsive design, as it allows developers to set the viewport width and scale, ensuring that the website displays correctly on mobile devices and smaller screens.

??? question "82. What is the difference between a `403 Forbidden` and a `401 Unauthorized` HTTP status code?"
    Answer: A `401 Unauthorized` status code indicates that authentication is required, but the user has not provided valid credentials. A `403 Forbidden` status code means that the user is authenticated but does not have the necessary permissions to access the resource.

??? question "83. What is the difference between the `POST` and `PUT` methods in HTTP?"
    Answer: The `POST` method is used to create a new resource on the server, while the `PUT` method is used to update an existing resource or create it if it does not exist. `POST` is generally used when the server decides the URL of the resource, while `PUT` specifies the URL.

??? question "84. What is the purpose of minifying CSS and JavaScript?"
    Answer: Minifying CSS and JavaScript removes unnecessary characters, such as whitespace and comments, without affecting functionality. This reduces file size, leading to faster load times and improved performance.

??? question "85. What is a DNS lookup, and how does it affect web performance?"
    Answer: A DNS lookup is the process of converting a domain name (like `example.com`) into an IP address that browsers can use to locate the server. Slow DNS lookups can delay the loading of web pages, affecting performance. Using a CDN or caching DNS queries can help speed this up.

??? question "86. What is the difference between the `200 OK` and `201 Created` status codes in HTTP?"
    Answer: A `200 OK` status code indicates that a request has succeeded, typically used for GET or POST requests. A `201 Created` status code is used when a new resource has been successfully created on the server, typically in response to a POST request.

??? question "87. What is the role of the `Accept` header in an HTTP request?"
    Answer: The `Accept` header in an HTTP request informs the server about the types of content the client can process, such as `application/json` or `text/html`. The server uses this information to send back the appropriate content type.

??? question "88. What is the `Accept-Encoding` header, and how does it affect performance?"
    Answer: The `Accept-Encoding` header specifies the types of compression the client can handle (e.g., `gzip`, `deflate`). By using compression, the server can reduce the size of the data sent to the client, improving performance by decreasing load times and bandwidth usage.

??? question "89. What is the purpose of content negotiation in HTTP?"
    Answer: Content negotiation is the process by which the client and server determine the best format for the response, based on the client's `Accept` headers and the server's capabilities. It allows the server to deliver the most appropriate content type (e.g., HTML, JSON, XML) for the client's needs.

??? question "90. What is a memory leak, and how does it affect web performance?"
    Answer: A memory leak occurs when a program fails to release memory that is no longer needed, causing it to consume more memory over time. In web development, memory leaks in JavaScript can degrade performance, leading to slower interactions and potentially crashing the browser.

??? question "91. What is preloading in web development?"
    Answer: Preloading is a performance optimization technique that allows developers to instruct the browser to load certain critical resources (like fonts or images) early, before they are requested in the normal rendering flow. It reduces resource loading delays, improving the overall performance of the page.

??? question "92. What is an HTTP `HEAD` request, and when should it be used?"
    Answer: An HTTP `HEAD` request retrieves the headers of a resource, without fetching its body. It is used when a client wants to check metadata (e.g., content type, last modified date) without downloading the resource, which can save bandwidth and improve efficiency.

??? question "93. What is long polling, and how does it differ from WebSockets?"
    Answer: Long polling is a technique where the client makes a request to the server, and the server holds the request open until it has new data to send, simulating real-time updates. Unlike WebSockets, which offer full-duplex communication, long polling repeatedly opens and closes HTTP connections.

??? question "94. What is the `Cache-Control` header, and how does it impact performance?"
    Answer: The `Cache-Control` header specifies caching policies for HTTP requests and responses, such as how long a resource should be cached by the client or intermediary caches. Effective caching improves performance by reducing server load and decreasing page load times.

??? question "95. What is the `Last-Modified` header in HTTP?"
    Answer: The `Last-Modified` header indicates the last time a resource was modified on the server. When used in combination with caching, it allows clients to make conditional requests (e.g., `If-Modified-Since`) to check whether the resource has changed and avoid downloading it unnecessarily.

??? question "96. What is a 503 Service Unavailable error?"
    Answer: A `503 Service Unavailable` error occurs when the server is temporarily unable to handle the request, often due to being overloaded or undergoing maintenance. It indicates that the server should be available again after some time.

??? question "97. What is the difference between a `GET` request and a `DELETE` request in HTTP?"
    Answer: A `GET` request retrieves data from the server, while a `DELETE` request is used to remove a resource from the server. `GET` is used for safe operations (no state changes), while `DELETE` modifies the server's state by removing resources.

??? question "98. What is DNS prefetching, and how does it improve performance?"
    Answer: DNS prefetching is a browser feature that pre-resolves domain names before the user navigates to them, reducing the time spent on DNS lookups. By resolving these names early, the browser can load resources faster, improving page load performance.

??? question "99. What is the difference between `300 Multiple Choices` and `301 Moved Permanently` in HTTP?"
    Answer: A `300 Multiple Choices` status code indicates that multiple possible responses are available, and the client can choose one. A `301 Moved Permanently` status code tells the client that the requested resource has been permanently moved to a new URL, and all future requests should be directed there.

??? question "100. What is the difference between a resource being cached by a browser and a resource being cached by a CDN?"
    Answer: When a browser caches a resource, it stores it locally on the user's device, so it can be quickly accessed without re-downloading it on subsequent visits. When a CDN caches a resource, it is stored on a distributed network of servers closer to the user, reducing latency and improving performance for all visitors to the site."

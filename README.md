# 📝Tutorial & Exercise📝

**Student Details :**

|  Attribute  | Information              |
|---------------|----------------------------|
| Name          | Andika Pramudya Wardana    |
| Student ID    | 2206046645              |
| Class         | Advanced Programming KKI   |

---
<details>
<summary>Module 09: High Level Networking</summary>

## Questions and Answers

### -> Reflection 

#### 1. What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?
- In Unary RPC, the client sends a single request and receives a single response. This is handy for tasks like fetching data from a database or executing actions on a server.
- Server streaming RPC involves the client sending a request and getting a continuous stream of data in response, useful for real-time data like weather updates or stock prices.
- Bi-directional streaming RPC allows both client and server to exchange data streams, making it ideal for applications like chat apps or real-time collaborative software.

#### 2. What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?
- When it comes to securing gRPC services, the go-to technologies are TLS/SSL and JWT. 
- TLS/SSL encrypts data between client and server, while JWT (or similar token-based methods) verifies the identity of clients accessing the service.

#### 3. What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?
- Bi-directional streaming, while powerful, brings along concurrency challenges like race conditions and deadlocks. 
- Managing states becomes crucial, especially in scenarios like chat apps where sessions track clients' interactions.

#### 4. What are the advantages and disadvantages of using the tokio_stream::wrappers::ReceiverStream for streaming responses in Rust gRPC services?
- `ReceiverStream` plays well with tokio, a popular choice for asynchronous Rust applications. 
- However, integrating it with other asynchronous crates might be cumbersome if tokio isn't in use.

#### 5. In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?
- Splitting server and client codebases into separate functionalities (like payment, transactions, or chat) and further organizing them based on the separation of concerns principle can enhance maintainability. 
- Refactoring for reusability, adding tests, robust error handling, and thorough documentation strengthen the codebase for future development.

#### 6.  In the __MyPaymentService__ implementation, what additional steps might be necessary to handle more complex payment processing logic?
- Essential functionality like request processing, input validation, and error handling, especially for unexpected requests, needs implementation. 
- Integration with third-party payment APIs like Stripe is also necessary for processing payments.

#### 7. What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?
- gRPC's appeal lies in its use of HTTP/2, leveraging features like multiplexing, header compression, and binary encoding. 
- It also adopts Protocol Buffers (protobuf) for serialization, offering faster and lighter data exchange compared to JSON.
- Moreover, gRPC tooling can auto-generate type-safe APIs across multiple languages, enhancing developer productivity and interoperability.

#### 8. What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?
- Advantages: HTTP/2 supports multiplexing, reducing latency by allowing multiple messages on the same connection. Efficient for gRPC performance.
- Disadvantages: More complex to implement and debug; potential for issues in environments where HTTP/2 is not fully supported.

#### 9. How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?
- REST typically operates over HTTP/1.1 with stateless servers and predictable, resource-oriented URLs, using JSON. Best for web APIs accessible from browsers and for systems that require cacheable responses.
- gRPC offers bidirectional streaming and operates over HTTP/2, making it better suited for real-time and highly interactive applications where performance and efficiency are critical.

#### 10. What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?
- gRPC uses Protocol Buffers, which provide a strong type system, compact binary data format, and a strict schema, enhancing performance and robustness.
- JSON used in REST is more flexible and human-readable, easier to use for dynamic or loosely coupled systems but typically less efficient in terms of performance and type-safety.

---

</details>

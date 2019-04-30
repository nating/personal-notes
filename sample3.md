
# Q2a

* The primary goal of TLS1.3 is to provide a private and secure *connection* **channel** between to communicating peers.

* The only requirement of TLS1.3 from underlying transport is a reliable and in-order data-stream.

* TLS1.3 provides:
  * Confidentiality: Data after *the connection has been established* **establishment** can only be read by the two ends of the channel.
  * Integrity: Data after *the connection has been established* **establishment** cannot be tampered with without detection.
  * Authentication: The server side of the channel is always authenticated; the client is optionally authenticated.

* TLS1.3 can be thought of as being made up of two components: the handshake protocol and the record protocol.

* The handshake protocol *establishes the connection* **authenticates the communicating parties**, negotiates *cipher* **cryptographic** parameters and modes, and *determines details about the keys* **establishes shared keying material**. It can be thought of as having three phases; Key Exchange, Server Parameters, and Authentication.

* The record protocol is responsible for the secure delivery of application data from one peer to the other. It breaks up data from the application layer into records and encrypts each one independently. The record protocol uses AEAD ciphers exclusively. AEAD ciphers wrap up authentication and encryption into one smooth operation that changes plaintext to authenticated ciphertext and back again. In TLS1.3, records can also be padded to change the length of the TLSCiphertext. This can be used to mask the length traffic from observers.

* The handshake protocol can be seen in the diagram below:



Also to note:

*

* PSKs that have been agreed upon in previous communications can be used for session resumption.
* 0-RTT is means that

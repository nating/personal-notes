
#

* TLS1.3's primary goal is to provide **a secure channel between two communicating peers**.

* TLS1.3's only requirement from the underlying transport *layer* is a reliable, in-order *packet delivery* **data stream**.

* TLS1.3 provides:
  * Confidentiality: *Messages are end to end encrypted and can only be read by the intended recipient.* **Data sent over the channel after establishment is only visible to endpoints.**
  * Integrity: *Messages* **Data sent over the channel after establishment** cannot be tampered with without *it being caught* **detection**.
  * Authentication: The server **side of the channel** is always authenticated and the client is optionally authenticated.

* TLS1.3 can be thought of as *two protocols* **having two components**; The Handshake protocol and the Record protocol.

* The handshake protocol deals with *setting up the secure channel, negotiating the parameters of the encryption.* **authenticating the communicating parties, negotiating cryptographic modes & parameters, and establishing keying material**.

* The record part of the protocol **uses the parameters established in the handshake protocol to protect traffic between the communicating peers.**. It deals with breaking up the application layer data into records and **independently** encrypting them for transit. The record layer uses exclusively AEAD ciphers. AEAD ciphers wrap up authentication and encryption into one smooth operation that turns plaintext into authenticated cipher text and back again. TLS1.3 records can also be padded so that the TLSCiphertext is of a different length than it would be otherwise. This adds a layer of security as the length of encrypted records may give information about its contents away.**hides the size of the traffic from an observer.**

* The details of the handshake protocol can be seen in the diagram below:


...


* The handshake layer can be thought of as being three phases; Key Exchange, Server Params, and Authenticate. *As seen in the above diagram.*

Some other things to note are:

* If the *DH algorithms* **key_share extensions** put forward in the ClientHello *don't match* **are not sufficient for** the server, then the server may respond with a HelloRetryRequest. This restarts the handshake but the fact that it has been restarted is recorded so it isn't exactly as if its brand new.

* PSKs can be agreed upon in previous messages and then used again for session resumption. **If the server accepts the PSK, it can be used with DH in order to provide forward secrecy**.

* TLS1.3 has a 0-RTT mode where users can re-use the key from the last session to reinitiate the communication **sending "early data" on the first flight**, but this comes with security risks as it is vulnerable to replay attacks.

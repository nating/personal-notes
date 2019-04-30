## 2018

### Q2.

**a. ### TLS 1.2 chosen protocol**

#### Intro
Transport layer Security is the successor to the Secure Sockets Layer (TLS/SSL).
SSL was originally designed to work with any application thats uses sockets to communicate. This was standardised into TLS, which is the best common practise protocol used for for secure communication across the web.

The key exchange protocol used for TLS 1.2 is the handshake protocol. It is a series of steps which takes place whenever a Client navigates to a website using HTTPS, and starts querying the websites origin Server. TLS handshake takes occur after a TCP connection has been opened.


#### Protocol

 *"Insert Packet Diagram"*


Steps:

1. The Client start the handshake by sending a ClientHello() message. This message contains the cipher suites, sessionID, compression methods and Client random number. The cipher suits is the collection of encryption methods the Client is capable of. The Client random is a random string of bytes which is used in generating the master secret key.
2. The Server responds with a ServerHello() message. This message also contains a sessionID, the Servers Ciphersuites and compression methods. The Server also sends back "Server random", a random string of bytes to be used generating the master secret key. The Server also send back its SSL certificate. The it send a SeverHello() done message.
3. The Client receives this and verifies the Servers identity with the certificate authority, using its SSL certificate. The Client then generates a premasterSecret. This is a random string of 48 bytes which is encrypted using the Servers public key. The public key was obtained from the CA. The Client also sends the chosen cipher suite based on capabilities of Server and Client.
4. The Server decrypts the premaster secret using its private key. The master secret key is computed by both the Client and Server using the premasterSecret, client and server random.

        masterSecret = f(premasterSecret, clientRandom, serverRandom)

5. Using the masterSecret a keyBlock is generated and from this the session keys of the connection are generated.

        keyBlock = f(masterSecret, clientRandom, serverRandom)
6. If they arrive at same results a finish message is sent


#### Application Layer

In order to apply the keys to the application layers, the stream is divided into blocks. The keyBlock stream is the compressed. The MAC address of the user is added to the data and its also padded. This is all encrypted and the application layer protocol version is added to the stream, along with the payload length and an application data indicator.


**Application Layer Protocol Negotiation ALPN**
ALPN is a TLS 1.2 extension that allows a client and server to agree on which application layer protocol they want to use. This is primarily a choice between HTTP 1.2 or H2. In TLS 1.2 it is sent in clear non-encrypted messages.
SNI

**Server Name Identification SNI**
SNI must be supported in TLS 1.2. The reason this is needed is as follows. The TLS handshake happens before application layer communication starts. Name based virtual servers share same certificate for their one server. This is problematic.

**Solution:** Add the server virtual host name as an extension. TLS extensions allow users to include a SNI extension in the extended ClientHello handshake message. This extension immediately lets the server know which name server the Client wishes to connect to, so the server can send the appropriate certificate. TLS 1.2 does not provide confidentiality for handshake extensions like SNI.



#### networking and problems

Efforts in TLS 1.3 were made to handle ClientHello retransmission via the HelloRetryRequest. Efforts were also made to decrease handshake time via 0-RTT connections. These methods are not implemented in TLS 1.2 and retransmission is done on a timeout, not by the Sever sending a HelloRetryRequest.

Session


**b.**

**HSTS**

TLS stripping is a Man in the middle attack which makes a users browser communicate with an agent in plaintext over http. This is essentially done by stripping the the 's' from https urls. **HSTS** is the Solution to this, and is implemented in TLS 1.2.

HTTP Strict Transport Security (HSTS) is a security policy mechanism which allows web servers to declare that web browsers/agents should only interact with them using a HTTPS connection. It specifies a period of time the clients and subdomains should maintain this for.

For TLS 1.2 HTTP clients and servers MUST support this. HTTP severs SHOULD use this.


**Compression**

The CRIME (Compression ratio info-leak made easy) attack showed the vulnerabilities of compression techniques made of HTTPS connections. The attack works on all TLS versions, including 1.2. It relies on compression functions revealing patterns in plaintext. Compression functions work by finding by finding repeated patterns and including them once. Every request includes a cookie, which associates the request with a user. The attacker can then observe the change in compressed payload size, which contains both the secret and cookie sent by a browser to a site. Once the content is smaller after compression it allows you to make good guesses from the ciphertext.

For this reason compression SHOULD be disabled in TLS 1.2.


**Certificate Transparency**
Certificate Transparency is an important aspect when having a large DB of public keys. Sites need to be able to check if someone else has claimed them. Compromised revoking authorities can ask to a CA to issue certificate which has already been issued by another CA.

**c.**

Infrastructure:

State level attackers will have greater vantage points. For example undersea fibre termination points or network switches. Industrial attackers will tend to exploit a certain node to get at a target.


## 2017


**b.**

Work on TLS 1.3 began in 2014 with the intention of dropping less desirable algorithms with the intention of moving toward AEAD (Authenticated Encryption with associated data) encryption forms.

The most notable efforts of 1.3 is the intention of shortening the handshake protocol to a 1-RTT (Round Trip Time) and 0-RTT resumption. The previous handshake protocol was changed to protocol described below.


  *"Insert Packet Diagram"*


1-RTT is aimed at reducing the handshake time. 0-RTT was added with the idea that returning recently visited are resuming a previous connection.

#### Barriers

There are several issues with 0-RTT. 0-RTT is poor terminology as the client first needs a PSK, and doesn't get an answer for at least 1-RTT.
A security problem is that early-data sent can be replayed. If an attacker records a 0-RTT message including early data, they can replay that against another instance of a load balance server.
Another problem is that the early data can not be authenticated until server validates the Client's finished message. This can cause issues for APIs, eg: don't act on early-data until after finished message checked.

There are also  Infrastructural barriers in upgrading TLS. There are existing middle-boxes and routers which only have TLS 1.2 capabilities, and there will break the protocol.
Because of this TLS 1.3 pretends to be 1.2 in various ways. ClientHello/ServerHello pretend to be TLS 1.2/1.0. Dummy change_cipher_spec have to be sent to make the handshake look more like TLS 1.2. The new HelloRetryRequest has to be disguised as a ServerHello. (Certain values distinguish HelloRetryRequest).
Deployments have shown 5-10% of TLS 1.3 sessions fail.

**c. TLS 1.2**

**1. CRIME (Compression Ration Info-leak Easy)

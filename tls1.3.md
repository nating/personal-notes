
# Q2a)

* TLS1.3's primary goal is to provide a secure channel between two communicating peers.

* TLS1.3's only requirement from the underlying transport is a reliable, in-order data stream.

* TLS provides:

  * **Confidentiality**: Data sent over the channel after establishment is only visible to endpoints.
  * **Integrity**: Data sent over the channel after establishment cannot be modified by attackers without detection.
  * **Authentication**: The server side of the channel is always authenticated; the client side is optionally authenticated.

* The two primary components of TLS1.3 are the **Handshake Protocol**, and the **Record Protocol**.

* The **Handshake Protocol** authenticates the communicating parties, negotiates cryptographic modes & parameters, and establishes shared keying material.

* The **Record Protocol** uses the parameters established in the handshake protocol to protect traffic between the communicating peers. The record protocol divides traffic up into a series of records, each of which is independently protected using the traffic keys. The record protocol in TLS1.3 uses exclusively AEAD ciphers. AEAD functions provide a unified encryption and authentication operation which turns plaintext into authenticated ciphertext and back again. All encrypted TLS records can be padded to inflate the size of the TLSCiphertext. This allows the sender to hide the size of the traffic from an observer.

* The handshake can be thought of as having three phases; Key Exchange, Server Parameters, and Authentication.

In the diagram below, you can see basic full TLS handshake:

```
       Client                                           Server

Key  ^ ClientHello
Exch | + key_share*
     | + signature_algorithms*
     | + psk_key_exchange_modes*
     v + pre_shared_key*       -------->
                                                  ServerHello  ^ Key
                                                 + key_share*  | Exch
                                            + pre_shared_key*  v
                                        {EncryptedExtensions}  ^  Server
                                        {CertificateRequest*}  v  Params
                                               {Certificate*}  ^
                                         {CertificateVerify*}  | Auth
                                                   {Finished}  v
                               <--------  [Application Data*]
     ^ {Certificate*}
Auth | {CertificateVerify*}
     v {Finished}              -------->
       [Application Data]      <------->  [Application Data]


       +  Indicates noteworthy extensions sent in the
          previously noted message.

       *  Indicates optional or situation-dependent
          messages/extensions that are not always sent.

       {} Indicates messages protected using keys
          derived from a [sender]_handshake_traffic_secret.

       [] Indicates messages protected using keys
          derived from [sender]_application_traffic_secret_N.
```

### Extra things to note:

#### Incorrect DHE Share

If the client has not provided a sufficient "key_share" extension, the server sends a HelloRetryRequest and the client needs to restart the handshake with an appropriate "key_share" extension.

#### Resumption and Pre-Shared Key (PSK)

PSKs can be established in previous connections and then be used again to establish a new connection. If the server accepts the PSK, it can be used with Diffie-Hellman in order to provide forward secrecy.

#### 0-RTT Data

When clients and servers share a PSK (either obtained externally or via a previous handshake), TLS 1.3 allows clients to send data on the first flight ("early data"). This data is not forward secret, and there are no guarantees of non-replay between connections.

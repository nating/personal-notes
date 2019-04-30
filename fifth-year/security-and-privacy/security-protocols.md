
*https://github.com/nating/personal-notes/blob/master/fifth-year/security-and-privacy/history-and-issues.md*

# Standard Security Structures & Protocols

* Knowing one of the following in detail is enough for exam purposes:
    * SMIME formats and secure email
    * TLS protocol (TLS1.2 or TLS1.3)
    * IPsec
    * Kerberos

* **PKI** stands for Public Key Infrastructure.

* **CA** stands for Certification Authority.

* PKI is about trusting CAs to bind public keys to names.

* There has been many suggestions to replace PKI but none have been sufficiently better to adopt.

* PKI is still the technology of choice for scalable key management.

## S/MIME

* **S/MIME** stands for Secure/Multipurpose Internet Mail Extensions.

* **CMS** can stand for Cryptographic Message Syntax.

* CMS defines how to sign and encrypt data.

* S/MIME is a combination of CMS, message specification and certificate specification.

* CMS message specification is to begin with a MIME message, treat the message "as like plaintext the CMS way", then take the resulting bytes and make them into a MIME message.

* **PGP** stands for Pretty Good Privacy.

* PGP does everything that S/MIME does.

* **MUA** stands for Mail User Agent.

* Most MUAs support S/MIME or PGP.

## TLS

* **TLS** stands for Transport Layer Security.

* **SSL** stand for Secure Sockets Layer.

* SSL is a general purpose network security protocol.

* SSL was designed to work with any application that uses sockets to communicate.

* SSL was standardised as TLS.

* The latest specification of TLS is TLS1.3 ([RFC 8446](https://tools.ietf.org/html/rfc8446)).

* TLS1.2 ([RFC 5246](https://tools.ietf.org/html/rfc5246)) is widely deployed.

* The original services of SSL were:

  * **Server Authentication** so that buyers could tell they were really dealing with the real merchants.

  * **Message Encryption** so that credit card details could be sent without fear of interception, and for message integrity.

* "**TLS** is broken down into four interrelated sub-protocols" (Stephen does not mention what he thinks these four are).

*


* [This](https://www.youtube.com/watch?v=VzWqnT5dErI) is really good for TLS1.3


* The "Bleichenbacher" or "Million Message" attack tries sending messages with different padding lengths to a server. If the server responds with the fact that the padding length was correct or not, it gives out information about the random integers used in generating the secret. This means that by carefully selecting values used in generating messages, an attacker can figure out the master secret for the encryption. This attack can be performed against PKCS#1 v1.5.

* [This](https://security.stackexchange.com/questions/46802/what-is-the-difference-between-dhe-and-ecdh) is very good for PFS, DH & ECDH.

















/

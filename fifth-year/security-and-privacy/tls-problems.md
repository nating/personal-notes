

# TLS Problems

* At the very beginning, there were only 47 bits of entropy instead of 128, which meant that the pre-master secret could be guessed. The solution was to add more entropy.

* CAs can screw up. e.g. VeriSign issued code-signing certs to someone who claimed to be a Microsoft employee. The solution was to revoke the certificate. Another example is someone hacking into a CA and issuing a load of certificates.

* Bleichenbacher could exploit how servers responds to invalid padding in handshake messages to guess the pre-master secret, allowing the entire conversation to be decrypted. The solution is to not reveal whether the padding is correct or not.

* There are so many embedded devices that generate keys before they have any real entropy on first boot. The solution to this is to have "more entropy (somehow ;-)".

*



## TLS1.3

* The slides are not a replacement for reading the spec

* Major Changes:
  * Drop less desirable algorithms and move to AEAD everywhere
  * Change how new ciphersuites get defined and get RECOMMENDED
  * Added “0-RTT” mode, a double-edged sword! (aka sharp implement)
  * RSA key transport removed, all key exchanges provide forward secrecy
  * More encryption of handshake including some extensions
  * ECC is now built-in
  * No more compression or custom DH groups
  * Pre-shared keying, tickets and session handling all done in one way
  * PKCS#1v1.5 -> RSA PSS for protocol signatures (but not certificates)
  * Versioning muck – need to pretend to not be TLSv1.3 for deployment in the real world of middleboxes

* Features:
  * 1-RTT handshake
  * HRR
  * PSK/Resumption
  * 0-RTT
  * Ciphersuite re-factoring
  * Key Derivation
  * Versioning muck
  * (Notable) extensions
  * Record Protocol
  * Security Properties


---

## 1a

#### Identification

For each component of the system, as many risks as possible would need to be
identified.

#### Classification

Once as many risks as possible have been identified, the risks would
be classified in terms of:
  * The impact they would have on the company
  * The likelihood of them occurring

The risks' impact and likelihood would be given values to from low to high
to normalise the importance of mitigating each risk. These values would be used
to order the risks by their importance.

#### Mitigation

After the risks have been ordered by importance, a mitigation is designed for
the most important risk on the list.

#### Iteration

As each risk is mitigated (or as necessary), the list is re-analysed to assess
the proper order for the remaining risks. This is because the mitigation for
one risk could effect the probability of other risks or may introduce new risks.

#### Termination

In practice, the process is terminated once available effort is expended. Time
and money may mean that mitigations may not be designed for every possible risk.

---

## 1b

*The main thing here is to describe risks with their impact and an estimate of probability of occurrence and to concentrate on the more significant of those.*

*Make sure to link all risks with specifics of the paragraph you are being questioned about.*

#### Risks

* Spam
* Phishing
* Malware
* Availability (e.g. DOS resiliance)
* MUAs that render active content
* Abuse of content if 3rd parties used
* Spear Phishing
* Database Leak (e.g. customer database)
* Outsourcers SecPriv quality must at least match theirs
* Hackers defacing site
* 3rd Party Staff abusing content from within
* Employees working for competitors from within
* Pervasive Monitoring
* Cloud-providers monitoring site traffic and data for their own benefit or for the benefit of competitors or governments
* Stolen / Lost laptop
* Any of the above but from a third party

#### What might go wrong

* Bad DB Salting
* Breach PCI requirements
* SQL Injection Vulnerabilities
* XSS
* CSRF
* Non-updated Technology (e.g. outdated wordpress)


---

## 2a

* TLS1.3's primary goal is to provide a secure channel between two communicating peers.

* TLS1.3's only requirement from the underlying transport is a reliable, in-order data stream.

* TLS provides:

  * **Confidentiality**: Data sent over the channel after establishment is only visible to endpoints.
  * **Integrity**: Data sent over the channel after establishment cannot be modified by attackers without detection.
  * **Authentication**: The server side of the channel is always authenticated; the client side is optionally authenticated.

* The two primary components of TLS1.3 are the **Handshake Protocol**, and the **Record Protocol**.

* The **Handshake Protocol** authenticates the communicating parties, negotiates cryptographic modes & parameters, and establishes shared keying material.

* The **Record Protocol** uses the parameters established in the handshake protocol to protect traffic between the communicating peers. The record protocol divides traffic up into a series of records, each of which is independently protected using the traffic keys.

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
```

* The handshake can be thought of as having three phases; Key Exchange, Server Parameters, and Authentication.

### Extra things to note:

#### Incorrect DHE Share

If the client has not provided a sufficient "key_share" extension, the server sends a HelloRetryRequest and the client needs to restart the handshake with an appropriate "key_share" extension.

#### Resumption and Pre-Shared Key (PSK)

PSKs can be established in previous connections and then be used again to establish a new connection. If the server accepts the PSK, it can be used with Diffie-Hellman in order to provide forward secrecy.

#### 0-RTT Data

When clients and servers share a PSK (either obtained externally or via a previous handshake), TLS 1.3 allows clients to send data on the first flight ("early data"). This data is not forward secret, and there are no guarantees of non-replay between connections.

---

## 2b)

---

## 2c)

Known attacks:
  * Lack of a good PRNG for elements of the ClientHello and ServerHello means that an attacker would be able to predict the keying material.
  *

---

## 3a

* Use HTTPS everywhere
* Use HSTS
* Use TLS1.3



---

# Appendix

|||
|---|---|
|Risk|Spam|
|How it occurs|Spammers send mass emails in order to get as many people as possible to interact with their schemes.|
|Impact|Low|
|Likelihood|High|
|Justification for values|Spam is everywhere and it takes very little effort for spammers to attempt to send an extra emails. The potential return on investment sending an extra extra emails is very high.|
|Recommendation|Strengthen anti-spam email filters.|

|||
|---|---|
|Risk|Phishing|
|How it occurs|Employees share their information unknowingly to malicious actors through email.|
|Impact|High|
|Likelihood|High|
|Justification for values|Impact is high as it could compromise the entire network, once malicious actors have the required information from an employee, they may have access to lots of private company information. Likelihood is high as it is a medium sized business with about a thousand employees (a lot). A manufacturing company is also a good target for phishing attacks, as it may have private information about products from other companies who avail of their services. This makes them a target for competitors of each company that is a client of theirs.|
|Recommendation|Educate employees, conduct training sessions, have personnel that employees can contact if they are suspicious of an email. Require 2FA so that stolen information from successful phishing attempts will be of no use without the second authentication device. Restrict each employee's access in the system to only the parts of the system that they are required to have access to, this means that successful phishing attempts will get access to less of the system. Restrict access to networks with a VPN, with 2FA on the VPN as well, so that malicious actors must be on the network to even use credentials they may have stolen.|

|||
|---|---|
|Risk|Lack of availability|
|How it occurs|A security measure often worth taking is to only allow access to the system from the company network. If this is the case, it could mean that the dozens of frequently travelling employees may not have vital access they need.|
|Impact|High|
|Likelihood|High|
|Justification for values|It is very likely that travelling employees will need access to information or process on the company system when working. For this reason, the impact of them not being able to access the system is high. The likelihood is very high as there are so many employees frequently travelling. This risk generally occurs as a result of previous security measures (limiting access to the company network).|
|Recommendation|Make sure the proper infrastructure is in place for employees to easily connect to the company network from anywhere through the use of a VPN. Preferably using 2FA to connect to the VPN.|

|||
|---|---|
|Risk|MUAs that render active content|
|How it occurs|MUAs can make network calls or run malicious code when opening emails, if they are not configured properly.|
|Impact|High|
|Likelihood|Medium|
|Justification for values| Impact is high, as  Likelihood is medium, as most MUAs will not support the running of malicious code in emails, but it is extremely likely that emails will contain tracking pixels that will cause the MUA to leak information about the interactions employees have with the email.|
|Recommendation|Educate employees about the risks. Enforce that employees use particular MUAs with specific set ups.|


































/

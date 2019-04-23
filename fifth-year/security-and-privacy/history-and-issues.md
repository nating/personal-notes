
*https://github.com/nating/personal-notes/blob/master/fifth-year/security-and-privacy/history-and-issues.md*

# History and Issues

"Privacy is the real next challenge"

* It was a basic law enforcement requirement that all telephone lines needed to be [tappable](https://en.wikipedia.org/wiki/Telephone_tapping).

* **RSH** stands for Remote Shell.

* **SSH** stands for Secure Shell.

### The Morris Worm

* The first widespread worm was the **"Morris worm"** in 1988.

* The Morris worm was launched from MIT with the purpose of gauging the size of the Internet.

* The Morris worm effected 10% of the Internet and regional networks had to disconnected from the Internet backbone to contain it.

* The Morris worm made use of several different vulnerabilities:

  * **fingerd** updates a server with a client's information. If the username supplied was more than 512 bytes, unforseen memory was written to. This is called a **Buffer Overflow Vulnerability**. This could be exploited to perform malicious code on the server.
  * Two operations were put in the oveerflowing bytes from the username to get the host machine to open up a shell attached to a socket. Commands could be sent to the socket to be executed on the victim machine.
  * Morris sends itself to the victim machine and then sends a command to execute itself on the victim machine.
  * The Morris worm used a dictionary attack: NULL, <the username>, <theusername><theusername>, <theusernamebackwards>, <theextrainfofromtheuserfile(likenickname)>, 432 other words, and then the unix dictionary.
  * The Morris worm used passwords to use rsh and rexec to execute itself on more systems.

---

* **DNS** (Domain Name System) was invented in 1983.

*




/

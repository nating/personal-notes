
*(https://github.com/nating/personal-notes/blob/master/fifth-year/security-and-privacy/question-compilation.md)*

# Security & Privacy Question Compilation

*This is a compilation of all the questions asked in Security and Privacy exams from 2008-2018 inclusive.**

## Q1 - Risk Analysis

**These questions are all preceded by paragraphs of text describing a company's system which needs to have its risks analysed. The paragraphs that these questions refer to can be found here:**

* [2018](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2018-exam.pdf#page=2)
* [2017](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2017-exam.pdf#page=2)
* [2016](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2016-exam.pdf#page=2)
* [2015](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2015-exam.pdf#page=2)
* [2014](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2014-exam.pdf#page=2)
* [2013](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2013-exam.pdf#page=2)
* [2012](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2012-exam.pdf#page=2)
* [2010](https://down.dsg.cs.tcd.ie/old-exams/cs7053-questions-2010.pdf)


#### Q1a)

Describe the risk analysis process you would follow in order to assist the company. **[10 marks]** (2018, 2017)

#### Q1b)

Describe the most relevant risks (at least 3) you see for the new system, including their potential impact and likelihood of occurrence, and outline the countermeasures you would recommend that the company and/or their chosen service providers (who provide outsourced functions) ought to implement to mitigate those risks. Risks that could emerge during migration from the old to the new system are in scope here. **[25 marks]** (2018, 2017, 2016, 2015, 2014, 2013, 2012, 2010)

#### Q1c)

List and justify the 5 most important high-level security requirements that you would
expect the system to meet. **[5 marks]** (2010)

#### Q1d)

Assume the company had instead gone ahead and deployed a new system without having done any risk analysis. Describe some mistakes, not covered in part (b), that they might have made? **[5 marks]** (2018, 2017)

#### Q1e)

What questions should the company ask the out-sourced service providers about their systems and operational practices? **[10 marks]** (2016, 2015, 2014)

#### Q1f)

What questions would you ask about the company's internal development processes and the operational processes of the hosting data centres? **[10 marks]** (2013)

#### Q1g)

What functions would you recommend that the company should not outsource and why? **[5 marks]** (2016)

#### Q1h)

What countermeasures would you put in place to detect or prevent a dishonest "developer employee / dishonest member of sales" (**Note to student reader: this question can be about either**) from misbehaving? **[5 marks]** (2015, 2014)

#### Q1i)

After you've finished this contract, another similar, competing company hires you to do a very similar piece of work. How might you expose confidential information related to the first company in carrying out this second contract? Describe steps you would take to avoid exposing such confidential information. **[7 marks]** (2013)

#### Q1j)

How and when should the company re-evaluate the security of their site after it has gone live? **[5 marks]** (2012)

#### Q1 k)

How would you, as a security professional, handle the situation where you suspect that the startup intends to lie to their major customer about some significant security issue? **[5 marks]** (2010)


---

## Q2 - Internet Key Exchange Protocol

#### Q2a)

For any real Internet key exchange protocol (e.g. TLS, S/MIME, IPsec, Kerberos) describe the key management and application data protection aspects of the protocol in detail. Your answer may describe any widely used version of your chosen protocol, but you need to state which version you are describing. Choosing TLSv1.3 is allowed – you don’t need to specify the exact Internet-draft version you’ve chosen in that case. **[20 marks]** (**Note to student reader: this question is always accompanied with a specific extra bit, as shown below:**)

Include a description of how networking failures, (e.g. packet drops, re-ordering), might affect use of your chosen protocol. (2018)

How would you test the security of a deployed application that uses that protocol? (2017)

How would you test a library implementation of the protocol before using it in some application. (2016)

Include a description of how you would test which protocol features have been deployed in the wild. (2015)

Include a description of how you would test interoperability between a new and an existing implementation of your chosen protocol. (2014)

Include a description of the impact of the exposure of relevant secret or private keys. (2013)

Include a description of how that security protocol is used by some real application. (2012)

Include a description of the relevant configuration settings that an implementation would require. (2011)

#### Q2b)

Outline the ways in which the security of your chosen protocol depends on other infrastructure such as the Internet routing system, the domain name system or a key management infrastructure. **[10 marks]** (2018)

#### Q2c)

State-level adversaries have different capabilities and interests when compared to potential industrial or commercial adversaries. Describe three ways in which the threat-model for an implementation or deployment of your chosen protocol would differ, when considering state-level versus industrial or commercial adversaries. **[10 marks]** (2018)

#### Q2d)

What are the main barriers to upgrading (**or to deployment using (2016, 2015)**) your chosen protocol (**on a very large scale (2013)**)? For example, if your chosen protocol is TLS, you might describe barriers to deployment of TLS1.3. **[10 marks]** (2017, 2016, 2015, 2013)

#### Q2e)

Describe two or three known attacks on implementations of your chosen protocol with an emphasis on explaining their significance for the Internet. **[10 marks]** (2017, 2016)

#### Q2f

Describe and justify how you think your chosen protocol might evolve in the coming decade. **[8 marks]** (2015, 2014)

#### Q2g

What are the main security failures that are likely to arise in implementations of your chosen protocol? **[10 marks]** (2014)

#### Q2h)

Describe any side-channel (e.g. timing, power) attacks might be attempted against a naïve implementation of your chosen protocol? **[8 marks]** (2013, 2012)

#### Q2i)

What are the main potential Denial-of-Service (DoS) attack vectors that are created via the use of your chosen protocol? Describe those and potential countermeasures. **[10 marks]** (2012)

#### Q2j)

For your selected protocol, describe the main issues that would arise were it to be used in a large distributed network with some “normal” nodes but mostly consisting of many (i.e., millions), very small devices (e.g. motes) with limited processing power and memory and disrupted network connectivity. An example of such a network might be a country-wide seismic monitoring system but you can use any other example if that helps. **[10 marks]** (2011)

#### Q2k)

Describe two changes you would recommend for your selected protocol that would mitigate some of the issues you identified in **Q2j**. Be specific as to whether you consider each recommended change in something that could immediately be used, or whether your recommendation would be to experiment with the relevant change. **[8 marks]** (2011)

#### Q2l)

Discuss, in detail, the performance implications of your chosen protocol, both for clients and servers (or senders and recipients) covering a range of platforms and a range of scaling factors. **[10 marks]** (2010)

#### Q2m)

Describe a way to modify the protocol, without seriously compromising security, that would result in improved performance in one of the situations you described in **Q2l** above. **[5 marks]** (2010)

#### Q2n)

For the application you chose above, say how five errors can occur in the cryptographic mechanism that affect the user interface of the application? For each error considered, say how you think it should (as opposed to is currently) be presented to the user. **[10 marks]** (2009)

#### Q2o)

User testing indicates that many security error handling user interfaces merely trains users to click “ok” without thinking. Why is that and what would you do about it? **[10 marks]** (2009)

#### Q2p)

For your selected protocol, where and how should it be used by a company selling tangible goods (e.g. books, hardware) over the web? Include a network diagram, and consider that the overall system must scale so as to handle millions of users. **[10 marks]** (2008)

#### Q2q)

What are the three most likely (note: most likely, not most impactful) threats related to the selected protocol that remain in the setup described in **Q2p**? **[5 marks]** (2008)

---

## Q3 - Design a System

**These questions are all preceded by paragraphs of text describing a system which needs to be designed. The paragraphs that these questions refer to can be found here:**

* [2018](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2018-exam.pdf#page=4)
* [2017](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2017-exam.pdf#page=3)
* [2016](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2016-exam.pdf#page=3)
* [2015](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2015-exam.pdf#page=3)
* [2014](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2014-exam.pdf#page=3&zoom=0,0,500)
* [2013](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2013-exam.pdf#page=3&zoom=0,0,500)
* [2012](https://down.dsg.cs.tcd.ie/old-exams/cs7053-2012-exam.pdf#page=3&zoom=0,0,630)
* [2011](https://down.dsg.cs.tcd.ie/old-exams/cs7053-questions-2011.pdf#page=3&zoom=0,0,500)
* [2010](https://down.dsg.cs.tcd.ie/old-exams/cs7053-questions-2010.pdf#page=3)
* [2009](https://down.dsg.cs.tcd.ie/old-exams/cs7012-exam.pdf#page=2&zoom=0,0,500)
* [2008](https://down.dsg.cs.tcd.ie/old-exams/nds106-2008-exam.pdf#page=2&zoom=0,0,650)

#### Q3a)

Outline your overall design for such a system (include a network diagram and describe how scheduling is handled), and state the security and privacy requirements the system must meet. **[15 marks]** (2018, 2017, 2016, 2015, 2014, 2013, 2012, ~2011, ~2010, ~2009)

#### Q3b)

Describe, in detail, the security solution you would propose to meet those requirements. **[20 marks]** (2018, 2017, 2016, 2015, 2014, 2013, 2012, ~2010)

#### Q3c)

How would you handle evaluating the security and privacy aspects of the system, before, during and after the planned exercise? **[5 marks]** (2018)

#### Q3d)

Describe a non-obvious way in which an adversary (**or employee/contractor (2016)**) might attempt to breach the system to their benefit. **[10 marks]** (2017, 2016)

#### Q3e)

Describe a non-obvious way in which you (as a system developer) might leave in place some feature that benefits you financially and that is hard to detect. **[8 marks]** (2015)

#### Q3f)

Having designed the system and being a user of the social network in question, you want to know if you are ever the target for such surveillance. Describe ways in which you might leave in place some form of covert channel so that only you would know if you were being targeted but so nobody else would realise that. **[8 marks]** (2014)

#### Q3g)

Having designed the system, you are then fired and decide to launch a denial-of-service attack that prevents the system working, but so that you could not be traced as the bad-actor. How would you go about doing this? **[8 marks]** (2013)

#### Q3h)

Researchers are competitive too. Describe the various ways in which you, as a dishonest highly-competitive researcher, would attempt to abuse or game the system so as to make use of others work for your own benefit. **[8 marks]** (2012)


#### Q3i)

List and justify the 5 most important high-level security requirements that you would expect the system to meet. **[5 marks]** (2010, 2009)

#### Q3j)

How would you convince a third party (say a local parliament or Government committee) that the outputs from the system are trustworthy? **[5 marks]** (2010)

#### Q3k)

How might law enforcement officials abuse this system? How might you detect and react to such abuse? **[5 marks]** (2009)

#### Q3l)

It turns out that you are dishonest and, after the system has been running for a few years, you are paid a large sum of money by one FI so they can avoid or subvert the system. How would you set about doing this for them? **[5 marks]** (2010)

#### Q3m)

You are an IMF system administrator based at IMF headquarters who is a citizen of a country being visited by an IMF negotiation team. Your government pay you to break into the system described above, in order to get information as to the negotiation position of the visiting IMF team. How would you go about that? **[8 marks]** (2011)

---

## Q4 - DNSSEC

#### Q4a)

Describe the architecture and key management hierarchy of DNSSEC. **[20 marks]** (2017, 2016, 2015, 2014)

#### Q4b)

Give some examples of how the DNS leaks private information? How can we mitigate that via changes to policies, protocols, implementations and deployments? **[10 marks]** (2017, 2016, 2015, 2014)

#### Q4c)

Why is DNSSEC hard to deploy? Suggest some changes to the protocol or overall DNS ecosystem that would make DNSSEC easier to deploy. **[10 marks]** (2017)

#### Q4d)

Why is DNSSEC less likely to be deployed, compared to DKIM? **[8 marks]** (2016)

#### Q4e)

How will DNSSEC deployment impact on registrars, registries and applications? **[8 marks]** (2015, 2014)

---

## Q5 - Security Review Process (2011 Q1)

You are a senior software developer in a large software company tasked to produce a security review process for a new product development group that has just been established. The group will be developing web services based applications for the healthcare market, including handling of sensitive (patient) data. The security review process will be followed by designers and developers. You cannot expect that all people in the group will be familiar with security, and they will be constant under time-pressure to produce product deliverables. For the purposes of the answer, you can assume whatever general software development methodology you like is to be used.

#5a)

Outline the security review process you would initially suggest, and how it fits with the general software development methodology you select. **[15 marks]**

#5b)

How would you get from your initial suggestion for a process to a final, signed-off security process to be followed by the group? Describe the actions you would take and the interactions with others you would expect to occur before you get that final sign-off. **[10 marks]**

#5c)

How would the security process be maintained over time in order to handle changes to the group's activities, the legal and the business environment? **[8 marks]**

---

## Q6 - End-to-End (2018 Q4)

#### Q6a)

Describe three significant security and privacy differences between real-world end-to-end and hop-by-hop security mechanisms as used for interpersonal messaging, in email and/or instant messaging systems. **[15 marks]**

#### Q6b)

Describe three significant barriers to the deployment of Internet-scale end-to-end email security mechanisms such as S/MIME or PGP. In each case, describe realistic actions you would recommend that aim to at least partially overcome those barriers. **[15 marks]**

#### Q6c)

If end-to-end email confidentiality became the norm, so that most email messages were encrypted between sender and recipient(s), what problems would that cause for email system administrators, and how would you recommend they address those issues? **[10 marks]**

---

## Q7 - DMZ (2013 Q4)

#### Q7a)

Describe the concept of a de-militarized zone (DMZ) and how that is used in typical enterprise networks. Describe three security technologies that one can reasonably place in a DMZ? For each, describe some threats that that technology mitigates and how that is achieved. **[18 marks]**

#### Q7b)

Describe a realistic network that uses the technologies, described in part A and say what kinds of penetration testing you would attempt in order to determine if the network is sufficiently secure. (The meaning of “sufficiently secure” will depend on the kind of network you describe.) **[10 marks]**

#### Q7c)

Describe common mis-configurations of one of the technologies that you described in part A and the kinds of exploit that such mis-configuration enables. **[7 marks]**

---

## Q8 - DKIM (2011 Q4)

#### Q8a)

Describe in detail the Domain Keys Identified Mail (DKIM) mechanism for associating an authenticated domain identifier with email messages. **[15 marks]**

#### Q8b)

Describe the role that DKIM can play in countering phishing and SPAM and explicitly describe what DKIM does not provide in terms of countering phishing and SPAM. **[8 marks]**

#### Q8c)

Briefly describe two other commonly used mechanisms that aim to mitigate problems caused by phishing attacks distributed via email. **[5 marks]**

#### Q8d)

You are a spammer. Describe two ways in which you would you attempt to get your SPAM delivered to users in systems that have deployed DKIM signature verification and the other mechanisms you described in part (c)? **[5 marks]**

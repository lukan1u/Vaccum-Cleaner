---
Date: 2023-10-03T12:45:00
Summary: To understand what digital forensics is. What crime is. Most important part is the forensics principles
---
# Crime
---
#digital-forensics  #uwe #year1
Table of contents >>>  [[0.Digital Forensics]]
Previous page >>> [[1.Induction]]
Next Page >>> [[Computer Crime - week 8]]

## What is Digital forensics
---
- **Digital forensics** - is the applications of science to law and is ultimately tested by use in court. The systematic study of digital data becomes a forensic discipline when it relates to the investigation and prosecution of a crime. Post incident analysis relates to digital forensics.
- **Forensic** we mean a characteristic of evidence that satisfied its suitability for admission as fact and its ability to persuade based upon proof (or high statistical confidence). Major decision are based on evidence.
- **Forensic Science** is the application of science to law and is ultimately tested by use in court
	- The systematic study of digital data becomes a forensic discipline when **it relates to the investigation** and prosecution of a crime

- **Digital Forensics Science** (full definition) - The use of **scientifically derived and proven methods** toward the  preservation, collection, validation, identification, analysis,  interpretation, documentation and presentation of digital evidence  derived from digital sources for the purpose of facilitating or  furthering the reconstruction of events found to be criminal, or  helping to anticipate unauthorized actions shown to be disruptive to  planned operations.

#### Crime breakdown
1. **Object of a crime** (stolen/destroyed)
2. **Subject of crime** (computer infected by malware)
3. **Tool for conduction** or planning a crime
4. **Symbol** to create false impression (especially in the financial sector)

---
## Principles of digital forensics

- Forensic Science is a field of study that involves the application of scientific methods to investigate legal cases. It provides a wide range of investigative techniques and methods that have been proven to achieve reliable results. Forensic evidence is characterized by its suitability for admission as fact and its ability to persuade based upon proof or high statistical confidence.
- Decisions are based on **solid evidence** and "Certainty" should be **used with extra care** as we cannot always proof of what actually has happened.

#### Evidence exchange
- Aim of investigation is to **follow trails** that offenders leave and **tie perpetrators** to the victim and crime scenes.
- Any contact between two items *(subjects)* will result in exchange:
	- Offender - victim, person - weapon, people - crime scene
- There will always be **evidence of interaction** however absence itself is not the evidence of absence.
- Just like in the real world **same rules apply to physical and digital** world such as fingerprints on victim's keyboard could  be a possible proof of murder.
![[Pasted image 20231003131437.png]]

#### Evidence attributes/charactiristics
The evidence can also be identified in two ways
- **Class characteristics** - common traits in similar items such as document encryption (Microsoft word version)
- **Individual characteristics** - unique traits such as printer's ability to mark every page with easily identifiable code used to prevent money printing.

#### Forensic soundness
All evidence must be preserved and examined in a forensically sound manner. That being said any forensic activity on original device can alter its state. Therefore the need for **documentation** is important. **Documentation** should include:
- Where the evidence originated and how it was handled 
- The acquisition process should change the original evidence as little as possible
- Any changes should be documented and assessed
- Document date and time data were preserved and tools used
- MD5 has values of all outputs

#### Authentication
- The process of ensuring that the recovered evidence is the same as the originally seized data
- **Use of hashes**
- The individual who collected the evidence can confirm that the evidence presented in the court is the same as when it was collected
- Sys admin can testify that log files presented in court originated from his/her system

#### Chain of custody
- Continuity of possession
- Each person that handled the evidence needs to be noted down keeping a chain of custody

#### Evidence Integrity
- To show that evidence has not been altered since it was collected
- Supports the authentication phase
- Comparison of the evidence fingerprint (hash value ) at the time of collection with the fingerprint of the evidence in its current state.
![[Pasted image 20231115225818.png]]

- Hash value are represented in hexadecimal 128bit value
- There number of possible values for one hash value is 2^128 therefore a 2 files with the same hash value have the same content. Also the process cannot be reversed.

#### Objectivity
- Evidence should be free from bias
- Always provide clearest possible view of facts
- Conclusions have to be supported by factual evidence

#### Repeatability
- Other forensic analysts should be able to follow the same process and get the same result.
- Any experiments or observations must be **repeatable in order to be independently verified.**
-  All steps should be documented so others can follow instructions and verify evidence independently.



---
## Examples of computer crime:
- **Terrorist** are using internet to communicate recruit launder money commit credit card theft post propaganda and training materials.
- **Cyber-terrorism**
- **Cyber-attacks** against critical infrastructure such as government power health communications financial and emergency and response what it called 
- **Cyberbullying** such as harassing, texting with the intent to threaten, trolling.
- **eCrime** traditional methods of committing a crime over the internet/computers. It could include publishing illegal content, economic crimes, accessing intellectual property etc.

---
## Digital evidence 
**Digital evidence** is defined as any data stored or transferred using a computer that support and refute a theory of how an offence occurred or that address critical elements of the offence such a intent or alibi. *All digital evidence have same rules and laws as documentary evidence*.
There are *3 categories* for digital evidence:
- **Open computer systems**  - (hard drives laptops, desktops)
- **Communications systems**  - (traditional telephone systems wireless communications system SMS messages)
- **Embedded computer systems**  - mobile devices, smart cards, activity trackers wearable watches.
- 

----

### Digital Forensics scope
1. **Computer forensics** - preservation and analysis of computers also called file sytem forensics
2. **Network forensics** - preservation and analysis of traffic and logs from networks
3. **Mobile device forensics** - preservation and analysis of cell phones and smart phones and satellite navigation
4. **Malware forensics** - preservation and analysis of malicious code such as viruses worms anf trojan horse programs
5. **Cloud forensics**




#### Links
https://ecrimeresearch.org/ - eCrimes
# Phishing Analysis Lab

## Objective
I completed the [The Planet's Prestige](https://blueteamlabs.online/home/challenge/the-planets-prestige-e5beb8e545) Phishing Lab on the platform Blue Team Labs Online. Below is some context behind the lab.

"After the meeting concluded the President was informed his daughter had disappeared. CoCanDa agents spread across multiple planets were working day and night to locate her. Two days later and there’s no update on the situation, no demand for ransom, not even a single clue regarding the whereabouts of the missing people. On the third day a CoCanDa representative, an Army Major on Earth, received an email."

The Objective is to anaylsis the email and it's attachments in order to reveal what the attackers want in return for the Presidents Daughter. 

### Skills Learned

- Using the first 4 bytes of a file in hex to indentify the file type.
- Development of critical thinking and problem-solving skills in cybersecurity.
- What fields to look at when analysing an email for suspicious activity.

### Tools Used

- Cyber Chef to covert from Base64 to Hex.
- Linux command xxd to output files in Hex.
- Square X to open the attachment in a safe disposable file viewer.
- Metadata2go to view the meta data of the attachment Jpeg.

## Steps
#### Question and Answers
What is the email service used by the malicious actor?

 Email headers contain information about the source of the email, and where it has traveled in order to land in your inbox. It is important to note that some headers can be faked if an environment is set correctly. To view the email header information, The email can be opened in a text editor such as Notepad++. Line 28 shows that the email was sent from IP 93.99.104.210, with the sending domain.

Answer: emkei.cz



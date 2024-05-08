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
1) What is the email service used by the malicious actor?

 Email headers contain information about the source of the email, and where it has traveled in order to land in your inbox. It is important to note that some headers can be faked if an environment is set correctly. To view the email header information, The email can be opened in a text editor. Line 28 shows that the email was sent from IP 93.99.104.210, with the sending domain. When doing a google search for emkei.cz it says it is a fake mailer service which raises questions about the authenticity of the email

 ![image](https://github.com/oli-philbin/Phishing-Analysis/assets/150199616/1ce39e4a-0d9a-4b23-89e1-0279c73a7e63)

Answer: emkei.cz


2) What is the Reply-To email address?

The reply-to field shows where any response to this email will be sent to. The email address in this field is different to the from address which is suspicious and suggest malicious intent. This can be found on line 44 in a text editor, or by searching for the Reply-To field.

![image](https://github.com/oli-philbin/Phishing-Analysis/assets/150199616/525cfcd0-2570-4f07-95c7-199ec3288025)


Answer: negeja3921@phashter.com


3) What is the filetype of the received attachment which helped to continue the investigation?

It says the attachment is a pdf. When you use cyber chef to decode the below from base64 into hex the first 4 bytes of the hex tells you the file type. Using the website you can check which file type the bytes relate to, which is .zip.

![image](https://github.com/oli-philbin/Phishing-Analysis/assets/150199616/cd2421b5-72b8-4314-94ba-4856b2c64be8)


(https://www.garykessler.net/library/file_sigs.html)

![image](https://github.com/oli-philbin/Phishing-Analysis/assets/150199616/9c96ed25-519e-4bec-86e7-cef16ef52db8)


Answer: .zip


3) What is the name of the malicious actor?

By using exiftool, metadata about the PDF can be discovered, where other tools might only identify anticipated metadata fields based on the file type. One of the metadata fields includes the author of this document.

Answer: Pestero Negeja


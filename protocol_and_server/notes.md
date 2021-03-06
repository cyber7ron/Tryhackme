## telent

- application layer protocol
- used to connect virtual terminal of another computer.
- not encrypted
- A Telnet server uses the Telnet protocol to listen for incoming connections on port 23.
- not a secure option.

## http

- Hypertext Transfer Protocol
- transfer web pages.
- send and recieve data in clear text. (not encrypted)
- We need an HTTP server (webserver) and an HTTP client (web browser) to use the HTTP protocol. 

## ftp

- file transfer protocol
- transfer of files between different computers with different systems efficient.
- send and recieve data in clear text.

![img](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/da71a52fddfbb268dc6c5857daf07f18.png)

- For FTP clients, in addition to the console FTP client commonly found on Linux systems, you can use an FTP client with GUI such as FileZilla. Some web browsers also support FTP protocol.

## smtp

- simple mail transfer protocol
- we can set up different email set up and configuration eg : email system to allow local users to exchange emails with each other with no access to the Internet. 

Email delivery over the Internet requires the following components:


1. Mail Submission Agent (MSA)
2. Mail Transfer Agent (MTA)
3. Mail Delivery Agent (MDA)
4. Mail User Agent (MUA)

![img](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/822a449fd569c16c875a13ca2487b714.png)


1. A Mail User Agent (MUA), or simply an email client, has an email message to be sent. The MUA connects to a Mail Submission Agent (MSA) to send its message.
2. The MSA receives the message, checks for any errors before transferring it to the Mail Transfer Agent (MTA) server, commonly hosted on the same server.
3. The MTA will send the email message to the MTA of the recipient. The MTA can also function as a Mail Submission Agent (MSA).
4. A typical setup would have the MTA server also functioning as a Mail Delivery Agent (MDA).
5. The recipient will collect its email from the MDA using their email client.

- In the same way, we need to follow a protocol to communicate with an HTTP server, and we need to rely on email protocols to talk with an MTA and an MDA. for this we use

1. smtp
2. pop3

- smtp used to communicate with mta
- it uses clear text.
- listen on port 25 by default.

## pop

- used to download email from MDA.

![img](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/ed910ad418376edc846846fc2a0dd3f6.png)

- uses default port 110
- authentication is required.


## imap

- Internet Message Access Protocol.
- more sophisticated than POP3.
- IMAP makes it possible to keep your email synchronized across multiple devices (and mail clients). 
- uses port 143


## summary

|Protocol |	TCP Port |	Application(s)| 	Data Security|
|----------|---------|----------------|-------------------|
|FTP |	21 	|File Transfer |	Cleartext|
|HTTP |	80 |	Worldwide Web |	Cleartext|
|IMAP |	143 |	Email (MDA) |	Cleartext|
|POP3 |110 |	Email (MDA) |	Cleartext|
|SMTP |	25 |	Email (MTA) |	Cleartext|
|Telnet |	23 |	Remote Access |	Cleartext|
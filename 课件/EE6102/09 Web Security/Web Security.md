---
tags:
  - cyber_security
  - 奇葩PPT大赏
---

- Web is widely used by business, government and individuals. However, Internet & Web are vulnerable as it uses HTTP (Hyper Text Transfer) protocol.
  Web 被广泛用于商业、政府和个人。然而，互联网和 Web 存在漏洞，因为它使用的是 HTTP（超文本传输）协议

- HTTP IS NOT A SECURE PROTOCOL
	- It is a simple and stateless client/server application running over TCP/IP.
	  它是一种简单且无状态的客户端/服务器应用程序，运行在 TCP/IP 之上
- WHAT ARE THE THREATS
	- INTEGRITY
		- Data modification, insertion
		  数据修改、插入
	- CONFIDENTIALITY
		- Eavesdropping on the net
		  网络监听
		- Theft from server machine
		  从服务器机器上盗取数据
	- AUTHENTICATION
		- Impersonation, data forgery
		  冒充、数据伪造
	- DENIAL OF SERVICE
		- Hacked web servers
		  被入侵的 Web 服务器

# HTTP and HTTPS

- HTTP is an application-layer protocol used for communication between clients (browsers) and web servers.
  HTTP 是一种应用层协议，用于客户端（浏览器）与 Web 服务器之间的通信
- It follows a request-response model, where a client sends a request, and the server returns a response.
  它遵循请求-响应模型，客户端发送请求，服务器返回响应
- **Stateless Protocol**: Each request is independent, meaning no session is maintained unless managed separately (e.g., using cookies).
  **无状态协议**：每个请求都是独立的，意味着不会维护会话，除非通过其他方式单独管理（如使用 Cookies）
- HTTP Methods
	- GET: Retrieve data.
	- POST: Send data (e.g., form submissions).
	- PUT: Update data.
	- DELETE: Remove data.
	- HEAD: Retrieve headers only.
- HTTPS (HTTP Secure)
	- It is an extension of the Hypertext Text Transfer Protocol for secure communication. Encrypted by TLS/SSL
	  是超文本传输协议的扩展版本，用于安全通信。通过 TLS/SSL 加密

- HTTPS is HTTP + TLS, ensuring data confidentiality, integrity, and authentication.
  **HTTPS 是 HTTP + TLS**，可确保数据的机密性、完整性和身份验证
- HTTP protocol uses port number 80 and provides no security as it doesn’t use any encryption.
  HTTP 协议使用端口号 **80**，不提供任何安全性，因为它不使用加密
- HTTPS protocol uses port number 443 and is Secure as it uses encryption.
  HTTPS 协议使用端口号 **443**，更加安全，因为它使用了加密技术

| Feature        | HTTP                            | HTTPS                           |
| :------------: | :-----------------------------: | :-----------------------------: |
| Security       | Unencrypted                     | Encrypted (TLS/SSL)             |
| Authentication | No authentication               | Server identity verified        |
| Data Integrity | Data can be modified            | Data cannot be altered          |
| Performance    | Faster (no encryption overhead) | Slightly slower (TLS handshake) |

# SSL/TLS

- Have you done any of the following today?
	- E-shopping: Amazon, eBay, Shopee, …..
	- Used Grab ride or grab food
	- Used WhatsApp, Skype, …….
	- Used ZOOM, TEAMS, ……
	- Watched YouTube, TikTok, Netflix, …….
	- Checked your Email, Instagram, …….
	- Visited a social networking site: Facebook, Twitter, …
	- Used Google or any other websiteUsed any URL starting with https:// or a lock
- Congratulations, you’ve used SSL/TLS

- The web and email together are a key part for 99% of successful breaches.
  网络和电子邮件共同构成了 99% 成功攻击的关键部分
- ADDED SECURITY MEASURES NEEDED
	- The SSL (Secure Socket Layer, originated by Netscape) and TLS (Transport Layer Security) was designed for web security. First version of TLS can be viewed as an SSLv3.1
	  SSL（安全套接字层，由 Netscape 首创）和 TLS（传输层安全）是为 Web 安全而设计的。TLS 的第一个版本可以看作是 SSLv3.1
- HTTPS
	- Secure HTTP protocol = HTTP+SSL
	  安全的 HTTP 协议 = HTTP + SSL

## Secure Socket Layer (SSL)

- SSL is a cryptographic protocol that secure communication over networks.
  SSL 是一种用于保护网络通信的加密协议
- Primary Goals
	- Confidentiality and Integrity (via encryption)
	  **机密性和完整性**（通过加密实现）
	- Authentication (verifies identity)
	  **身份验证**（验证身份）
	- Can provide server authentication with digital certificate
	  可以通过数字证书提供服务器认证
	- It can authenticate client (rare).
	  也可以认证客户端（少见）
- HISTORY
	- Internal Netscape design, early 1994.
	- SSLv1 was broken by members of audience while it was being presented.
	  **SSLv1** 在展示时被观众攻破
	- SSLv2 was shipped with Navigator 1.0, in November 1994, however it was vulnerable to man-in-the-middle attack.
	  **SSLv2** 于 1994 年 11 月随 Navigator 1.0 发布，但易受中间人攻击
	- SSLv3 was designed by Netscape and Paul Kocher (American cryptographer, winner of 2019 Marconi Prize), in November 1996 and was designed with public input/feedback.
	  **SSLv3** 于 1996 年 11 月由 Netscape 和 Paul Kocher（美国密码学家，2019 年马可尼奖获得者）设计，并基于公众反馈完善
	- SSL is easy to apply and use because it is built in all major Web browsers (Edge, Opera, Chrome, Firefox, etc.) and servers.
	  SSL 易于应用和使用，因为它内置于所有主流 Web 浏览器（如 Edge、Opera、Chrome、Firefox 等）和服务器中

## Transport Layer Security (TLS)

![[Pasted image 20250403015518.png#pic_75center|]]

- By the end of the 1990s, Netscape handed SSL over to the IETF(Internet Engineering Task Force).
- The (IETF), renamed SSL 3 as Transport Layer Security (TLS) in 1999 and made SSL obsolete in 2015.
- SSL version 3.0 was adopted by Internet Engineering Task Force (IETF) as TLS version 1.0.
- All TLS versions up to 1.2 were backward-compatible with SSL 3.0, however, backward compatibility with SSL was removed from TLS 1.3.
- The latest version: TLS1.3 (Finalized on March 21st, 2018).
- Many people still refer to web encryption as SSL, even though most services have switched over to supporting TLS only.

| Feature        | SSL                   | TLS                              |
| :------------: | :-------------------: | :------------------------------: |
| Latest Version | SSL 3.0 (Deprecated)  | TLS 1.3 (secure)                 |
| Security       | Vulnerable to attacks | Stronger encryption & efficiency |
| Handshake      | More overhead, slower | Optimized, faster                |
| Cipher Suites  | Outdated algorithms   | Uses stronger ciphers            |

- SSL 2.0 & 3.0 are deprecated due to security vulnerabilities.
- TLS 1.2 & 1.3 are widely used, with TLS 1.3 being the most secure.

## Key Size for SSL/TLS

- There are two different types of encryption rates used with SSL/TLS
	- Session Key and Public & Private Key
- FOR PUBLIC/PRIVATE KEY
	- 512 bits is considered weak and 1024 is stronger, but can be broken
	  512位被认为是弱的，1024位更强，但仍可能被破解
	- Most providers encourage you to generate 2048-bit keys.
	  大多数服务商建议生成2048位密钥
- A SESSION KEY
	- It is generated during the SSL/TLS handshake process each time someone connects to the website.
	  每次有人连接到网站时，Session Key会在SSL/TLS握手过程中生成
	- It is shorter than the public/private key size because the data of only one session is at risk if it is broken and it reduces load on the server.
	  它比公钥/私钥的位数短，因为如果被破解，只有一个会话的数据处于风险中，而且这也减少了服务器负载
	- If the browser supports 256-bit but your web server only supports 128-bit, the SSL connection will be at 128-bit.
	  如果浏览器支持256位但您的网络服务器仅支持128位，则SSL连接将使用128位
	- The session keys are usually between 40-bit and 256-bit.
	  Session Key通常介于40位到256位之间
	- Anything lower than 128-bit is considered insecure.
	  低于128位的任何加密强度都被认为是不安全的

## SSL/TLS Architecture

![[Pasted image 20250403014343.png#pic_75center|SSL/TLS Architecture]]

## Two SSL/TLS Concepts

- SSL has two layers of protocols
	1. SESSION
	   会话
		- Association between a client and a server
		  客户端和服务器之间的关联。
		- Created by the **Handshake Protocol**
		  由**握手协议**创建
		- Defines secure cryptographic parameters that can be shared by multiple connections
		  定义了可以被多个连接共享的安全加密参数
	2. CONNECTION
	   连接
		- End-to-End reliable secure communication
		  端到端的可靠安全通信
		- Every connection is associated with a session
		  每个连接都与一个会话相关联
## SSL/TLS Protocol

- SSL RECORD PROTOCOL
	- Provides confidentiality and message integrity using shared keys established by the Handshake Protocol.
	  使用握手协议建立的共享密钥提供机密性和消息完整性

![[Pasted image 20250403020128.png#pic_75center|SSL/TLS Record Protocol]]

- CHANGE CIPHER SPEC PROTOCOL
  变更密码规范协议（CHANGE CIPHER SPEC PROTOCOL）
	- It is a very simple protocol that uses the record protocol
	  这是一种非常简单的协议，使用记录协议（Record Protocol）
	- It causes pending state to become current hence updating the cipher suite in use.
	  它使挂起状态变为当前状态，从而更新正在使用的密码套件
- ALERT PROTOCOL
	- Send SSL/TLS related alerts to peers
	  向对端发送与 SSL/TLS 相关的警报
	- Alert messages are compressed and encrypted
	  警报消息会被压缩和加密
	- MESSAGE: Two bytes, one defines fatal/warnings, other defines the code of alert
	  **消息结构**：两字节组成，一个定义警告或致命错误，另一个定义警报代码
		- Unexpected message, bad record MAC, decompression failure
		  意外消息（Unexpected message）、错误的记录 MAC（Bad record MAC）、解压失败（Decompression failure）
		- Handshake failure (no common ground), illegal parameters (inconsistent or unrecognized parameters)
		  握手失败（Handshake failure，无共同基础）、非法参数（Illegal parameters，不一致或无法识别的参数）
		- No certificate, bad certificate, unsupported certificate, certificate revoked, certificate expired, certificate unknown.
		  无证书（No certificate）、证书错误（Bad certificate）、不支持的证书（Unsupported certificate）、证书被吊销（Certificate revoked）、证书过期（Certificate expired）、证书未知（Certificate unknown）

### SSL Handshake Protocol

- The most complex part of SSL
- Allows server and client to:
	- Authenticate each other
	- Negotiate encryption and MAC algorithms
	- Negotiate cryptographic keys to be used
	- In general, to establish a state
	- Comprises a series of messages in phases
		- Establish Security Capabilities
		- Server Authentication and Key Exchange
		- Client Authentication and Key Exchange
		- Finish

| Sender | Name of Message     | Semantics (Meaning)                                                                                                                                                                                                                                                                    |
| ------ | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Client | Client Hello        | Client requests secure connection.<br>客户端请求安全连接<br>Client lists cipher suites it supports<br>客户端列出其支持的密码套件                                                                                                                                                                             |
| Server | Server Hello        | Server indicates willingness to proceed.<br>服务器愿意处理<br>Selects a cipher suite to use in the session.<br>选择一个密码套件在会话中使用                                                                                                                                                                 |
| Server | Certificate         | Server sends its digital certificate containing its public key<br>服务器发送有公钥的电子证书                                                                                                                                                                                                        |
| Server | Server Hello Done   | Server indicates that its part is finished<br>服务器提示它的部分完成                                                                                                                                                                                                                              |
| Client | Client Key Exchange | Client generates a random symmetric session key. Encrypts it with the server's public key. It sends this encrypted key to the server. The server decrypts the session key. Both sides now have the session key.<br>客户端生成一个随机对称会话密钥。用服务器的公钥加密该会话密钥。将加密后的密钥发送给服务器。服务器解密会话密钥。双方现在都拥有会话密钥。 |
| Client | Change Cipher Spec  | Client changes selected cipher suite from pending to active<br>客户端将选择的密码套件从挂起状态更改为激活状态                                                                                                                                                                                                 |
| Client | Finish              | Client indicates that its part in the initial introduction is finished<br>                                                                                                                                                                                                             |
|        |                     | Ongoing communication stage begins                                                                                                                                                                                                                                                     |

### TLS Key Exchange

- TLS is based on “hybrid” crypto system.
  TLS使用混合加密系统
- In hybrid crypto systems, public key cryptography is used to securely exchange the key between both parties, which is then used to encrypt/decrypt the data exchanged.
  在混合加密系统中，公钥加密用来加密传输双方用来加解密的密钥
- There are two main ways of doing this with public key cryptography.
	- RSA Key Exchange
	- Diffie-Hellman Key Exchange

![[Pasted image 20250403025909.png#pic_75center|TLS 1.2 Key Exchange]]

![[Pasted image 20250403025923.png#pic_75center|TLS 1.3 Key Exchange]]

#### RSA

- In TLS RSA key exchange, the shared secret is decided by the client, who then encrypts it with the server’s public key (extracted from the certificate) and sends it to the server
  在TLS RSA密钥交换中，共享密钥由客户端决定，然后客户端使用服务器的公钥（从证书中提取）加密共享密钥并将其发送给服务器

![[Pasted image 20250403024137.png#pic_75center|TLS Key Exchange, RSA]]

- RSA mode has a serious downside: it’s not forward secret.
  RSA模式有一个严重的缺点：它不具备前向保密性
- That means that if someone records the encrypted conversation and then gets a hold of the RSA private key of the server, they can decrypt the conversation.
  这意味着，如果有人记录了加密的会话，然后获得了服务器的RSA私钥，他们就可以解密会话
- This even applies if the conversation was recorded, and the key is obtained some time well into the future.
  即使会话是在过去被记录的，而密钥在未来某个时间才被获取，这种情况也适用
- To reduce the risks, RSA encryption was removed from TLS 1.3, leaving ephemeral DiffieHellman as the only key exchange mechanism.
  为了降低风险，TLS 1.3移除了RSA加密，将临时Diffie-Hellman作为唯一的密钥交换机制

#### Diffie-Hellman

![[Pasted image 20250403023526.png#pic_75center|TLS Key Exchange, Diffie-Hellman]]

![[Pasted image 20250403025437.png#pic_75center|TLS 1.3 Key Exchange, Diffie-Hellman, 客户端发送密钥和Hello是同时的]]

- Diffie-Hellman key agreement.
	- The client and server both start by creating a public and a private key pair.
	  客户端和服务器首先各自创建一个公钥和私钥对
	- They then send the public portion of their key share to the other party.
	  然后他们将密钥对的公钥部分发送给对方
	- When each party receives the public key share of the other, they combine it with their own private key and end up with the same value: the pre-master secret.
	  当每一方接收到对方的公钥后，将其与自己的私钥结合，最终得到相同的值：pre-master secret

	- The server then uses a digital signature to ensure the exchange hasn’t been tampered with.
	  服务器随后使用数字签名确保交换未被篡改
	- This key exchange is called "ephemeral" if the client and server both choose a new key pair for every exchange.
	  如果客户端和服务器每次交换都选择一个新的密钥对，这种密钥交换被称为临时的（Ephemeral）

### TLS Handshaking Phase

![[Pasted image 20250403025950.png#pic_75center|]]

![[Pasted image 20250403031432.png#pic_75center|]]

![[Pasted image 20250403031753.png#pic_75center|]]

- The TLS 1.3 handshake is significantly shorter than its predecessors.
  TLS 1.3握手显著短于其前代版本
- The Client Hello message starts the handshake. However, TLS 1.3 has reduced the number of supported ciphers from 37 to 5. This means that the client can guess what key agreement/exchange protocol will be used and then sends its key share from whatever protocol it guessed.
  握手由Client Hello消息开始。然而，TLS 1.3将支持的密码套件从37个减少到5个。这意味着客户端可以猜测将使用的密钥协议/交换协议，然后从其猜测的协议发送密钥共享部分
- The server will respond with its own Server Hello message, and it will send the certificate and its own portion of the key share, calculates the session key and ends with a server finished message.
  服务器将通过Server Hello消息进行响应，并发送证书及其密钥共享部分，计算会话密钥，并以服务器完成消息结束
- The client will authenticate the SSL certificate and use the two key shares to calculate its own copy of the session key. When this is complete it sends its own Finished message.
  客户端将验证SSL证书，并使用这两个密钥共享部分计算自己的会话密钥副本。完成后，客户端发送其完成消息

- Keys are generated/shared using **Ephemeral Diffie-Hellman (EDH or DHE)**, while the three main signature algorithms allowed in TLS 1.3 are: RSA (signature only), Elliptic Curve Digital Signature Algorithm (ECDSA) and Edwards-curve Digital Signature Algorithm (EdDSA).
  密钥通过**临时Diffie-Hellman（EDH或DHE）** 生成/共享，而TLS 1.3中允许的三种主要签名算法是：RSA（仅签名）、椭圆曲线数字签名算法（ECDSA）和Edwards曲线数字签名算法（EdDSA）

### Improved Security with TLS 1.3

- TLS 1.2 is secure if it’s configured correctly, but improper configuration can leave websites open to cyber attacks.
- To offer better protection, version 1.3 has done away with numerous obsolete features that have known vulnerabilities including:
	- 3DES
	- DES
	- MD5
	- RC4
	- SHA-1
	- …
- Because the new protocol has been simplified, administrators are less likely to make mistakes, which is the main issue with TLS 1.2 and that leave websites open to attacks during configuration.

### Summary

| Version | Status      | Key Features                                                |
| :-----: | :---------: | ----------------------------------------------------------- |
| SSL 2.0 | Obsolete    | Weak encryption, deprecated in 1995                         |
| SSL 3.0 | Deprecated  | Vulnerable to POODLE attack                                 |
| TLS 1.0 | Deprecated  | Susceptible to downgrade attacks                            |
| TLS 1.1 | Deprecated  | Improved security but outdated                              |
| TLS 1.2 | Secure      | Supports ARS-GCM, SHA-256, better security                  |
| TLS 1.3 | Most Secure | Removes weak ciphers, faster handshake, improved encryption |

- Improvements in TLS 1.3
	- Removes outdated cryptographic algorithms (RSA key exchange, SHA-1).
	- Faster handshake (reduced round trips from 2 to 1).
	- Perfect Forward Secrecy (PFS): Ensures past communications remain secure even if a key is compromised.
	- Stronger encryption (ChaCha20, AES).

#### Common SSL/TLS Attacks & Mitigations

| Attack                   | Description                                 | Mitigation                                     |
| ------------------------ | ------------------------------------------- | ---------------------------------------------- |
| MITM (Man-in-the-Middle) | Attacker intercepts communication           | Use HTTPS, Verify certificates                 |
| Downgrade Attack         | Forces use of old insecure TLS/SSL versions | Disable TLS 1.0/1.1 and enforce TLS 1.2 or 1.3 |
| BEAST Attack             | Exploits weaknesses in TLS 1.0              | Upgrade to TLS 1.2 ot 1.3                      |
| POODLE Attack            | SSL 3.0 vulnerability                       | Disable SSL 3.0, Use TLS 1.2 or 1.3            |
| Heartbleed               | OpenSSL volnerability leaks memory          | Update OpenSSL patches                         |
| DROWN Attack             | Exploits SSL v2 on misconfigured servers    | Disable SSLv2 and weak ciphers                 |

#### TLS

- Server-Side Best Practices
	- Use TLS 1.2 or 1.3 (disable older versions).
	  使用TLS 1.2或1.3（禁用较旧版本）
	- Strong cipher suites (AES, ChaCha20).
	  使用强密码套件（AES、ChaCha20）
	- Enable Perfect Forward Secrecy (PFS).
	  启用完全前向保密（PFS）
	- Enable HSTS (HTTP Strict Transport Security).
	  启用HTTP严格传输安全（HSTS）
	- Use OCSP Stapling to check certificate validity.
	  使用OCSP Stapling检查证书有效性
	- Regularly update OpenSSL, TLS libraries.
	  定期更新OpenSSL、TLS库
- Client-Side Best Practices
	- Validate SSL/TLS certificates before connecting.
	  在连接前验证SSL/TLS证书
	- Use certificate pinning to prevent MITM attacks.
	  使用证书绑定以防止中间人攻击（MITM）
	- Disable weak protocols and ciphers in browsers.
	  在浏览器中禁用弱协议和密码
- Summary & Key Takeaways
	- TLS (not SSL) should be used for secure communication.
	  应使用TLS（而非SSL）进行安全通信
	- TLS 1.3 is the most secure version, removing weak ciphers.
	  TLS 1.3是最安全的版本，移除了弱密码
	- TLS certificates ensure authentication and data security.
	  TLS证书确保认证和数据安全
	- Regular security updates are essential for TLS security.
	  定期进行安全更新对于TLS安全很关键

#### Issues with SSL/TLS

- It slows down servers.
  它会减慢服务器速度
- It protects data in transit, but not databases.
  它保护传输中的数据，但不保护数据库中的数据
- SSL/TLS Cannot:
	- Authenticate the actual operator of a computer
	  验证计算机的实际操作者
	- Authenticate the owner of an online shop (merchant)
	  验证在线商店（商户）的所有者
	- Authenticate the actual online consumer
	  验证实际的在线消费者
	- Authenticate other parties involved in online payment system
	  验证在线支付系统中涉及的其他方
	- Protect the use of stolen credit cards online
	  线上保护被盗信用卡
- Cost of the certificate used in SSL/TLS (Depending on the type of certificate as the price will vary quite a bit)
  使用在SSL/TLS中的证书的成本（取决于证书的类型，价格会有很大差异）
- SSL is a two-party protocol (unlike SET).
  SSL是一个双方协议（与SET不同）

### SSL/TLS Best Practices

- Choose a Reliable Certificate Authority (CA)
  选择可靠的证书授权机构（CA）
	- Certificates are only as trustworthy as the CA that issues them, therefore, choose most reputable CA.
- Secure Private Key
  保护私钥
	- The SSL/TLS protocol uses a pair of keys to authenticate identities and encrypt information sent over the Internet. One of these (the public key) is intended for wide distribution, and the other (the private key) should be kept as securely as possible.
	  SSL/TLS协议使用一对密钥来验证身份并加密通过互联网发送的信息。其中一个（公钥）用于广泛分发，另一个（私钥）应尽可能地安全保管
- Use TLS 1.3
	- Widespread browser support of earlier SSL/TLS versions, such as SSLv3, is long gone. While TLS 1.2 is currently the most widely-used version of the SSL/TLS protocol, TLS 1.3 (the latest version) is already supported in the current versions of most major web browsers.
	  早期的SSL/TLS版本（如SSL v3）已不再广泛支持。目前，TLS 1.2是最广泛使用的SSL/TLS协议版本，而最新版本TLS 1.3已在大多数主流网页浏览器的当前版本中获得支持
	- TLS 1.3 is the preferred choice as it provides forward secrecy for all TLS sessions via the Ephemeral Diffie-Hellman (EDH or DHE) key exchange protocol, which is faster and more secure.
	  TLS 1.3是首选，因为它通过临时Diffie-Hellman（EDH或DHE）密钥交换协议为所有TLS会话提供前向保密性，同时速度更快、安全性更高

# SET (Secure Electronic Transaction)

![[Pasted image 20250403035010.png#pic_75center|]]

- SET was a messaging protocol specifically designed by Master Card, Visa, and others in 1996 to secure bank-card payment transactions over open networks.
  SET是一种消息协议，由Master Card、Visa等公司在1996年专门设计，用于通过开放网络保护银行卡支付交易的安全
- It is not a payment system, rather a set of security protocols & formats.
  它不是支付系统，而是一组安全协议和格式
- Not widely deployed.
  SET未被广泛部署使用
- SET models all the players involved in card payments: Purchaser, (Merchants, Banks) , the trust relationships between them, legal meaning of digital signatures.
  SET对卡支付中的所有参与者进行了建模：购买者（商户、银行），他们之间的信任关系，以及数字签名的法律意义
- SET provides cryptographic identity authentication of every entity involved in a transaction (multiparty security).
  SET为交易中涉及的每个实体提供加密的身份认证（多方安全）
- SET uses message not channel encryption.
  SET使用消息加密，而非通道加密
  >  - **消息加密**：
  > 	 - 对具体的消息内容进行加密。
  > 	 - 加密后的消息可以存储或发送，不依赖于传输的安全性。
  > 	 - 即使消息离开加密通道，依然保持加密状态。
  > 	 - 适用于需要存储加密数据或防止数据本身被篡改的场景。
  >  - **通道加密**：
  > 	 - 对整个通信通道进行加密，确保数据在传输过程中不会被拦截或窃取。
  > 	 - 通信通道关闭后，数据本身可能不会保持加密状态。 
  > 	 - 依赖于协议（如SSL/TLS）来保护传输的数据。 
  > 	 - 适用于实时通信和数据在传输途中保密的场景。
- With SET every cardholder is issued a digital signature. This, plus the software that talks SET protocol, compose a SET electronic wallet.
  使用SET时，每个持卡人都会被分配一个数字签名。这与实现SET协议的软件一起组成一个SET电子钱包
- SET messages are essentially the same as those that have been used in the traditional banking networks for years.
  SET消息基本与传统银行网络中多年来使用的消息相同

---

- SET allows them to flow across the insecure, open Internet.
  SET允许它们通过不安全的开放互联网传输。
- SET defines all necessary communication between banks, merchants, cardholders, whereas SSL creates a secure connection between 2 computers.
  SET定义了银行、商户、持卡人之间所有必要的通信，而SSL仅在两台计算机之间创建安全连接
- SET provides merchants with assurance that the card holder will not say “it is not me”; the bank has evidence that I made a purchase.
  SET为商户提供保证，确保持卡人不会声称“这不是我”；银行拥有我进行购买的证据
- SET provides a card holder with assurance that the merchant is legitimate.
  SET为持卡人提供保证，确保商户是合法的
- Disadvantage
	- SET requires appropriate software installed in the banking network, at merchant’s locations, and on consumer’s computers.
	  SET需要在银行网络、商户地点以及消费者的计算机上安装适当的软件
- Advantage
	- Merchant does not have access to client’s account information (privacy of financial data).
	  商户无法访问客户的账户信息（财务数据的隐私性）
- SET offers a complete card payment system (payment transport, confirmation and inquiry).
  SET提供一个完整的卡支付系统（包括支付传输、确认和查询）
- Confidentiality: Symmetric Key Cryptography
  机密性：对称密钥密码术
- Authorization: Public key Cryptography RSA
  授权：公钥密码术（RSA）
- Integrity: Hashing
  完整性：哈希

## SET Transaction

1. Customer opens account.
   客户开户
2. Customer receives a certificate.
   客户收到证书
3. Merchants have their own certificates.
   商户拥有自己的证书
4. Customer places an order.
   客户下订单
5. Merchant is verified.
   验证商户
6. Order and payment are sent.
   订单和付款被发送
7. Merchant requests payment authorization.
   商户请求支付授权
8. Merchant confirms order.
   商户确认订单
9. Merchant provides goods or service.
   商户提供商品或服务
10. Merchant requests payment.
    商户请求付款

## SET vs. SSL/TLS

- The primary differences between the SSL and the SET protocol are that SSL can not provide irrefutability and only provides server-side authentication while SET uses digital certificates to authenticate both the cardholder and the merchant making it difficult for charges to be refuted.
  SSL协议和SET协议的主要区别在于，SSL不能提供不可否认性，并且仅提供服务器端认证，而SET通过使用数字证书同时认证持卡人和商户，使得难以否认交易
- By using SET, merchants can be assured that received orders have not been altered.
  使用SET可以确保商户收到的订单未被篡改
- WILL SET REPLACE SSL/TLS IN THE FUTURE?
	- NO, there are virtually no technical similarities between SET and SSL, except that both use cryptography and digital certificates.
	  不会，SET和SSL之间几乎没有技术相似性，除了它们都使用密码学和数字证书
- Is SET dead ?
	- NO, however it is not being used at all.
	  没有，但它完全没有被使用
- Is SSL good enough for e-commerce?
	- NO, but it is being used as there is no other choice
	  不够，但由于没有其他选择，它仍被使用
- Does SSL merchant know who the client is?
	- NO

| Issue                            | Secure Socket Layer (SSL)                                                                  | Secure Electronic Transaction (SET)                                                     |
| -------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| Main Aim                         | Exchange of Data in an Encrypted form<br>以加密形式交换数据                                         | Ecommerce Related payment mechanism<br>与电子商务相关的支付机制                                     |
| Certification                    | Two parties exchange certification<br>双方交换认证                                               | All parties so involved must be certified by third trusted party<br>所有相关方必须由第三方可信机构进行认证 |
| Authentication                   | Mechanisms in place but not very strong<br>机制存在但不够强                                        | Strong mechanism in SET for all parties involved<br>对所有参与方提供强有力的身份验证机制                  |
| Risk of Merchant Fraud           | Possible since customer gices Financial details to merchant<br>可能，因为客户将财务信息提供给商户           | Unlikely as Financial details are gicen to PAYMENT Gateway<br>不太可能，因为财务信息提供给支付网关        |
| Risk of Customer Fraud           | Possible as no mechanism exist if a customer refuses to pay later<br>可能，因为如果客户拒绝支付，缺乏相应的机制 | Customer has to digitally sign payment instructions<br>客户必须对支付指令进行数字签名                  |
| Action in case of customer fraud | Merchant is Liable<br>商户承担责任                                                               | Payment Gateway is Liable<br>支付网关承担责任                                                   |
| Practical Usage                  | High                                                                                       | Not much                                                                                |

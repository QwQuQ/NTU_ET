---
aliases: 
tags:
  - cyber_security
---

# Digital Signature

| HAND-WRITTEN                                                      | DIGITAL                                           |
| :---------------------------------------------------------------: | :-----------------------------------------------: |
| Physical part of the document signed                              | No physical part                                  |
| Verify the signature by comparing it with the authentic signature | Verify the signature by a publicly know algorithm |
| Easy to forge                                                     | Hard to forge                                     |

- In today’s digital world, there’s a need for authenticity when sending documents over insecure channels.
- With authenticity, we can protect ourselves from malicious third-parties trying to use someone’s identity.
  通过真实性，我们可以保护自己免受恶意第三方冒用身份的威胁。
- Digital signing is used to provide trust that the content has come from the claimed source and has not been altered.
  数字签名用于确保内容来自声明的来源且未被更改。
- Basic feature of digital signatures consists of two components
	- A signing algorithm: A private signing algorithm which permits a user to securely sign a message
	  签名算法：一个私有的算法以让用户能够对一条消息签名
	- A verification algorithm: A public verification algorithm which permits anyone to verify that the signature is authentic.
	  验证算法：一个公开的算法让任何人都能验证这个签名是真实的

![[Pasted image 20250402193635.png#pic_75center|]]

- A digital signature (“digital thumbprint”) is a message digest used to cryptographically sign a message.
  数字签名（“数字指纹”）是一种用于密码学签署消息的消息摘要
- Digital signatures rely on asymmetric (public key) cryptography.
  数字签名依赖于非对称（公钥）密码学
- To create a digital signature, you sign the message with your private key. The digital signature then becomes part of the message.
  要创建数字签名，您使用私钥签署消息。数字签名随后成为消息的一部分
- This has two effects:
	- Any changes to the message can be detected, due to the message digest algorithm.
	  由于消息摘要算法，消息的任何更改都可以被检测到
	- You can not deny signing the message, because it was signed with your private key.
	  由于消息是用您的私钥签署的，您不能否认签署了消息
- These two features, message integrity and non-repudiation, make digital signatures a very useful component for e-commerce applications.
  这两个功能——消息完整性和不可否认性，使数字签名成为电子商务应用中的一个非常有用的组件。
- Digital signature can be used in all electronic communications
  数字签名可以用于所有电子通信中。
- It is an electronic stamp or seal that is append to the document.
  它是一种电子邮戳或印章，可附加到文档上。
- Ensure that the document remains unchanged during the transmission
  - 确保文档在传输过程中保持不变。

- Properties
	- Only private-key holder can compute signatures.
	  只有私钥持有者可以计算签名
	- Any holder of matching public-key can verify signature.
	  任何匹配公钥的持有者都可以验证签名
	- Digital signature schemes work with two major steps:
		- Prepare a message representative
		- Apply a signature transform.
		- The general verifying method is generally similar to the signing method
		  通用的验证方法通常与签名方法类似
		- Undo the signature transformation
		  撤销签名转换
		- Check the message digest for any issues
		  检查消息摘要是否存在问题

- HOW DOES DIGITAL SIGNING WORK?
	- We extract a value (binary string) from the message with a **[[Hash]]** function.
	  我们使用哈希从消息中提取一个值（二进制字符串）
	- We use a digital signature algorithm to produce the signature from the hash value and the private key.
	  我们使用数字签名算法根据哈希值和私钥生成签名
	- The message can now be authenticated with the public key and the signature
	  现在可以通过公钥和签名来验证消息的真实性

![[Pasted image 20250403002809.png#pic_75center|不进行消息保护的数字签名过程]]

![[Pasted image 20250403002921.png#pic_75center|进行消息保护的数字签名流程]]

# Finding the True Party's Public Key

- Cannot use the sender’s public key
  不能使用发送者的公钥
	- It would always “validate” the sender’s digital signature
	  它总是能“验证”发送者的数字签名
- Normally requires a digital certificate
  通常需要一个数字证书
	- File provided by a certificate authority (CA)
	  由证书授权机构（CA）提供的文件
		- The certificate authority must be trustworthy
		  证书授权机构必须是可信的
	- Digital certificate provides the subject’s (True Party’s) name and public key
	  数字证书提供了主体（真实方）的姓名和公钥
# Digital Certificates & Certificate Authoritie

- A digital certificate is an electronic document, similar to a digital signature, attached to a file certifying that this file is from the organization it claims to be and has not been modified from the original format
  **数字证书**是一种电子文档，类似于数字签名，附加在文件上，用于证明该文件来自声称的组织，并且未被修改过其原始格式
- A Certificate Authority is an agency that manages the issuance of certificates and serves as the electronic notary public to verify their worth and integrity
  证书授权机构（CA）是一个管理证书签发的机构，充当电子公证人以验证证书的价值和完整性
- For digital signatures to work, a trusted third party known as a Certification Authority (CA) is needed to issue digital certificates that certify the electronic identities of users and orgnizations.
  为了使数字签名发挥作用，需要一个名为证书授权机构（CA）的可信第三方来颁发数字证书，以认证用户和组织的电子身份
- Some Trusted CA operating in Singapore
	- Verisign
	- GlobalSign
	- Netrust Pte Ltd

![[Pasted image 20250403005914.png#pic_75center|如何获取一个数字证书]]

## X.509 Digital Certificate Fields

| Field                          |                                                                                                    Description                                                                                                     |
| :----------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Version Number                 | Version number of the X.509 standard. Most certificates follow Version 3. Different versions have different fields. This figure reflects the Version 3 standard.<br>X.509标准的版本号。大多数证书遵循版本3。不同的版本包含不同的字段。此图反映了版本3标准 |
| Issuer                         |                                                                                       Name of the Certificate Authority (CA)                                                                                       |
| Serial Number                  |   Unique serial number for the Certificate set by the CA<br>由证书授权机构（CA）设置的证书唯一序列号。<br>Serial number allows the receiver to check if the digital certificate has been revoked by the CA<br>序列号允许接收方检查数字证书是否已被CA吊销   |
| Subject (True Party)           |                          The name of the person, organization, computer, or program to which the certificate has been issues. This is the true party<br>证书签发对象的名称，可以是个人、组织、计算机或程序。这是真正的主体                          |
| Public Key                     |                                                                            The public key of the subject (the true party)<br>主体（真实方）的公钥                                                                            |
| Public Key Algorithm           |                                                                      The algorithm the subject uses to sign messages with digital signatures.                                                                      |
| Digital Signature              |                                              The digital signature of the certificate, signed by the CA with the CA's own private key<br>由证书授权机构（CA）使用其自身私钥签署的证书数字签名。                                              |
| Signature Algorithm Identifier |                                                          The digital signature algorithm the CA uses to sign its certificates<br>证书授权机构（CA）用于签署其证书的数字签名算法                                                          |
| Other fields                   |                                                                                                        ...                                                                                                         |

## Verifying the Digital Certificate

- TESTING THE DIGITAL SIGNATURE
	- The digital certificate has a digital signature of its own
	  数字证书本身具有一个数字签名
	- Signed with the Certificate Authority’s (CA’s) private key
	  由证书授权机构（CA）的私钥签名
	- Must be tested with the CA’s well-known public key
	  必须使用CA的众所周知的公钥进行验证
	- If the test works, the certificate is authentic and unmodified
	  如果验证成功，则证明证书是可信的且未被修改
- CHECKING THE VALID PERIOD
	- Certificate is valid only during the valid period in the digital certificate
	  证书仅在数字证书中的有效期内有效
	- If the current time is not within the valid period, reject the digital certificate
	  如果当前时间不在有效期内，则拒绝该数字证书
- CHECKING FOR REVOCATION
	- Certificates may be revoked for improper behavior or other reasons
	  证书可能因不当行为或其他原因被吊销
	- Revocation must be tested
	  必须对吊销状态进行检查
	- Cannot be done by looking at fields within the certificate
	  不能通过查看证书中的字段来完成
	- Receiver must check with the CA
	  接收方必须向CA确认

# Summary

- Digital signature can provide nonrepudiation and authentication
  数字签名可以提供不可否认性和认证功能
- Nonrepudiation means that the sender cannot deny that he or she sent a message
  不可否认性意味着发送者无法否认他或她发送了一条消息
- With digital signatures, the sender must use his or her private key
  使用数字签名时，发送者必须使用其私钥
	- It is difficult to repudiate that you sent something if you use your private key.
	  如果使用私钥签名某物，否认其发送行为是困难的
- Hashing is used to make sure that digital signatures are not altered.
  哈希用于确保数字签名未被篡改
- Digital certificates provide assurance that the public-key claimed by the user does indeed belong to him/her.
  数字证书保证用户所声称的公钥确实属于他/她
- Certification authorities (CAs) are responsible for issuing digital certificates and are supposed to be trustworthy. However, in practice many CAs are not regularized and thus, it is important to only accept certificates issued by reputable CAs.
  证书授权机构（CA）负责颁发数字证书，并且被认为是可信的。然而，实际上许多CA并未被严格监管，因此，重要的是仅接受由声誉良好的CA签发的证书

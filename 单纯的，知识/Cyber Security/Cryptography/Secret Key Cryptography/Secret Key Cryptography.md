---
aliases:
  - "Symmetric \rEncryption"
tags:
  - cyber_security
---

![[Pasted image 20250402125900.png#pic_75center|]]

- Uses a single key to encrypt and decrypt a message.
- Main problem is getting the sender and receiver to agree on the secret key without anyone else finding out.
- This requires a method by which the two parties can communicate without fear of eavesdropping.
- ADVANTAGES OF SKC
	- Speed: Algorithms are computationally efficient, making them suitable for encrypting large amounts of data.
	- Simplicity: Easier to implement compared to asymmetric cryptography.
	- Wide Adoption: Used in many real-world applications, such as SSL/TLS, disk encryption, and file encryption.
- DISADVANTAGES OF SKC
	- Key Distribution: Securely sharing the secret key between parties is a major challenge.
	- Scalability: In a network with many users, managing unique secret keys for each pair becomes impractical.

# Popular Symmetric Encryption Algorithms

- **DES**, **3DES**, **AES**, CAST, RIVEST, Blowfish, IDEA and many others
- DES was the first symmetric key algorithms used for commercial applications, while 3DES was a temporary solution to replace DES
- AES is the current gold standard and is widely used in numerous commercial and government applications all over the world

![[Pasted image 20250402144347.png#pic_50center|]]

# Data Encryption Standard (DES)

![[Pasted image 20250402144714.png#pic_75center|]]

- In 1973, the National Bureau of Standards (NBS) now National Institute of Standards and Technology (NIST) requested proposals for national symmetrickey cryptosystem.
  1973年，美国国家标准局（NBS），现为国家标准与技术研究院（NIST），请求提交一项国家对称密钥加密系统的提案。
- A proposal from IBM, a modification of a project called Lucifer, was accepted as DES. DES was adopted in 1976-77.
  IBM提交的一个名为“Lucifer”项目的改进版本被采纳为DES（数据加密标准）。DES在1976-77年被正式采用
- The request specified the following set of design criteria:
  需求规定了以下设计标准
	- The cryptographic algorithm must be secure to a high degree.
	  加密算法必须具有高度的安全性
	- The details of the algorithm should be described in an easy-to-understand computer language.
	  算法的详细内容应以易于理解的计算机语言描述
	- The security of the algorithm must depend on the key.
	  算法的安全性必须依赖于密钥
	- The details of the algorithm must be publicly available, so that anyone could implement it in software or hardware.
	  算法的细节必须公开，以便任何人都可以在软件或硬件中实现它
	- The method must be adaptable for use in many applications.
	  方法必须能够适应多种应用场景
	- Hardware implementation of the algorithm must be practical.
	  算法的硬件实现必须可行
	- The method must be efficient (i.e., fast and with reasonable memory requirements).
	  该方法必须高效（即快速且内存要求合理）
	- It should be possible to test and validate the algorithm under real-life conditions.
	  必须能够在现实条件下测试和验证算法
---
![[Pasted image 20250402145355.png#pic_75center|]]
- Block cipher
	- The block size is 64 bits. This means 64 bits of plaintext gives out 64 bits of ciphertext.
	- 56-bit key length
	- Performs a substitution and permutation (a form of transposition) based on the key 16 times on every 64-bit block.
	  根据密钥，对每个64位数据块执行替换和置换（置换是一种转置形式），重复16次。

![[Pasted image 20250402145541.png#pic_75center|]]
> 密钥长 64 位，密钥事实上是 56 位参与 DES 运算（第8、16、24、32、40、48、56、64位是奇偶校验位）

- The DES cipher encrypts messages 64 bits at a time. The DES cipher (in codebook mode) needs two inputs.
  DES密码算法每次加密消息64位。在代码本模式（codebook mode）下，DES算法需要两个输入
  > **Electronic Code Book (ECB)**: Each block encrypted separately
	  电子密码本（ECB）：每个块单独加密

- Strengths
	- Simple and efficient to implement in hardware and software.
	  在硬件和软件中实现简单且高效
	- Well-studied and understood, making it a good teaching tool for cryptography.
	  经过充分研究和理解，非常适合作为密码学教学工具
- Weaknesses
	- Short key length (56 bits) makes it vulnerable to brute-force attacks.
	  密钥长度较短（56位），容易受到暴力破解攻击
	- Fixed S-boxes and permutations may have hidden weaknesses.
	  > S-boxes: Substitution-box是对称密钥算法中执行置换计算的基本结构
- Applications of DES
	- Historically used in financial systems, secure communications, and government applications.
	- Replaced by AES in most modern applications but still used in legacy systems.
	- DES is no longer considered secure for most applications.
	- It is primarily used for educational purposes and in legacy systems.
	- AES (Advanced Encryption Standard) is the recommended replacement.

## DES Structure

![[Pasted image 20250402145952 1.png#pic_75center|]]

- The encryption process is made of two permutations (P-boxes), called initial and final permutations, and sixteen rounds
  加密过程由两个序列（P-Boxes）组成，被称为初始和最终序列，包含16轮加密操作。
  > P盒的作用是扩散(Diffusion)，目的是让明文和密钥的影响迅速扩散到整个密文中。即1位的明文或密钥的改变会影响到密文的多个比特

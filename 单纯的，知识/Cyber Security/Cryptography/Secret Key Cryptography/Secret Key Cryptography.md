---
aliases:
  - "Symmetric \rEncryption"
  - 私钥加密
  - 对称加密
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
	  固定的S盒和置换可能存在隐藏的弱点
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
  加密过程由两个置换组成（P-Boxes）组成，被称为初始和最终置换，包含16轮加密操作。
  > P盒的作用是扩散(Diffusion)，目的是让明文和密钥的影响迅速扩散到整个密文中。即1位的明文或密钥的改变会影响到密文的多个比特

## DES Controversy

- Originally designed by researchers at IBM in the early 1970s with block size and key size as 128 bits. However, once it was adopted as DES, the key size was changed to 56 and the block size to 64. According to USA government, this was done in order to ensure that DES was quickly adopted by industries such as financial services, where the need for strong encryption is high. This argument proved to be true as the simplicity of DES saw it used in a wide variety of applications. However, many security experts felt the 56-bit key length was inadequate even before DES was adopted as a standard. Another change made to original algorithm LUCIFER was that S-boxes were designed under classified conditions and no reasons for their particular design were ever given. This change led people to assume that the NSA had introduced a “trapdoor” through which they could decrypt any data encrypted by DES even without knowledge of the key.
- 最初，DES由IBM的研究人员在1970年代初设计，原始算法的块大小和密钥大小均为128位。然而，当它被采纳为DES（数据加密标准）时，密钥大小被改为56位，块大小改为64位。据美国政府称，这样的更改是为了确保DES能够迅速被包括金融服务在内的行业采纳，因为这些行业对强加密的需求较高。事实证明，这一观点是正确的，因为DES的简单性使其被广泛应用于各种领域。然而，许多安全专家在DES成为标准之前就已经认为56位的密钥长度不足。另一个对原始算法LUCIFER的更改是，S盒的设计是在保密条件下完成的，并且没有提供设计理由。这一变化使得人们猜测，美国国家安全局（NSA）可能通过这种设计引入了一个“后门”，使其能够在不知密钥的情况下解密任何用DES加密的数据。

# Someone Broke DES, so What?

![[Pasted image 20250402153125.png#pic_75center|]]

- Use DES multiple times?
- How many Times?

## Use Double DES (2 DES)

![[Pasted image 20250402153510.png#pic_75center|2 DES]]

- Use DES twice, with two keys ($2\times 56 = 112 \text{bits}$)
- ISSUES
	- With two pair of keys of known plain-text/cipher-text, double DES can be guessed with very high confidence, for roughly same computational complexity as breaking DES itself.
	  在已知两对明文/密文的情况下，可以以与破解单一DES相似的计算复杂度，高概率猜出双重DES的密钥
	- Also Meet-in-the middle- attack using known plain/cipher pairs.
	  还存在使用已知明文/密文对的中途相遇攻击（Meet-in-the-Middle Attack）

## Use DES Thrice (3 DES)

![[Pasted image 20250402153853.png#pic_75center|3 DES]]

![[Pasted image 20250402154030.png#pic_50center|]]

- Triple DES (3DES) is a variant of DES.
	- Multiple encryption – goes through the DES algorithm three times.
	- It is three times slower than regular DES but can be billions of times more secure if used properly.
	- 3DES is stronger than DES but has similar weakness.
	- The longer key length makes it more resistant to brute force attacks.
	- 3DES was a good interim step before the new encryption standard, AES.

- ISSUES
	- #TODO 

# AES (Advanced Encryption Standard)

- Rather than using just a substitution and a permutation at each stage like DES, AES consists of multiple cycles of Substitution, Shifting, Column mixing and a KeyAdd operation.
  与DES每阶段仅使用替换和置换不同，AES由多个循环组成，包括替换（Substitution）、移位（Shifting）、列混合（Column Mixing）和密钥加操作（KeyAdd Operation）。

![[Pasted image 20250402155314.png#pic_75center|]]
![[Pasted image 20250402155512.png#pic_75center|]]

## AES Selection Process

- When proposals were called by USA government to replace DES/3DES with a secure encryption system, there were 15 finalist competitors.
- The most prominent were:
	- MARS: submitted by a large team from IBM Research
	- RC6: submitted by RSA Security
	- **Rijndael: submitted by two Belgian cryptographers, Joan Daemen and Vincent Rijmen**
	- Serpent: submitted by Ross Anderson, Eli Biham and Lars Knudsen
	- Twofish: submitted by a large team of researchers from Counterpane Internet Security, including noted cryptographer Bruce Schneier
- It was Rijndael, that eventually became the standard and henceforth acquired the title Advanced Encryption Standard or AES. The selection process was very stringent, taking 5 years to complete. During that span, many experts from the cryptographic community carried out detailed tests and painstaking discussions to find vulnerabilities and weaknesses.
  最终，Rijndael被选为标准，并因此获得了“高级加密标准”（AES）的称号。整个甄选过程非常严格，历时5年完成。在此期间，密码学界的许多专家进行了详细的测试和艰苦的讨论，以发现潜在的漏洞和弱点。

- Although the cipher's strength against various attacks was a major consideration in choosing the standard, other factors like speed, versatility, and computational requirements were likewise given importance. The government wanted an encryption standard that wasn't just strong, but also fast, reliable and easily implemented in both software and hardware - even those with limited CPU and memory. Although the other encryption algorithms were also very good (Some of those ciphers are also widely used today but understandably don't enjoy the same level of acceptance as AES) the Rijndael cipher was ultimately selected and declared a Federal Information Processing Standards or FIPS standard by the NIST (National Institute of Standards and Technology) in 2001. In 2003, the government deemed it suitable for protecting classified information. In fact, up to this day, the NSA (National Security Agency) is using AES to encrypt even Top Secret Information. That should explain why AES has gained the confidence of various industries. If it's good enough for the NSA, then it must be good enough for businesses.
- 尽管密码对各种攻击的强度是选择标准时的主要考虑因素，但诸如速度、通用性和计算需求等其他因素同样重要。  政府希望一种加密标准不仅强大，而且快速、可靠，并且可以轻松地在软硬件中实现——甚至是在有限的CPU和内存条件下。  尽管其他加密算法也非常优秀（其中一些密码今天仍被广泛使用，但可以理解的是，它们的接受程度不如AES），最终选择了Rijndael密码，并在2001年由NIST（国家标准与技术研究院）宣布为联邦信息处理标准（FIPS）。  2003年，政府认为其适合用于保护机密信息。实际上，直到今天，美国国家安全局（NSA）仍在使用AES来加密最高机密的信息。这应该可以解释为什么AES赢得了多个行业的信任。如果对NSA来说足够好，那么对企业来说也一定足够好

## Differences Between AES and RIJINDAEL

- Rijndael allows for both key and block sizes to be chosen independently from the set of 128, 160, 192, 224, 256 bits.
  Rijndael允许块大小和密钥大小独立选择，可以从以下选项中进行选择：128位、160位、192位、224位和256位。
- However, AES specifies that the block size must always be 128 bits in AES, and that the key size may be either 128, 192, or 256 bits.
  然而，AES规定，在AES中，块大小必须始终为128位，而密钥大小可以是128位、192位或256位
- Therefore AES-128, AES-192, and AES-256 are actually: In other words, AES has a fixed block size of 128 bits and a key size of 128, 192, or 256 bits, whereas Rijndael can be specified with block and key sizes in any multiple of 32 bits, with a minimum of 128 bits and a maximum of 256 bits.
  因此，AES-128、AES-192和AES-256实际上是：换句话说，AES的块大小固定为128位，而密钥大小可选为128位、192位或256位；相比之下，Rijndael可以指定块和密钥大小为任意32位的倍数，最小为128位，最大为256位

## Summary

- Advanced Encryption Standard, also known as Rijndael, is a **block cipher** adopted as an encryption standard by the US government
- Result of a public process
- Evaluation criteria:
	- Security
	- No licensing
	- Computational efficiency
	- Memory requirements
	- Flexibility (key size, block size, time/memory tradeoffs)
	- Hardware and software suitability
	- Simplicity of design
- Acts on 128-bit blocks
- Key 128, 192 or 256 bits (for 10, 12, 14 rounds)
- WHY IS AES SECURE?
- Considered highly secure and resistant to all known practical attacks when implemented correctly.
	- Large Key Space
		- 128-bit AES has $2^{128}$ possible keys (infeasible to brute-force).
		- 256-bit AES has $2^{256}$ possible keys (even stronger).
	- Resistant to Cryptanalysis
		- No practical attacks exist against full AES.
		- Resistant to differential, linear, and algebraic attacks.
- Widespread Adoption
	- Used by governments (NSA, NIST), banks, and enterprises.
	- TLS, VPNs, disk encryption, and messaging apps rely on AES.
- AES is the gold standard of encryption, ensuring secure communication and data protection worldwide.
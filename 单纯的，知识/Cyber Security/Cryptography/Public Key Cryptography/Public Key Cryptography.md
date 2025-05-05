---
aliases:
  - "Asymmetric \rEncryption"
  - 公钥加密
  - 不对称加密
tags:
  - cyber_security
---

![[Pasted image 20250402163506.png#pic_75center|]]

- SYMMETRIC ALGORITHMS ARE IMPORTANT BECAUSE
	- They are comparatively fast and have few computational requirements
- THEIR MAIN WEAKNESSES
	- Two geographically distant parties both need to have a key that matches the other key exactly.
	  两个地理位置遥远的参与者都需要拥有完全匹配的密钥
	- Secure key exchange is an issue.
	  安全的密钥交换是一个问题
- PUBLIC KEY (ALSO KNOWN AS ASYMMETRIC-KEY ENCRYPTION)
	- Uses two different but related keys
	  使用两个不同但相关的密钥
	- Either key can encrypt or decrypt message
	  任一密钥都可以加密或解密消息
	- If Key A encrypts message, only Key B can decrypt
	  如果密钥A加密消息，则只有密钥B能解密
	- One key serves as private key and the other serves as public key
	  一个密钥作为私钥，另一个密钥作为公钥
- PUBLIC KEY ALGORITHMS
	- DIFFIE-HELLMAN, El-Gamal, RSA and Elliptic Curve

- USES 2 KEYS
	- PUBLIC-KEY: May be known by anybody, and can be used to encrypt messages, and verify signatures.
	  能够被任何人知道，并且可以用来加密文件和验证签名
	- PRIVATE-KEY: Known only to the recipient, used to decrypt messages, and sign (create) signatures.
	  只有接收者知道，能够解密文件和创建签名

- Keys are mathematically related to each other but it is not feasible to find out private key from the public key
  密钥们在数学上是互相关联的，但从公钥中找到私钥是不可能的

- PKC was invented by Whitfield Diffie and Martin Hellman in 1976
	- PhD students at Stanford University
- Some give credit to Ralph Merkle (in 2002, he was recognized)
- NSA says that they knew PKC back in 60’s
- The two main uses for public key cryptography are:
	- PUBLIC KEY ENCRYPTION: A message encrypted with a recipient's public key cannot be decrypted by anyone except a possessor of the matching private key. This is used to attempt to ensure confidentiality.
	  公钥加密：使用接收者的公钥加密的消息只能由持有匹配私钥的人解密。这种方法用于确保机密性。
	- DIGITAL SIGNATURES: A message signed with a sender's private key can be verified by anyone who has access to the sender's public key, and, therefore, is likely to be the person associated with the public key used.
	  数字签名：由发送者的私钥签署的签名可以通过任何持有发送者公钥的人进行验证，因此很可能是与所用公钥关联的人。
- A central problem with public-key cryptography is proof that a particular public key is correct and has not been tampered with.
  公钥密码学的一个核心问题是证明某个特定的公钥是正确的并且未被篡改。
- The usual approach to this problem is to use a public-key infrastructure (PKI), in which one or more third parties-known as certificate authorities (CA) certify ownership of key pairs.
  解决这一问题的常见方法是使用公钥基础设施（PKI），其中一个或多个第三方（称为证书授权机构，CA）认证密钥对的所有权。

![[Pasted image 20250402164710.png#pic_75center|Public Key Encryption]]

![[Pasted image 20250402165122.png#pic_75center|Public Key Authentication]]

# Prime Numbers and MOD

- PRIME NUMBERS
	- Prime numbers only have divisors of 1 and self
	- they cannot be written as a product of other numbers
	- note: 1 is prime, but is generally not of interest
	- eg. 2,3,5,7 are prime, 4,6,8,9,10 are not.
- MOD:
	- Example 1:
		- 15 mod 20. Since 15 < 20, answer = 15 (i.e. 15 is remainder)
	- Example 2:
		- 320 MOD 9. Use MOD key on the calculator. If your calculator doesn’t have MOD key, you can use division $320/9=35.5555$. Now take the value after decimal point, which is $0.5555$ and multiply it with $9$. $0.5555\times 9=5$ This is the MOD value.

# Diffie-Hellman Key Exchange

![[Pasted image 20250402171847.png#pic_50center|]]

- It is a Public Key Algorithm only for Key Exchange and Does NOT Encrypt or Decrypt the message.
- The protocol is one of the most common encryption protocols in use today.
- In 2002, the inventor Martin Hellman suggested that it should be known as “Diffie–Hellman–Merkle” as it was based on a concept developed by Merkle.
- USED FOR
	- Electronic key exchange method of the Secure Sockets Layer (SSL) protocol
	- Enables the sharing of a secret key between two people who have not contacted each other before.
- Security is based on "Discrete Log Problem" $$y = f(x) = g^x (\mathrm{mod}\ p)$$
	- Given $g$, $x$, $p$ it is Easy to calculate $y$
	- Given $y$, $g$, $p$ it is Very Difficult to calculate $x$

- 这是一种公钥算法，仅用于密钥交换，不用于加密或解密消息。
- 该协议是当今最常用的加密协议之一。
- 2002 年，发明者马丁·赫尔曼建议将其称为“Diffie–Hellman–Merkle”，因为它基于默克尔提出的概念。
- **用途**
    - 安全套接字层（SSL）协议的电子密钥交换方法  
    - 允许两个未曾联系过的用户共享一个密钥 
- **安全性基于“离散对数问题”** $$y = f(x) = g^x (\mathrm{mod}\ p)$$
    - 已知 $g$、$x$、$p$ 时，计算 $y$ 很容易
    - 已知 $y$、$g$、$p$ 时，计算 $x$ 非常困难
---

- STEP 1 : GLOBAL PUBLIC ELEMENTS
	- Select any prime no : $q$
	- Calculate the primitive root of $q$: $a$ such that $a<q$
	  > **Primitive root**: A primitive root of a prime number $p$ is one whose powers generate all the integers from $1$ to $p-1$. （其他解释）使$a^d \equiv 1\ (\mathrm{mod}\ q)$成立的最小正整数$d$，若$d=\phi(q)$，则$d$是$q$的一个原根（其中$\phi(q)$是欧拉函数，表示小于等于$q$的正整数中与$q$互质的正整数的个数，如果$q$是质数则$\phi(q)=q-1$）
- STEP 2 : KEY GENERATION BY USER A
	- Select a random number as the private key $X_A$ where $X_A < q$
	- Calculate the public key $Y_A$ where $Y_A = a^{X_A}\ \mathrm{mod}\ q$
- STEP 3 : KEY GENERATION BY USER B
	- Select a random number as the private key $X_B$ where $X_B < q$
	- Calculate the public key $Y_B$ where $Y_B = a^{X_B}\ \mathrm{mod}\ q$
- STEP 4 : EXCHANGE THE PUBLIC KEY BETWEEN A & B
	- User A sends his/her public key to user B
	- User B sends his/her public key to user A
- STEP 5 : KEY GENERATION BY USER A
	- $K_A= Y_B^{X_A}\ \mathrm{mod}\ q$
- STEP 6: KEY GENERATION BY USER B
	- $K_B= Y_A^{X_B}\ \mathrm{mod}\ q$
- 能够发现$K_A=K_B$

- **步骤 1：全局公有元素**
    - 选择一个质数：$q$
    - 计算 $q$ 的原根：$a$，满足 $a < q$
- **步骤 2：用户 A 的密钥生成**
    - 选择一个随机数作为私钥 $X_A$，满足 $X_A < q$
    - 计算公钥 $Y_A$，其中 $Y_A = a^{X_A} \mod q$
- **步骤 3：用户 B 的密钥生成**
    - 选择一个随机数作为私钥 $X_B$，满足 $X_B < q$
    - 计算公钥 $Y_B$，其中 $Y_B = a^{X_B} \mod q$
- **步骤 4：A 与 B 交换公钥**
    - 用户 A 将其公钥发送给用户 B
    - 用户 B 将其公钥发送给用户 A
- **步骤 5：用户 A 计算密钥**
    - $K_A = Y_B^{X_A} \mod q$
- **步骤 6：用户 B 计算密钥**
    - $K_B = Y_A^{X_B} \mod q$
- 由此可发现 $K_A = K_B$

# RSA Algorithm

- Originally discovered by GCHQ in 1973 but kept secret
	- RSA = Rivest, Shamir, Adelman, published in 1978 (MIT professors)
	- Patented in 1983, expired in 2000. RSA, won 2002 Turing Award
	- RSA obtains its security from the difficulty of factoring large numbers
---
- RSA ALGORITHM - KEY GENERATION
	- Each user generates a public/private key pair by selecting two large primes at random $p$, $q$
	- Compute their products (called modulus) $N= p \times q$
	- Compute $z=(p-1)(q-1)$ this is also known as $\phi(N)=(p-1)(q-1)$
	- Select at random the encryption key $e$
		- $0 < e < \phi(N)$ (between 1 and φ(n))
		- $e$ should be a prime number
		- $e$, and $(p-1)$ and $(q-1)$ shouldn't have common factors
	- Solve following equation to find decryption key $d$
		- $e\times d\equiv 1\ \mathrm{mod}\ \phi(N)$
		- $0\leq d\leq N$
	- Publish the public encryption key $e$
	- Keep secret private decryption key $d$
---
- RSA USE
	- TO ENCRYPT A MESSAGE $M$, THE SENDER
		- Obtains public key of recipient $e$
		- Computes: $C=M^e\ \mathrm{mod}\ N$, where $0\leq M<N$
	- TO DECRYPT THE CIPHERTEXT $C$, THE OWNER
		- Uses their private key $d$
		- Computes: $M=C^d\ \mathrm{mod}\ N$
	- Note that the message $M$ must be smaller than the modulus $N$

# ELGAMAL

- It was designed by Taher Elgamal in 1985
- Based on original ideas of Diffie and Hellman
- Security based on assumed difficulty of discrete log
  安全性依赖于离散对数难题的假设复杂性
- Consists of both encryption and signature algorithms
  包含加密和签名算法
- Cipher text is twice the size of plain text
  密文的大小是明文的两倍
- It is slow

# Elliptic Curve Cryptography (ECC)

- In 1985, Neal Koblitz and Victor Miller - proposed using elliptic curves, however it only saw wide use in 2005
- Majority of public-key crypto (RSA, D-H) uses large numbers and imposes a significant load in storing and processing keys and messages
  大多数公钥加密（如RSA、D-H）使用大数，存储和处理密钥及消息的负担较重
- ECC on the other hand uses elliptic curves and offers same security with smaller bit sizes
  而ECC（椭圆曲线密码）使用椭圆曲线，以更小的位大小提供同样的安全性
- Even though RSA is still widely used, in recent times, ECC is becoming very popular, particularly after its use in crypto currencies
  尽管RSA仍被广泛使用，近年来ECC正变得非常流行，特别是在其被应用于加密货币之后
---
<center>同等加密强度下不同方法的密钥长度</center>

| 对称加密 | ECC | RSA   |
| :--: | :-: | :---: |
| 56   | 112 | 512   |
| 80   | 160 | 1024  |
| 112  | 224 | 2048  |
| 128  | 256 | 3072  |
| 192  | 384 | 7680  |
| 256  | 512 | 15360 |

# Public Key + Symmetric

![[Pasted image 20250402190747.png#pic_75center|]]

- PROBLEM: Public key systems are powerful but slow, while symmetric systems are inflexible but fast.
- SOLUTION: A hybrid system!
	- Sender generates random symmetric session key
	- Sender encrypts session key using **Public Key** crypto
	- Sender encrypts message using session key (and symmetric cipher)
- RESULT: A fast, flexible system
- HYBRID SCHEME
	- Combine advantages of symmetric and asymmetric ciphers
		- Throughput of symmetric cipher
		- Key management of asymmetric cipher
	- A two-stage approach is used
		- In the first step public key cryptography is used to share a session key.
		- Subsequently, the session key is used to encrypt the actual message.

# Summary

- Public-key solves the main issue of key distribution, where the sender and receiver uses two separate keys.
- Public-key is based on two keys:
	- A public key that can be made public and a private key, which has to be kept secret.
	  一个可以公开的公钥，以及一个必须保密的私钥
- Diffie-Hellman was the first protocol which showed how two parties can share a secrete key without compromising the security
  Diffie-Hellman是第一个展示如何在不妥协安全性的情况下让两方共享密钥的协议
- RSA is a complete system which includes key generations, encryption and decryption.
  RSA是一个完整的系统，包括密钥生成、加密和解密
- RSA is the most commonly used system for web security.
  RSA是用于网络安全的最常用系统
- Hybrid system is based on combining the both methods and is used for web security as SSL
  混合系统基于结合两种方法，用于网络安全，例如SSL
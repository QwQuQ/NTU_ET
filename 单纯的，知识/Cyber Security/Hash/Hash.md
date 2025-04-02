---
aliases:
  - 哈希
tags:
  - cyber_security
---

![[Pasted image 20250402195504.png#pic_75center|哈希]]

- A hashing algorithm is applied to a bit string of any length
  哈希算法应用于任意长度的位字符串
- It is designed in such a way that every bit in the message has some effect on the resulting message digest.
  它的设计使得消息中的每个位都会对生成的消息摘要产生影响
- The message digest can then be input to the Digital Signature Algorithm (DSA) which generates or verifies the signature for the message
  然后，消息摘要可以作为输入传递给数字签名算法（DSA），用于生成或验证消息的签名

---

![[Pasted image 20250403001841.png#pic_75center|一个很小的变化都会导致哈希值出现巨大的变化]]

- Properties
	- Can be applied to a block of data of any size
	- Produces a fixed-length output
	- $H(x)$ is relatively easy to compute for any given $x$
	- One-way or pre-image resistant 
	  单向性或抗原像性
		- Computationally infeasible to find $x$ such that $H(x) = h$
	- Computationally infeasible to find $y \neq x$ such that $H(y) = H(x)$
	- Collision resistant or strong collision resistance
	  抗碰撞性或强抗碰撞性
		- Computationally infeasible to find any pair $(x,y)$ such that $H(x) = H(y)$
		  （话说这俩应该是一个意思吧，虽然PPT上写了两行）

- A hashing function is a special mathematical function that performs one-way encryption.
  哈希函数是一种特殊的数学函数，用于执行单向加密
- Once the algorithm is processed, there is no feasible way to use the ciphertext to retrieve the plaintext.
  一旦算法处理完成，就无法通过密文以可行的方式还原明文
- There is no feasible way to generate two different plaintexts that compute to the same hash value.
  也无法以可行的方式生成两个不同的明文，使它们计算出相同的哈希值
- Two popular hash algorithms are the Secure Hash Algorithm (SHA) series and Message Digest (MD).
  两种常用的哈希算法是安全哈希算法（SHA）系列和消息摘要（MD）系列

---

- **Secure Hash Algorithm (SHA)**
	- Applies compression function to data input.
	- Accepts up to $2^{64}$ bits or less and then compresses it down to a smaller number of bits.
	- SHA-1: has been found to be vulnerable to a collision attack
	- SHA-2: These longer versions are referred to as SHA-2.
	- SHA-256, SHA-384, and SHA-512
		- All have longer hash results and are more difficult to attack successfully.
		- SHA-2 does require more processing power to compute the hash.

---

- **Message digest (MD)** is the generic version and work in the same manner as SHA.
- The MD algorithms were all developed by Ronald L. Rivest of MIT.
	- MD2, MD4 and MD5 (MD4 is obsolete)
	- MD5 (128-bit hashes)
	- SHA-1 (160-bit hashes)
	- SHA-224, SHA-256, SHA-384, and SHA-512 (name gives hash length in bits)
- Note: MD5 and SHA-1 should not be used because they have been shown to be unsecure.

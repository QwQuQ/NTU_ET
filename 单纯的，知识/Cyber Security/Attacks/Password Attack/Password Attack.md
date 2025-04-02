---
aliases:
  - 密码攻击
tags:
  - cyber_security
---


- It is a form of attack wherein a hacker cracks your password with various programs and password cracking tools like Aircrack, Cain, Abel, John the Ripper, Hashcat, etc., for illegal use.
  这是一种攻击形式，黑客使用各种程序和密码破解工具（如 Aircrack、Cain、Abel、John the Ripper、Hashcat 等）来破解您的密码，并进行非法使用。
- According to Microsoft report of 2022, there are an estimated 921 password attacks every second globally, which is 74% increase in just one year.
  根据微软2022年的报告，全球每秒估计发生921次密码攻击，这在短短一年内增加了74%。
- According to “Digital Defence Report 2022”,from July 2021 to June 2022, it blocked 34.7 billion password attack and 37 billion email threats.
  根据《数字防御报告2022》，从2021年7月至2022年6月，它共阻止了347亿次密码攻击和370亿次电子邮件威胁。

- Dictionary attack: Use every password that is possible through the dictionary
  字典攻击（Dictionary attack）：通过字典中的所有可能密码进行尝试，以破解密码。
- Brute force: Trial and error method used to decode the password or data
  暴力破解（Brute force）：通过反复尝试和错误的方法来解码密码或数据。
- Keylogger records all the hits on the keyboard
- Shoulder surfing: Attackers observe user’s keyboard by looking over the user’s shoulder
- Rainbow table: Attacker use hash tables to find the password of the user

# 破解密码用时

- Password choices = 95 printable ASCII characters
- Length of the password = 10 characters in length
- Password cracker rate = 6.4 millions operations per second $6.4\times 10^6$

- 可能的密码数量：$95^{10}\approx 6\times 10^{19}$
- 用时：$$\frac{6\times 10^{19}}{6.4\times 10^6}\approx 9.375\times 10^{12}(\mathrm{s})\approx 297000 年$$

# How to Prevent Password Attacks

- Listed below are a few ways to prevent password attacks:
	- Use strong alphanumeric passwords with special characters
	  使用包含特殊字符的强字母数字密码。
	- Refrain from using the same password for multiple websites or accounts.
	  避免在多个网站或账户上使用相同的密码。
	- Update your passwords (advisable to changed it every 90 days); this will limit your exposure to a password attack.
	  定期更新您的密码（建议每90天更换一次）；这样可以减少您遭受密码攻击的风险。
	- Do not have any password hints in the open.
	  不要公开显示任何密码提示。
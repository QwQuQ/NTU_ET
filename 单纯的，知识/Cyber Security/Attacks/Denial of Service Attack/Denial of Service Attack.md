---
aliases:
  - 拒绝服务攻击
tags:
  - cyber_security
---
- A Denial-of-Service (DoS) Attack is a significant threat to companies. Here, attackers target systems, servers, or networks and flood them with traffic to exhaust their resources and bandwidth or crashes their system.
  拒绝服务（DoS）攻击对公司构成重大威胁。在这里，攻击者以系统、服务器或网络为目标，向其注入大量流量，耗尽其资源和带宽，或使其系统崩溃。
- When this happens, catering to the genuine incoming requests becomes overwhelming for the servers, resulting in the website it hosts either shut down or slow down. This leaves the legitimate service requests unattended.
  当这种情况发生时，疲于应对的服务器无法响应真正的请求，导致其托管的网站要么关闭，要么速度减慢。这使得合法的服务请求无人值守。
- It is also known as a DDoS (Distributed Denial-of-Service) attack when attackers use multiple compromised systems to launch this attack.
  当攻击者使用多个受损系统发起这种攻击时，它也被称为DDoS（分布式拒绝服务）攻击。

- DDoS attacks can be categorized into mainly three categories
	- Volume bases Attacks: Work on saturating the target network's bandwidth with heavy volumes of traffic. Ping (ICMP) flood and UDP floods are two popular examples of this attack.
	  基于流量的攻击（Volume-based Attacks）：通过大量的流量来饱和目标网络的带宽。Ping（ICMP）和UDP洪水攻击是这种攻击的两个常见例子。

	- Protocol Attacks
	  > 在分布式拒绝服务（DDoS）攻击中，**协议攻击（Protocol Attacks）** 是一种利用网络通信协议中的弱点来破坏目标系统的攻击方式。这类攻击通常针对网络层和传输层协议，例如 TCP、UDP 和 ICMP。
	  > 常见的协议攻击包括：
	  > 	- **SYN Flood**：通过发送大量的半开连接请求（SYN 包）来耗尽服务器的资源。
	  > 	- **Ping of Death**：发送超大数据包导致目标系统崩溃。

	- Application Layer Attacks
	  > 在分布式拒绝服务（DDoS）攻击中，**应用层攻击（Application Layer Attacks）** 是一种针对应用层（如 HTTP、DNS、SMTP 等协议）的攻击方式。这类攻击旨在耗尽服务器的资源或使应用服务不可用，而不需要占用过多的带宽。
	  > 常见的应用层攻击包括：
	  > 	- **HTTP Flood**：发送大量合法的 HTTP 请求，导致目标服务器过载。
	  > 	- **DNS Query Flood**：向目标服务器发送大量的伪造 DNS 查询，导致服务器无法响应合法查询。

![[Pasted image 20250401164926.png#pic_75center|Simple DoS Attack]]

![[Pasted image 20250401165049.png#pic_75center|Distributed DoS (DDoS) Attack]]

# Classic DoS Attack (PING Attack)

- The simplest classical denial of service attack is a flooding attack on an organization.
  最简单的经典拒绝服务攻击是一种针对一个组织的流量洪水攻击。
- Can use simple flooding ping.
	- The attack might be as simple as using a flooding ping command directed at the target network.
	  攻击可能仅仅是使用针对目标网络的洪水 ping 命令
- From higher capacity link to lower
	- Can likely generate a higher volume of traffic than the lower capacity target connection can handle.
	  可能会生成超过低容量目标所能承受的高流量。
- Causing loss of traffic
  导致流量丢失
- Source of flood traffic easily identified.
	- Since its address is used as the source address in the ICMP echo request packets.
	  由于其地址被用作 ICMP 回显请求数据包中的源地址。
	- This has two disadvantages.
		- Firstly, since the source of the attack is identified, the attacker can be identified, and legal action taken in response.
		  首先，由于识别了攻击的来源，因此可以识别攻击者，并采取相应的法律行动。
		- Secondly, the targeted system will attempt to respond to the packets being sent.
		  其次，目标系统将尝试对发送的数据包做出响应。
- For that reason, usually spoofed address is used.
  因此，通常会使用伪造的地址。

![[Pasted image 20250401170009.png#pic_75center|]]

- Historically, attackers would often spoof in a bogus IP address in order to mask the sending device. With modern botnet attacks, the malicious actors rarely see the need to mask the bot’s IP, and instead rely on a large network of un-spoofed bots to saturate a target’s capacity.
  以前，攻击者经常会伪造一个IP地址来掩盖发送设备。在现代僵尸网络攻击中，黑客没必要伪造Bot的IP，而是依靠一个庞大的未被伪造的[[Malware Attack#Botnet|Botnet]]来饱和目标的容量。
- A network administrator can disable a device’s ability to send and receive any requests using the ICMP, however, in that case, all network activities that involve ICMP will also be disabled and the device will not responsive to any ping requests (including genuine requests).
  网络管理员可以通过禁用设备的ICMP（互联网控制消息协议）功能，使该设备无法发送或接收任何ICMP请求。然而，这种情况下，所有涉及ICMP的网络活动也会被禁用，该设备将不会对任何ping请求作出响应（包括真实的请求）。

## How Many Packets Are Needed?

- 网络带宽/包大小（记得分辨Byte和Bit）

# Protocol Based DDoS ATTACK

- This attack targets the networking layer of the target device.
- Types of protocol attack are Ping of Death (PoD) and SYN floods DDoS.

## Ping of Death (PoD)

> **Ping of Death (PoD)** 
> 虽然一些ping数据包很小，但是IP4 ping数据包要大得多，可以和最大允许数据包大小为65,535字节一样大。一些TCP / IP系统从未被设计为处理大于最大数据包的数据包，使得它们容易受到超过该大小的数据包的影响。
> 当恶意大数据包从攻击者发送到目标时，数据包将分段成分段，每个数据段都低于最大大小限制。当目标机器尝试将这些部分重新放在一起时，总数超过了大小限制，并且可能会发生[缓冲区溢出](https://zhida.zhihu.com/search?content_id=3898575&content_type=Article&match_order=1&q=%E7%BC%93%E5%86%B2%E5%8C%BA%E6%BA%A2%E5%87%BA&zhida_source=entity)，导致目标机器冻结，崩溃或重启。
- Most devices manufactured after 1998 are generally protected against PoD.
## SYN Flood Attack

> SYN Flood顾名思义就是用洪水一样的SYN报文进行攻击。SYN报文指的是TCP协议中的Synchronize报文，是TCP三次握手过程中的首个报文。

![[Pasted image 20250401171824.png#pic_75center|]]

- SYN flood attacks work by exploiting the handshake process of a TCP connection.
- Under normal conditions, TCP connection exhibits three distinct processes in order to make a connection.
	1. First, the client sends a SYN packet to the server in order to initiate the connection.
	2. The server than responds to that initial packet with a SYN/ACK packet, in order to acknowledge the communication.
	3. Finally, the client returns an ACK packet to acknowledge the receipt of the packet from the server.
- After completing this sequence of packet sending and receiving, the TCP connection is open and able to send and receive data.

- To create denial-of-service, an attacker exploits the fact that after an initial SYN packet has been received, the server will respond back with one or more SYN/ACK packets and wait for the final step in the handshake.
  为了制造拒绝服务攻击，攻击者利用了以下事实：在收到初始的SYN数据包后，服务器会响应一个或多个SYN/ACK数据包，并等待握手过程的最后一步完成。

![[Pasted image 20250401173801.png#pic_75center|]]

- Here’s how it works:
	1. The attacker sends a high volume of SYN packets to the targeted server, often with spoofed IP addresses.
	   攻击者向目标服务器发送高流量SYN包，通常使用伪造的IP地址
	2. The server then responds to each one of the connection requests and leaves an open port ready to receive the response.
	   服务器随后响应每个请求，然后预留一个打开的端口来准备接受回应
	3. While the server waits for the final ACK packet, which never arrives, the attacker continues to send more SYN packets.
	   当服务器等待最终不会被传输的ACK包时，攻击者继续发送更多SYN包
	4. The arrival of each new SYN packet causes the server to temporarily maintain a new open port connection for a certain length of time, and once all the available ports have been utilized the server is unable to function normally.
	   每个新SYN包都将导致服务器暂时打开更新的端口一段时间，当所有可用端口用尽时这个服务器将无法正常工作。

# Application Layer DDoS Attack

- These attacks are sophisticated and focus on crashing the web servers.
  这些攻击非常复杂，旨在使网络服务器崩溃
## HTTP Flood Attack

![[Pasted image 20250401174028.png#pic_75center|HTTP Flood Attack]]

- HTTP flood attack is designed to overwhelm a targeted server with HTTP requests. Once the target has been saturated with requests and is unable to respond to normal traffic, denial-of-service will occur for additional requests from actual users.
  HTTP洪水攻击旨在通过大量的HTTP请求来压垮目标服务器。一旦目标服务器被请求淹没，无法响应正常的流量，实际用户的额外请求将会导致拒绝服务的发生。
	- **HTTP GET/Post Attack**: Multiple computers or other devices are coordinated to send/request multiple requests for images, files, or some other asset from a targeted server until it capacity is saturated.
	  **HTTP GET/Post攻击**：通过协调多台计算机或其他设备，从目标服务器发送或请求多个图像、文件或其他资源的请求，直到目标服务器的处理能力被完全饱和为止。

## DNS Flood Attack

![[Pasted image 20250401174258.png#pic_75center|DNS Flood Attack]]

- The function of the Domain Name System (DNS) is to translate between easy to remember names (e.g., example.com) and hard to remember addresses of website servers (e.g., 192.168.0.1), so successfully attacking DNS infrastructure makes the Internet unusable for most people.
  域名系统 (DNS) 的功能是将易于记忆的名称（例如：example.com）翻译为网站服务器难以记忆的地址（例如：192.168.0.1）。因此，成功攻击DNS基础设施会导致大多数人无法正常使用互联网。
- A DNS flood is DDoS attack where an attacker floods a particular domain’s DNS servers to disrupt DNS resolution for that domain.
  DNS泛洪是一种分布式拒绝服务（DDoS）攻击，攻击者通过向某个域的DNS服务器发送大量请求来导致该域的DNS解析功能中断。
- DNS flood attacks use the high bandwidth connections of IP cameras, DVR boxes and other IoT devices to directly overwhelm the DNS provider’s services. The only way to withstand these types of attacks is to use a very large and highly distributed DNS system that can monitor, absorb, and block the attack traffic in real time.
  DNS泛洪攻击利用IP摄像机、DVR设备和其他物联网（IoT）设备的高带宽连接，直接压垮DNS提供商的服务。应对这类攻击的唯一方法是使用一个非常庞大且高度分布式的DNS系统，该系统可以实时监控、吸收并阻止攻击流量。
# How to Prevent DDoS Attack

![[Pasted image 20250401175039.png#pic_75center|用于过滤的地方]]

- Let’s now look at how to prevent a DDoS attack:
	- Run a traffic analysis to identify malicious traffic.
	  进行流量分析，以识别恶意流量。
	- Understand the warning signs like network slowdown, intermittent website shutdowns, etc. At such times, the organization must take the necessary steps without delay.
	  了解警告信号，例如网络速度变慢、网站间歇性关闭等。在这些情况下，组织必须立即采取必要措施。
	- Formulate an incident response plan, have a checklist and make sure your team and data center can handle a DDoS attack.
	  制定事件响应计划，准备检查清单，并确保您的团队和数据中心能够应对DDoS攻击。
	- Outsource DDoS prevention to cloud-based service providers (Cloudflare, NETSCOUT, Akamai, AWS, etc.).
	  将DDoS防护外包给基于云的服务提供商（如Cloudflare、NETSCOUT、Akamai、AWS等）。
---
aliases:
  - 防火墙
tags:
  - cyber_security
  - TODO
---

![[Pasted image 20250403041507.png#pic_75center|]]
![[Pasted image 20250403041514.png#pic_75center|]]

- A Firewall is a network security device/software that monitors and filters incoming and outgoing network traffic based on an organization’s previously established security policies.
  防火墙是一个网络安全设备/软件，它根据组织预先设定的安全政策监控和过滤进出网络的流量。
- At its most basic, a firewall is essentially the barrier that sits between a private internal network and the public Internet.
  从最基本的层面上讲，防火墙本质上是一个位于私人内部网络和公共互联网之间的屏障。
- A firewall’s main purpose is to allow non-threatening traffic in and to keep dangerous traffic out.
  防火墙的主要目的是允许无威胁的流量通过，同时阻止危险的流量进入。

- A firewall is hardware or software (or a combination of hardware and software) that monitors the transmission of packets of digital information that attempt to pass through the perimeter or a network.
  防火墙可以是硬件、软件（或硬件和软件的组合），用于监控试图通过网络边界的数据包传输。
- HARDWARE FIREWALLS
	- Protect an entire network
	  保护整个网络
	- Implemented on the router level
	  在路由层实施
	- Usually more expensive, harder to configure
	  通常更昂贵，配置更复杂
- SOFTWARE FIREWALLS
	- Protect a single computer
	  保护单台计算机
	- Usually less expensive, easier to configure
	  通常更便宜，配置更简单
- HOW DOES A SOFTWARE FIREWALL WORK?
	- Inspects each individual “packet” of data as it arrives at either side of the firewall (Inbound to or outbound from your computer)
	  在数据包到达防火墙的任一侧时（从电脑入站或出站），逐个检查每个数据包。
	- Determines whether it should be allowed to pass through or if it should be blocked
	  决定是否允许数据包通过或将其阻止。

- Advantages of Firewalls
	- **Enhanced Security**: Blocks unauthorized access and cyberattacks.
	  **增强安全性**：阻止未经授权的访问和网络攻击。
	- **Traffic Filtering**: Controls which data packets are allowed into the network.
	  **流量过滤**：控制哪些数据包被允许进入网络
	- **Logging & Alerts**: Provides administrators with logs of suspicious activity.
	  **日志记录与警报**：为管理员提供可疑活动的日志
- Disadvantages of Firewalls
	- **Performance Impact**: Can slow down network speed due to traffic inspection.
	  **性能影响**：由于流量检查可能会降低网络速度
	- **Complex Configuration**: Requires expertise to set up and maintain effectively.
	  **配置复杂**：需要专业知识才能有效设置和维护
	- **No Protection Against Insider Threats**: Firewalls cannot stop attacks from internal users.
	  **无法防范内部威胁**：无法阻止来自内部用户的攻击
	- **Bypass Risk**: Attackers can use techniques like tunneling or encrypted threats to evade detection.
	  **规避风险**：攻击者可能使用隧道或加密威胁等技术逃避检测
	- **Limited Defense Against Advanced Attacks**: Cannot protect against social engineering or zero-day exploits.
	  **对高级攻击的防护有限**：无法防御社会工程攻击或零日漏洞攻击

# Keeping Worms and Crankers Out

- When you request something from the internet, the firewall pretends that it made the request, not your computer.
  当您从互联网请求内容时，防火墙会伪装成是它发出的请求，而不是您的计算机发出的
- Since the internet never even sees your computer, there’s nothing for the worms or crackers to probe or attack other than your firewall.
  由于互联网甚至无法看到您的计算机，因此蠕虫或黑客无法对您的计算机进行探测或攻击，唯一的攻击目标是防火墙
- And your firewall is just a dumb box.
  而您的防火墙只是一个“笨盒子”

# Firewall Policies

![[Pasted image 20250403181714.png#pic_75center|]]

- To protect private networks and individual machines from the dangers of the greater Internet, a firewall can be employed to filter incoming or outgoing traffic based on a predefined set of rules called firewall policies.
  为了保护私有网络和个人计算机免受更大范围互联网的威胁，可以使用防火墙根据一组预定义的规则（称为防火墙策略）来过滤进出网络的流量。
- Think of IP addresses as houses, and port numbers as rooms within the house. Only trusted people (source addresses) are allowed to enter the house (destination address) at all—then it’s further filtered so that people within the house are only allowed to access certain rooms (destination ports), depending on if they're the owner, a child, or a guest. The owner is allowed to any room (any port), while children and guests are allowed into a certain set of rooms (specific ports).
  将 IP 地址比作房屋，将端口号比作房屋内的房间。只有被信任的人（源地址）才被允许进入房屋（目标地址）——然后会进一步过滤，确保进入房屋的人只能访问特定的房间（目标端口），具体取决于他们是房主、孩子还是客人。房主可以进入任何房间（任意端口），而孩子和客人只能进入特定的一组房间（特定端口）。

# Personal Firewall

- A personal firewall (sometimes called a desktop firewall) is a software application used to protect a single Internet-connected computer from intruders
  个人防火墙（有时称为桌面防火墙）是一种用于保护单台连接互联网的计算机免受入侵的软件应用程序
- WHAT A PERSONAL FIREWALL CAN DO
	- Stop hackers from accessing your computer
	  阻止黑客访问您的计算机
	- Protects your personal information
	  保护您的个人信息
	- Blocks “pop up” ads and certain cookies
	  阻止“弹出”广告和某些 Cookies
	- Determines which programs can access the Internet
	  决定哪些程序可以访问互联网
- WHAT A PERSONAL FIREWALL CANNOT DO
	- Cannot prevent e-mail viruses
	  无法防止电子邮件病毒
	- Only an antivirus product with updated definitions can prevent e-mail viruses
	  只有具有更新病毒定义的杀毒软件才能防止电子邮件病毒
	- After setting it initially, you can forget about it
	  初次设置后，您可以不再操心
	- The firewall will require periodic updates to the rule sets and the software itself
	  防火墙需要定期更新规则集和软件本身

# Packet Filtering Firewall

![[Pasted image 20250403183448.png#pic_75center|]]

- Examines individual packets based on IP address, port, and protocol.
  基于 IP 地址、端口和协议检查单个数据包
- Fast and efficient but lacks deep inspection capabilities.
  快速高效，但缺乏深度检查功能

---

- Packet filtering firewalls is low cost and low impact on network performance
  包过滤防火墙成本低，对网络性能的影响小。
- Three subsets of packet filtering firewalls
  包过滤防火墙的三个子集
	- STATIC FILTERING: If a packet matches the packet filter's set of rules, the packet filter will drop or accept it.
	  **静态过滤**：如果数据包与包过滤器的规则集匹配，包过滤器将丢弃或接受该数据包
	- DYNAMIC FILTERING: Allows firewall to react to emergent event and update or create rules to deal with event by understanding how the protocol functions, based on information in the packet header.
	  **动态过滤**：允许防火墙通过理解协议功能，根据数据包头信息对突发事件作出反应，并更新或创建规则以应对事件
	- STATEFUL INSPECTION: Firewalls that keep track of each network connection between internal and external systems using a state table.
	  **状态检测**：利用状态表跟踪内部和外部系统之间的每个网络连接的防火墙

## Static Packet Filtering Firewall

![[Pasted image 20250403183341.png#pic_75center|]]

- This was the earliest firewall filtering mechanism.
  这是最早的防火墙过滤机制
- Examines packets one at a time, in isolation.
  单独逐个检查数据包
- Only looks at some internet and transport headers.
  仅查看部分互联网和传输头信息
- Consequently, unable to stop many types of attacks.
  因此，无法阻止许多类型的攻击
- It can stop attacks Packets with spoofed IP addresses.
  可以阻止伪造 IP 地址的数据包攻击
- No longer used as the main filtering mechanism for border firewalls.
  不再作为边界防火墙的主要过滤机制使用
- May be used as a secondary filtering mechanism on main border firewalls.
  可能作为主要边界防火墙的辅助过滤机制使用

## Stateful Inspection Firewall

- Monitors active connections and tracks the state of network traffic.
- More secure than packet filtering but requires more resources.

---

- **Stateful Packet Inspection Firewalls (SPI)**: Reviews the same packet information but also records information about TCP connections.
  **状态包检测防火墙 (SPI)**：检查与普通数据包相同的信息，但还记录有关 TCP 连接的信息。
- Keeps track of each network connection established between internal and external systems using a state table.
  使用状态表跟踪内部和外部系统之间建立的每个网络连接
- Tracks the state and context of each packet in the conversation by recording which station sent what packet and when.
  通过记录每个数据包的状态和上下文，包括哪个站点何时发送了哪个数据包，跟踪会话中的每个数据包
- SPI firewalls can tell when packets are part of legitimate sessions originating within a trusted network.
  SPI 防火墙可以识别数据包是否属于可信网络内发起的合法会话
- SPI firewalls maintain tables containing information on each active connection, including the IP addresses, ports, and sequence numbers of packets.
  SPI 防火墙维护包含每个活动连接的信息的表格，包括数据包的 IP 地址、端口和序列号
- Using these tables, SPI can allow only inbound TCP packets that are in response to a connection initiated from within the internal network.
  通过使用这些表格，SPI 可以仅允许响应由内部网络发起的连接的入站 TCP 数据包
- **Primary disadvantage**: Additional processing requirements of managing and verifying packets against the state table which can possibly expose the system to a [[Denial of Service Attack]]
  **主要缺点**：管理和验证数据包与状态表的附加处理要求，可能会使系统暴露于[[Denial of Service Attack|拒绝服务攻击]]的风险之中

### Perspective on SPI Firewall

- LOW COST
	- Most packets are not part of packet-opening attempts
	  大多数数据包不是连接尝试的一部分
	- These can be handled very simply and therefore inexpensively
	  这些数据包可以非常简单地处理，因此成本较低
	- Connection-opening attempt packets are more expensive process but are rare
	  连接尝试的数据包处理成本较高，但出现频率较低
- SAFETY
	- Attacks other than application-level attacks usually fail to get through SPI firewalls
	  除了应用级攻击以外的攻击通常无法通过 SPI 防火墙
	- In addition, SPI firewalls can use other forms of filtering when needed
	  此外，SPI 防火墙在需要时可以使用其他形式的过滤
- DOMINANCE
	- The combination of high safety and low cost makes SPI firewalls extremely popular
	  高安全性与低成本的结合使 SPI 防火墙非常受欢迎
	- Nearly all main border firewalls today use Stateful packet inspection
	  当今几乎所有主要边界防火墙都使用状态包检测技术

### States in Connection

![[Pasted image 20250403184102.png#pic_75center|]]

- Connections have distinct states or stages
  连接具有不同的状态或阶段
- Different states are subject to different attacks
  不同的状态会受到不同类型攻击的威胁
- SPI firewalls use different filtering rules for different states
  SPI 防火墙针对不同状态使用不同的过滤规则

![[Pasted image 20250403184221.png]]

# Proxy Firewall

- Acts as an intermediary between users and the internet.
  充当用户与互联网之间的中介
- Provides strong security but can slow down network performance.
  提供强大的安全性，但可能会降低网络性能

## Application Gateway/Proxy Servers

- Frequently installed on a dedicated computer; also known as a proxy server
  通常安装在专用计算机上；也称为代理服务器
- Since proxy server is often placed in unsecured area of the network (e.g., DMZ), it is exposed to higher levels of risk from less trusted networks
  由于代理服务器通常位于网络的不安全区域（例如 DMZ），因此会面临来自较不可信网络的更高风险
- With this configuration the proxy server, rather than the Web server, is exposed to the outside world.
  在这种配置下，代理服务器而不是 Web 服务器暴露给外界
- Additional filtering routers can be implemented behind the proxy server.
  可以在代理服务器后实施额外的过滤路由器
- Gateway that is configured to be a web proxy will not allow any ftp, gopher, telnet or other traffic through.
  配置为 Web 代理的网关不会允许任何 ftp、gopher、telnet 或其他流量通过
- Has full access to protocol
  具有完整的协议访问权限
	- User requests service from proxy.
	  用户向代理请求服务
	- Proxy validates request as legal.
	  代理验证请求是否合法
	- Then actions request and returns result to user.
	  然后执行请求并将结果返回给用户
- Tends to be more secure than packet filters
  通常比包过滤更安全
	- Need only scrutinize a few allowable apps.
	  只需检查少数允许的应用程序
	- Easy to log and audit all incoming traffic.
	  易于记录和审计所有进入的流量

# Next-Generation Firewall (NGFW)

- Many of the most recently-released firewall products are being touted as “next-generation” architectures. However, there is no one definition of a next-generation firewall.
- Includes traditional firewall features plus intrusion prevention, deep packet inspection (DPI), and application awareness.
- More advanced but also more expensive.

# Cloud-Based Firewall

- Hosted on cloud infrastructure, providing scalable protection for remote users.
- Reduces on-premises hardware dependency but relies on thirdparty services.

# Web Application Firewall (WAF)

- Protects web applications from threats like SQL injection and cross-site scripting (XSS).
- Focused on application security rather than general network protection.

# Firewall Architectures

*老师你在写什么登西*

- Firewall devices can be configured in a number of network connection architectures
  防火墙设备可以配置为多种网络连接架构
- Best configuration depends on three factors:
  最佳配置取决于以下三个因素
	- Objectives of the network
	  网络的目标
	- Organization’s ability to develop and implement architectures
	  组织开发和实施架构的能力
	- Budget available for function
	  用于该功能的预算

- Four common architectural implementations of firewalls:
  四种常见的防火墙架构实现：包过滤路由器、屏蔽主机防火墙、双宿主防火墙、屏蔽子网防火墙
	- **Packet Filtering Routers**
	- **Screened Host Firewalls**
	- **Dual-Homed Firewalls**
	- **Screened Subnet Firewalls**

## Packet Filtering Routers

![[Pasted image 20250403190443.png#pic_75center|]]

- Most organizations with Internet connection have a router serving as interface to Internet
  大多数与互联网连接的组织都有一个充当互联网接口的路由器
- Many of these routers can be configured to reject packets that organization does not allow into network
  许多这样的路由器可以配置为拒绝组织不允许进入网络的数据包
- Drawbacks include a lack of auditing and strong authentication
  缺点包括缺乏审计功能和强身份验证

## Screened Host Architecture

- Combines packet filtering router with separate, dedicated firewall such as an application proxy server
  结合包过滤路由器与单独的专用防火墙（例如应用代理服务器）
- Allows router to prescreen packets to minimize traffic/load on internal proxy
  允许路由器预筛选数据包，以最大限度地减少内部代理的流量负载

![[Pasted image 20250403190936.png#pic_75center|Single Host Architecture]]

- **Single Host Architecture**
  **单主机结构**
	- A single firewall is placed between the internal network and the internet.
	  在内部网络和互联网之间放置一个防火墙
	- Simple but vulnerable if the firewall is compromised.
	  简单但如果防火墙被攻破，则易受攻击
	- Separate host (referred to as bastion host or sacrificial host), and can be target for external attacks and should be very thoroughly secured.
	  独立的主机（称为堡垒主机或牺牲主机）可能成为外部攻击的目标，需非常彻底地进行安全防护

![[Pasted image 20250403191428.png#pic_75center|]]

- **Dual-Homed Host Architecture**
  **双宿主主机结构**
	- A firewall with two network interfaces: one connected to the internet and the other to the internal network.
	  拥有两个网络接口的防火墙：一个连接互联网，另一个连接内部网络
	- More secure than a screened host but still a single point of failure.
	  比屏蔽主机更安全，但仍然存在单点故障问题

## Screened-Subnet Firewalls

![[Pasted image 20250403192533.png#pic_75center|]]

- Uses two firewalls to create a demilitarized zone (DMZ) where public-facing services (e.g., web servers) are placed.
  使用两个防火墙创建一个非军事区（DMZ），将面向公众的服务（例如 Web 服务器）置于其中
  > DMZ 的全称是“Demilitarized Zone”（非军事区），在网络安全中是指一个用于公开访问的子网，其主要目的是将外部访问和内部网络隔离开来。DMZ 部署在内部网络和外部网络（如互联网）之间，用来放置需要被外界访问的服务器，如邮件服务器、Web 服务器等。通过这种隔离，能更好地保护内部网络免受外部的直接攻击。
- Provides an additional security layer by isolating internal systems from the internet.
  提供额外的安全层，通过隔离内部系统与互联网来增强安全性

- ADVANTAGES
	- There are now three levels of defense to thwart intruders.
	  现在有三层防御措施来阻止入侵者
	- The outside router advertises only the existence of the screened subnet to the Internet; therefore, the internal network is invisible to the Internet.
	  外部路由器仅向互联网广播屏蔽子网的存在，因此内部网络对互联网不可见
	- Similarly, the inside router advertises only the existence of the screened subnet to the internal network; therefore, the systems on the inside network cannot construct direct routes to the Internet.
	  同样，内部路由器仅向内部网络广播屏蔽子网的存在，因此内部网络的系统无法直接构建到互联网的路由
	- Firewalls are essential for cybersecurity, but they must be complemented by other security measures like intrusion detection systems (IDS) and endpoint protection.
	  防火墙是网络安全的关键，但必须结合其他安全措施，例如入侵检测系统（IDS）和终端保护
	- Organizations should choose the appropriate firewall type and architecture based on their security needs, network size, and budget.
	  组织应根据其安全需求、网络规模和预算选择适当的防火墙类型和架构
	- Firewalls alone cannot prevent all cyber threats; a layered security approach is necessary.
	  单独的防火墙无法防御所有网络威胁，需要采用分层的安全策略

# The Death of the Perimeter in Firewall Security

- The Traditional Perimeter-Based Security Model
- Traditionally, firewalls acted as the main defense at the network perimeter based on the assumption that everything inside the corporate network is trusted, and everything outside is a potential threat. However, the concept of a fixed security perimeter has eroded due to several factors:
  传统上，防火墙作为网络边界的主要防御机制，基于的假设是公司网络内部的所有内容都是可信的，而外部的所有内容都是潜在的威胁。然而，由于以下几个因素，固定的安全边界概念逐渐被削弱：
	1. Cloud Computing
		- Organizations now store data in cloud environments (AWS, Azure, Google Cloud) instead of on-premises servers.
		  组织现在将数据存储在云环境（如 AWS、Azure、Google Cloud）中，而不是本地服务器上
		- Employees access corporate resources from anywhere, bypassing traditional firewalls.
		  员工可以从任何地方访问企业资源，从而绕过传统防火墙
	2. Remote Work & BYOD (Bring Your Own Device)
		- Employees use personal devices and home networks to access corporate data.
		  员工使用个人设备和家庭网络访问企业数据
		- Traditional firewalls can't enforce security policies on remote users effectively.
		  传统防火墙无法有效执行对远程用户的安全政策
	3. Zero Trust Security Model
		- "Never trust, always verify" replaces the old perimeter-based trust model.
		  “永不信任，总是验证”取代了旧有的基于边界的信任模型
		- Access is granted based on identity, context, and least privilege rather than network location.
		  访问是基于身份、上下文和最小权限授予的，而不是基于网络位置
	4. Increased Use of Encrypted Traffic (TLS/SSL)
		- Many cyberattacks now use encryption, making it harder for firewalls to inspect traffic.
		  许多网络攻击现在利用加密技术，这使得防火墙很难检查流量
		- Attackers use techniques like SSL/TLS tunneling to bypass traditional firewalls.
		  攻击者使用诸如 SSL/TLS 隧道等技术绕过传统防火墙
	5. Rise of Sophisticated Threats
		- Malware and hackers now infiltrate networks through phishing, insider threats, and compromised credentials.
		  恶意软件和黑客通过网络钓鱼、内部威胁和被盗凭据渗透网络
		- Attackers often gain access inside the network, rendering perimeterbased firewalls ineffective.
		  攻击者通常能够获得网络内部的访问权限，从而使基于边界的防火墙变得无效

# Do We Still Need a Firewall?

- The Perimeter Has Shifted, Not Disappeared
	- The idea that the network perimeter has "died" is somewhat misleading. Instead, the perimeter has become dynamic and decentralized.
	  关于网络边界“消亡”的说法有些误导。实际上，边界已经变得动态化和去中心化
	- This means a single firewall at the network edge is no longer enough to secure corporate assets.
	  这意味着仅靠网络边缘的单个防火墙不足以保护企业资产的安全
	- Firewalls Are Still Essential, But Must Adapt
	  防火墙仍然至关重要，但必须适应变化
- Firewalls Are Evolving, Not Dying
	- Firewalls are still a critical part of cybersecurity, but they are no longer the only line of defense.
	  防火墙仍然是网络安全的关键部分，但它不再是唯一的防线
	- Organizations should not abandon firewalls but rather integrate them with modern security strategies like Zero Trust, endpoint security, and cloud security.
	  组织不应放弃防火墙，而是应将其与现代安全策略（如零信任、终端安全和云安全）结合起来
	- The perimeter has shifted from a fixed location to a fluid, identity-based model, where access and security policies follow users, devices, and data instead of being tied to a physical network.
	  边界已从固定位置转变为动态的、基于身份的模型，访问权限和安全策略跟随用户、设备和数据，而不再依赖于物理网络

# Selecting the Right Firewall

- What type of firewall technology offers the right balance of protection features and cost for the needs of the organization?
  什么类型的防火墙技术能够在保护功能和成本之间为组织的需求提供最佳平衡？
- What features are included in the base price? What features are available at extra cost? Are all cost factors known?
  基础价格中包含哪些功能？哪些功能需要额外付费？是否已知所有的成本因素？
- How easy is it to set up and configure the firewall? How accessible are staff technicians with the mastery to do it well?
  防火墙的设置和配置有多容易？是否可以轻松找到熟练的技术人员来妥善完成此任务？
- Can the candidate firewall adapt to the growing network in the target organization?
  候选防火墙能否适应目标组织不断增长的网络？

---

- CONFIGURING AND MANAGING FIREWALLS
  配置和管理防火墙
	- Each firewall device will have its own set of configuration rules that regulate its actions.
	  每个防火墙设备都有一套自己的配置规则来调节其操作
	- Simple mistakes can turn the device into a choke point.
	  简单的错误可能会将设备变成一个瓶颈
	- When security rules conflict with the performance of business, security loses since organizations are much more willing to live with a potential risk than a certain failure.
	  当安全规则与业务性能发生冲突时，安全通常会让步，因为组织更愿意接受潜在风险而非确定性的失败

## Recommended Practices

- All traffic from the trusted network is allowed out.
  来自可信网络的所有流量都被允许外出
- The firewall device is always inaccessible directly from the public network.
  防火墙设备始终无法直接从公共网络访问
- Allow Simple Mail Transport Protocol (SMTP) data to pass through your firewall, but insure it is all routed to a well-configured SMTP gateway to filter and route messaging traffic securely.
  允许简单邮件传输协议 (SMTP) 数据通过防火墙，但确保所有数据都被路由到一个配置良好的 SMTP 网关，以安全地过滤和路由消息流量
- All Internet Control Message Protocol (ICMP) data should be denied.
  所有互联网控制消息协议 (ICMP) 数据都应被拒绝
- Block telnet (terminal emulation) access to all internal servers from the public networks.
  阻止从公共网络对所有内部服务器的 Telnet（终端仿真）访问
- When Web services are offered outside the firewall, deny HTTP traffic from reaching your internal networks by using some form of proxy access or DMZ architecture.
  当 Web 服务在防火墙外提供时，使用某种代理访问或 DMZ 架构来阻止 HTTP 流量到达您的内部网络

- TRADEOFF
	- Degree of communication with outside world, level of security!
	  与外界的通信程度与安全水平之间的平衡！
	- Remember many highly protected sites still suffer from attacks.
	  请记住，即使是高度保护的网站仍然可能受到攻击

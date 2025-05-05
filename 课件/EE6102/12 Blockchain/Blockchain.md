# Computer Technology

![[Pasted image 20250504163444.png#pic_50center|]]

- Mainframe Computers (Centralized computing Power)
  大型机（集中式计算能力）
	- Typically housed all computing power, memory, data storage, and code.
	  通常包含所有计算能力、内存、数据存储和代码。
	- Access to mainframes was mainly by 'dumb terminals', which only take inputs and outputs, and do not store or process data.
	  访问大型机主要通过“哑终端”进行，这些终端仅用于输入和输出，不存储或处理数据。
- Client-Server (Distributed computing Power)
  客户端-服务器（分布式计算能力）
	- With the advent of personal computers and private networks, similar computational capabilities were now housed both on the clients, as well as the servers.
	  随着个人计算机和私有网络的出现，类似的计算能力现在既存在于客户端，也存在于服务器上。
	- This, in part, gave rise to the 'client-server' architecture, which supported the development of relational database systems.
	  这部分促成了“客户端-服务器”架构的发展，支持了关系型数据库系统的建立。
- Peer-to-Peer (Decentralized computing power)
  点对点（P2P，去中心化计算能力）
	- In its simplest form, a peer-to-peer (P2P) network is created when two or more PCs are connected and share resources without going through a separate server computer.
	  在最简单的形式下，点对点（P2P）网络是由两个或多个计算机连接而成，资源可以共享，而无需通过独立的服务器计算机。
	- P2P networks are generally considered to be more secure than centralized networks, as they do not have a single point of attack.
	  P2P网络通常被认为比集中式网络更安全，因为它们没有单一的攻击点。

## Distributed Ledger: Where Technological Revolution Starts

- More than 5000 years ago, clay tablets were used as a record keeping centralized ledger.
  5000多年前，泥板被用作记录保存的集中式账本
- But about 700 years ago, a newer kind of centralized ledger system emerged in northern Italy. Here, merchants tried to accomplish a logical connection between all the entries. Every item on the centralized ledger would have a debit and credit entry.
  但大约700年前，在意大利北部出现了一种较新的集中式账本系统。商人们试图在所有条目之间建立逻辑连接。账本上的每个项目都会有借方和贷方的记录
- In the 1980s and 90s computer system started to take over the typical banking centralized digital ledger systems.
  在20世纪80年代和90年代，计算机系统开始接管传统的银行集中式数字账本系统
- In 2009, Satoshi Nakamoto introduced the first distributed ledger technology, and this is how the revolutionary decentralized ledger technology came into being.
  2009年，中本聪推出了第一种分布式账本技术，这便是革命性的去中心化账本技术的诞生
- A distributed ledger is a form of digital database that is updated and held by every member independently in a large network space.
  分布式账本是一种数字数据库，在大型网络空间中由每个成员独立更新和维护
- In this type of ledger there’s isn’t any central authority to broadcast the records to every member. Instead, all the nodes will hold the ledger and construct it independently.
  在这种账本中，没有中央权威机构向每个成员广播记录。相反，所有节点都持有账本，并独立构建它

# Introduction to Blockchain

- Blockchain is a decentralized and distributed digital ledger technology that records transactions in a secure, immutable, and transparent manner. It eliminates the need for a central authority, enhancing trust and security.
  区块链是一种去中心化和分布式的数字账本技术，以安全、不可更改和透明的方式记录交易。它消除了对中央权威的需求，增强了信任和安全性
- Key Characteristics
	- Decentralization: No single entity controls the network, reducing risks of corruption and central points of failure.
	  去中心化：没有单一实体控制网络，降低了腐败和中心故障的风险
	- Transparency: All transactions are visible to participants, increasing accountability.
	  透明性：所有交易对参与者都是可见的，提高了问责性
	- Immutability: Once recorded, transactions cannot be altered or deleted, ensuring data integrity.
	  不可变性：一旦记录，交易无法更改或删除，确保数据完整性
	- Security: Uses cryptographic techniques, such as hashing and digital signatures, to ensure transaction authenticity.
	  安全性：使用加密技术，如哈希和数字签名，以确保交易的真实性
	- Consensus Mechanisms: Ensures that all nodes in the network agree on the validity of transactions.
	  共识机制：确保网络中的所有节点就交易的有效性达成一致
	- Structure: A block consists of transaction data, and are cryptographically linked to form a chain, making data tamper-proof.
	  结构：一个区块包含交易数据，并以加密方式链接形成区块链，使数据防篡改

- Blockchain is a system comprised of: 
	- Transactions
	  交易
	- Immutable ledgers
	  不可变账本
	- Decentralized peers
	  去中心化节点
	- Encryption processes
	  加密过程
	- Consensus mechanisms
	  共识机制
	- Optional Smart Contracts
	  可选的智能合约
- Transactions
	- The record of an event, cryptographically secured with a digital signature, that is verified, ordered, and bundled together into blocks, form the transactions in the Blockchain. In the Bitcoin, Blockchain transactions involve the transfer of bitcoins, while other Blockchain, transactions may involve the transfer of any asset, or a record of some service being rendered.
	  事件的记录，经过数字签名的加密保护，被验证、排序并捆绑到区块中，构成区块链中的交易。在比特币区块链中，交易涉及比特币的转移，而在其他区块链中，交易可能涉及任何资产的转移或某项服务的记录。

# Blockchain

![[Pasted image 20250504175804.png#pic_75center|]]
- As with enterprise transactions today, Blockchain is a historical archive of decisions and actions taken
  与当今的企业交易一样，区块链是一个记录决策和行动的历史档案
- Proof of history, provides provenance
  历史证明提供了溯源能力
- Immutable
  不可变性
	- 'unchanging over time’. Once a transaction is written onto the Blockchain, no one can change it, or, at least, it would be extremely difficult to change it.
	  “随时间不变”。一旦交易被写入区块链，任何人都无法更改，或者至少极难更改
	- The transaction is, immutable
	  交易是不可变的
	- Like a ledger written in ink, an error would be resolved with another entry
	  就像用墨水书写的账本，错误将通过另一个条目来解决
![[Pasted image 20250504175830.png#pic_25center|Legacy Network Centralized DB]]
![[Pasted image 20250504175933.png#pic_25center|Blockchain Network Distributed Ledgers]]
- Decentralized Peers
  去中心化节点
	- Rather than the centralized “Hub” type of network, Blockchain is a decentralized peer to peer network. Where each NODE has a copy of the ledger.
	  与集中式“中心”类型的网络不同，区块链是一个去中心化的点对点网络。其中，每个节点都持有账本副本
- Encryption
  加密
	- All blocks are encrypted
	  所有区块均经过加密
	- Some Blockchains are public, some are private
	  一些区块链是公开的，一些是私有的
	- Public Blockchains are still encrypted, but are viewable to the public
	  公开区块链仍然经过加密，但可以被公众查看
	- Private Blockchains employ user rights for visibility, e.g.
	  私有区块链使用用户权限控制可见性，例如：
		- Customer – Writes and views all data
		  客户——可写入并查看所有数据
		- Auditors – View all transactions
		  审计员——可查看所有交易
		- Supplier A – Writes and views Partner A data
		  供应商A——可写入并查看合作伙伴A的数据
		- Supplier B – Writes and views Partner B data
		  供应商B——可写入并查看合作伙伴B的数据
![[Pasted image 20250504180250.png#pic_75center|]]
- Consensus
  共识
	- Ensures that the next block in a blockchain is the one and only version of the truth
	  确保区块链中的下一个区块是唯一真实的版本
	- Ensures that parties agree to a certain state of the system as the true state.
	  确保各方对系统的某个状态达成一致，使其成为真实状态
	- Many Consensus mechanisms, each with pros and cons
	  存在多种共识机制，各具优缺点

## Consensus Algorithms in Blockchain

- A consensus algorithm is a procedure through which all the peers of the Blockchain network reach a common agreement about the present state of the distributed ledger.
  共识算法是一种程序，通过它区块链网络的所有节点就分布式账本的当前状态达成一致。
	- Proof of Work (PoW):The idea behind this algorithm is to solve a complex mathematical puzzle to validate the block, which requires a lot of computational power and the node who solves the puzzle first gets to add the next block (Bitcoin uses this algorithm).
	  工作量证明（PoW）：该算法的理念是通过解决复杂的数学难题来验证区块，这需要大量的计算能力。最先解出难题的节点可添加下一个区块（比特币使用此算法）。
	- Proof of Stake (PoS): Validators invest in the coins of the system and validate blocks by placing a bet on a block they think can be added to the chain (Ethereum 2.0 uses this algorithm).
	  权益证明（PoS）：验证者在系统的代币中投资，并通过对认为可以加入区块链的区块下注来验证区块（以太坊2.0使用此算法）。
	- Delegated Proof of Stake (DPoS): A more efficient PoS variant where token holders vote for delegates to validate transactions.
	  委托权益证明（DPoS）：更高效的PoS变体，代币持有者投票选举代表进行交易验证。
	- Proof of Burn (PoB): Validators sends coins to an unreachable address which means long term commitment and earns a privilege. This algorithms is not popular as it wastes resources needlessly.
	  烧币证明（PoB）：验证者将代币发送至无法访问的地址，以此表明长期承诺并获得权利。这种算法不受欢迎，因为它无谓地浪费资源。
	- Proof of Capacity: Validators invest their hard drive and more space a validator has, better are his chances of getting selected for mining the next block.
	  容量证明：验证者投入硬盘空间，拥有更多空间的验证者被选中挖掘下一个区块的机会更大。
	- Proof of Elapsed Time: PoET is one of the fairest and widely used in permissioned Blockchain networks. All the nodes wait for random amount of time and add it as a proof of their wait in the block. There are additional checks in the algorithm to stop nodes from always winning and stop nodes from generating a lowest timer value (Intel developed hardware).
	  经过的时间证明（PoET）：PoET是许可区块链网络中最公平且广泛使用的共识机制之一。所有节点等待随机时间，并将其作为证明添加到区块中。该算法中有额外的检查，以防止某些节点始终获胜，并阻止节点生成最低的计时器值（由英特尔开发的硬件）。
	- Proof of Authority (PoA): It is based on the reputation of trusted parties in a blockchain network. It is considered an efficient mechanism for private blockchains and was conceptualized by Ethereum co-founder and former CTO Gavin Wood in 2017.
	  权威证明（PoA）：基于区块链网络中可信方的声誉。这被认为是私有区块链的高效机制，并由以太坊联合创始人及前首席技术官加文·伍德于2017年提出
	- Byzantine Fault Tolerance (BFT): Ensures consensus even in the presence of malicious nodes (e.g., Hyperledger Fabric).
	  拜占庭容错（BFT）：即使在存在恶意节点的情况下，也能确保共识（例如，Hyperledger Fabric）
	- Directed Acyclic Graph (DAG): A blockchain alternative used in projects like IOTA, which allows parallel transaction validation.
	  有向无环图（DAG）：一种区块链替代方案，应用于IOTA等项目，允许并行交易验证
	- There also exist other consensus algorithms like Proof of Activity, Proof of Weight, Proof of Importance, Leased Proof of Stake, etc.
	  其他共识算法包括活跃度证明、权重证明、重要性证明、租赁权益证明等
	- Blockchain networks cannot function properly without the consensus algorithms in order to verify each transaction that is being committed.
	  没有共识算法，区块链网络无法正常运行，因为它们用于验证每一笔提交的交易

## Smart Contracts in Blockchain

- Smart contracts are self-executing programs stored on the blockchain that execute predefined rules automatically. They eliminate intermediaries, reducing costs and increasing efficiency.
  智能合约是存储在区块链上的自执行程序，能够自动执行预定义的规则。它们消除了中介机构，降低了成本并提高了效率。

| Platform | Language Used          | Notable Features                                          |
| -------- | ---------------------- | --------------------------------------------------------- |
| Ethereum | Solidity               | Largest smart contract ecosystem, DeFi, NFTs              |
| Solana   | Rust, C, C++           | High throughput, low transaction fees                     |
| Binance  | Smart Chain            | Solidity EVM compatible, faster and cheaper than Ethereum |
| Cardan   | Plutus (Haskell-based) | Focus on security and formal verification                 |
| Polkadot | Ink!, Rust             | Interoperability and cross-chain support                  |
![[Pasted image 20250504181439.png#pic_50center|]]
- User-defined self-executing computer programs running on top of blockchain
  用户定义的自执行计算机程序，运行在区块链之上
- Managing exchange of digital assets
  管理数字资产的交换
- Applications across many different sectors
  应用于多个不同的行业

Use Cases of Smart Contracts

| Sector         | Example use Cases                                         |
| -------------- | --------------------------------------------------------- |
| Finance (DeFi) | Automated lending, borrowing, insurance<br>自动借贷、保险        |
| Real Estate    | Property transfers, escrow services<br>财产转让、托管服务          |
| Supply Chain   | Tracking goods, automated payments<br>跟踪货物、自动付款           |
| NFTs & Gaming  | Ownership rights, in-game assets<br>所有权、游戏内资产             |
| Voting Systems | Tamper-proof voting and election mechanisms<br>防篡改投票和选举机制 |
| Healthcare     | Patient data management, insurance claims<br>患者数据管理、保险索赔  |


- Benefits of Smart Contracts
  智能合约的优势
	- Eliminates intermediaries
	  消除中介机构
	- Reduces fraud risk
	  降低欺诈风险
	- Faster and more efficient transactions
	  更快速且高效的交易
	- Cost-saving
	  节省成本
	- Highly secure due to blockchain technology
	  由于区块链技术，安全性极高

Challenge and Risks

| Challenge                    | Description                                                 |
| ---------------------------- | ----------------------------------------------------------- |
| Code Vulnerabilities<br>代码漏洞 | Bugs in code can be exploited<br>代码中的错误可以被利用                |
| Immutability Risks<br>不变性风险  | Can't correct errors once deployed<br>部署后无法纠正错误             |
| Scalability<br>可扩展性          | Limited by blockchain network performance<br>受区块链网络性能限制     |
| Legal Issues<br>法律问题         | Unclear regulation and legal enforceability<br>监管和法律可执行性不明确 |

- Popular Examples
	- Uniswap (DeFi): Automated trading using smart contracts
	  使用智能合约进行自动交易
	- OpenSea (NFTs): Buying/selling NFTs with smart contracts
	  通过智能合约买卖NFT
	- Chainlink (Oracles): Connecting smart contracts to real-world data
	  将智能合约与现实世界的数据连接起来
- Future of Smart Contracts
  智能合约的未来
	- Integration with AI & IoT
	  与人工智能和物联网的集成
	- Legal recognition and smart legal contracts
	  法律认可和智能法律合同
	- Cross-chain compatibility
	  跨链兼容性
	- Enhanced security audits and formal verification
	  加强安全审计和正式验证

## Differences Between Blockchains and Databases

- Blockchain is a specific form or subset of distributed ledger technologies, which constructs a chronological chain of blocks, hence the name 'block-chain'.
  区块链是一种特定形式或子集的分布式账本技术，它构建了一个按时间顺序排列的区块链，因此得名“区块链”。
- A block refers to a set of transactions that are bundled together and added to the chain at the same time.
  区块是指一组交易，这些交易被捆绑在一起，并同时添加到链上。
- A Blockchain is a write-only data structure, where new entries get appended onto the end of the ledger by linking to the previous block's 'hash'.
  区块链是一种仅可写的数据结构，其中新条目通过链接到前一个区块的“哈希”来附加到账本的末尾。
- Every new block gets appended to the block chain There are no administrator permissions within a Blockchain that allow editing or deleting of data.
  每个新的区块都会被附加到区块链上。区块链中没有管理员权限可以编辑或删除数据。
- In a relational database, data can be easily modified or deleted.
  在关系型数据库中，数据可以轻松修改或删除。
- Typically, there are database administrators who may make changes to any part of the data and/or its structure.
  通常，数据库管理员可以对数据的任何部分及其结构进行更改。
- However, Blockchains were designed for decentralized applications, whereas relational databases, in general, were originally designed for centralized applications, where a single entity controls the data.
  然而，区块链是为去中心化应用程序而设计的，而关系数据库通常最初是为集中式应用程序设计的，在集中式应用程序中，一个实体控制着数据。

## Where it all Started

- Blockchain technology started with the creation of Bitcoin in 2008.
  区块链技术始于 2008 年比特币的诞生。
- It was introduced by an anonymous person or group under the pseudonym Satoshi Nakamoto in the Bitcoin whitepaper titled "Bitcoin: A Peer-to-Peer Electronic Cash System."
  它由一个匿名个人或团体以化名中本聪（Satoshi Nakamoto）在比特币白皮书《比特币：一种点对点电子现金系统》中首次提出。
- The blockchain was designed as a decentralized and secure ledger to record Bitcoin transactions without the need for a trusted central authority.
  区块链被设计为一个去中心化且安全的账本，用于记录比特币交易，而无需依赖可信的中央机构。
- While Bitcoin was the first real-world implementation, the concept of blockchain-like structures existed earlier. In 1991, Stuart Haber and W. Scott Stornetta proposed a cryptographically secured chain of blocks to timestamp digital documents, preventing tampering.
  尽管比特币是区块链的第一个现实世界应用，但类似区块链的概念早在此前就已经出现。1991 年，斯图尔特·哈伯（Stuart Haber）和 W. 斯科特·斯托内塔（W. Scott Stornetta）提出了一种加密保护的区块链结构，用于对数字文件进行时间戳标记，以防止篡改。
- However, Nakamoto combined cryptographic techniques, proof-of-work consensus, and decentralized networking to create the first fully functional blockchain.
  然而，中本聪将加密技术、工作量证明共识机制和去中心化网络结合在一起，创造了第一个完全可运行的区块链。
- Think of Bitcoin as an electronic asset (as well as a digital currency)
  可以把比特币看作是一种电子资产（也是一种数字货币）。
- A network of computers keeps track of Bitcoin payments and adds them to an ever-growing list of all the Bitcoin payments that have been made, called “The Bitcoin Blockchain”.
  一组计算机网络负责记录比特币支付并将其添加到一个不断增长的支付列表中，这个列表称为“比特币区块链”。
- Blockchain is an incorruptible digital ledger of transactions that can be programmed to record not just financial transactions but virtually everything of value.
  区块链是一种不可篡改的数字账本，可以被编程用于记录不仅仅是金融交易，还可以记录几乎所有有价值的事物。
- A block refers to a set of transactions that are bundled together and added to the chain at the same time.
  区块是指一组交易，这些交易被捆绑在一起，并同时添加到链上。
- Each block is timestamped, with each new block referring to the previous block.
  每个区块都有时间戳，并且每个新区块都会引用前一个区块。
- Combined with cryptographic hashes, this timestamped chain of blocks provides an immutable record of all transactions in the network, from the very first (or genesis) block.![[Pasted image 20250504190455.png#pic_75center|]]
  结合加密哈希，这种带有时间戳的区块链提供了网络中所有交易的不可变记录，从最初的（创世）区块开始。
- This immutability, or 'unchanging over time' feature makes the Blockchain useful for accounting, financial transactions, identity management, asset ownership, management and transfer, just to name a few examples.
  这种不可变性，即“随时间推移不会改变”的特性，使区块链在会计、金融交易、身份管理、资产所有权、管理和转移等多个领域具有重要价值。
- It has grown in popularity in part because it securely allows exchange between two people or a network, without the need for a trust or a central authority.
  它之所以越来越受欢迎，部分原因是它可以安全地在两个人或一个网络之间进行交换，而无需信任或中央机构的参与。
- Crypto currencies also use Blockchain technology.
  加密货币也使用区块链技术。

## How blockchain Technology Works

![[Pasted image 20250504190911.png#pic_75center|]]
- Step 1: Transaction Initiation
  步骤 1: 交易发起
	- A user initiates a transaction (e.g., sending cryptocurrency or recording data).
	  用户发起交易（例如，发送加密货币或记录数据）。
	- This transaction is broadcast to a decentralized network of computers (nodes).
	  此交易被广播到去中心化的计算机网络（节点）
- Step 2: Transaction Verification
  步骤 2: 交易验证
	- Network nodes validate the transaction using a consensus mechanism (e.g., Proof of Work, Proof of Stake)
	  网络节点使用共识机制（例如，工作量证明或权益证明）验证交易
	- The transaction is checked against predefined rules (e.g., ensuring the sender has enough balance)
	  交易会根据预定义规则进行检查（例如，确保发送方有足够的余额）
- Step 3: Block Creation
  步骤 3: 区块创建
	- Valid transactions are grouped into a block
	  经过验证的交易被分组成一个区块
	- Each block contains
	  每个区块包含
		- A list of transactions
		  一系列交易
		- A unique identifier (hash)
		  一个唯一标识符（哈希）
		- A reference to the previous block's hash (creating a chain)
		  对前一个区块哈希的引用（形成链条）
- Step 4: Consensus & Block Addition
  步骤 4: 共识与区块添加
	- Miners (or validators) solve a complex crytographic puzzle (Proof of Work) or stake coins (Proof of Stake)
	  矿工（或验证者）解决复杂的密码学难题（工作量证明）或质押代币（权益证明）
	- Once verified, the new block is added to the blockchain
	  一旦验证完成，新区块被添加到区块链中
- Step 5: Chain Continuation & Security
  步骤 5: 链的延续与安全性
	- The block is permanently recorded and linked to previous blocks.
	  该区块被永久记录并链接到之前的区块
	- Any tampering would require changing all previous blocks. baking blockchain highly secure
	  任何篡改都需要更改所有之前的区块，使区块链高度安全
- Step 6: Completion & Transparency
  步骤 6: 完成与透明性
	- The transaction is confirmed, and the updated blockchain is distributed across all nodes
	  交易被确认，并且更新后的区块链被分发到所有节点
	- The process esures transparency, security, and decentralization
	  该过程确保了透明度、安全性和去中心化

## Types of Blockchains

- Public: These are blockchain networks that anyone can read, transact within and participate in the consensus process. The code is open-source and Bitcoin and Ethereum are the best-known public blockchain.
  公有链：这些区块链网络允许任何人阅读、进行交易，并参与共识过程。代码是开源的，比特币和以太坊是最知名的公有区块链
- Private: The private blockchain operates similarly to a public network but is limited to a single organization or group. That group determines the participants and maintains the distributed ledger. It also writes the transactions and can restrict read privileges to certain participants. Ripple, Multichain and Corda are private blockchains.
  私有链：私有区块链的运作方式类似于公有网络，但仅限于单个组织或团体使用。该团体决定参与者，并维护分布式账本。它还负责记录交易，并可以限制某些参与者的读取权限。Ripple、Multichain 和 Corda 是私有区块链的例子
- Permissioned: Permissioned blockchain networks require an invitation to join and participate.
  许可链：许可区块链网络要求收到邀请才能加入和参与
- Consortium: In a consortium network, multiple companies or organizations collaborate to organize a shared set of transactions. According to IBM, consortium blockchains are “ideal for business when all participants need to be permissioned and have a shared responsibility for the blockchain.” R3, HyperLedger and Fabric are examples of this category of blockchain.
  联盟链：在联盟网络中，多个公司或组织合作，共同管理一组共享的交易。根据 IBM 的定义，联盟区块链“非常适用于所有参与者需要获得许可，并共同承担区块链责任的商业环境。” R3、HyperLedger 和 Fabric 是这一类别的区块链示例
- Hybrid: Combines features of public and private blockchains (e.g., XinFin Network).
  混合链：结合公有链和私有链的特点（例如 XinFin Network）

## Blockchains Transaction Rates

Assume that blockchain has a new block added every 10 minutes (600 seconds) with a block size limit of 1 MB. If we assume an average transaction size of 250 bytes, determine how many transactions can fit in a block.
- 1000000 bytes/250 bytes =4000 transactions/block
- 4000 transactions/600 seconds ≈ 6.67 TPS

Assume a block time of 15 seconds and an average block includes 100 transactions. Calculate transactions per second (TPS).
- TPS=100 transactions/15 seconds ≈ 6.67 TPS

A blockchain network can process 1,000 transactions per second (TPS), and the average transaction size is 250 bytes. Calculate the maximum data throughput in Megabits per second.
- Bytes/second=TPS × Transaction Size =1000×250 =250000 bytes/second

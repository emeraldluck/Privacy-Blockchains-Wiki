#privacy blockchains

- Current Vulnerabilities + Need for privacy

  Bitcoin Privacy Model: Pseudonymity As a Decoy
  Bitcoin is the most popular application of blockchain, and many of its descendants share its privacy model. The network doesn’t store IPs or personal information. Instead, it relies on cryptographic pseudonymous addresses to protect its users’ identities. A user — let’s call him Dorian — generates a new address each time he collects a payment. Dorian gives the payer this new account number with no history. The payer can’t guess much about Dorian.
  The main concern comes when Dorian spends his money. A Bitcoin transaction often has multiple inputs and outputs. We can make the following assumptions (not always true, as we will see later on):
  When a transaction has many inputs, the owner of these is the same person.
  When a transaction has two outputs, one will be going to the payee, and the other will be change money (unspent transaction output).
  A bad actor can crawl the transaction graph and group together addresses that are likely to belong to the same person. All it takes to expose account owners is to associate one of these pseudonyms to an identity. Then it is like unrolling a ball of strings.
  Concretely, when you disclose your identity along with a payment, the payee may guess your bank statement. And they may follow your future transactions. Even more worrisome, the payee may not be the one spying you. An ICO can be subpoenaed, an exchange may be hacked, or a shopping website may have curious cookies.
  Machines and analytics algorithms are way better at crawling data than humans. They can scrape for data on social media, combine several data sources, and build a probabilistic model associating addresses with identities. In practice, the privacy model that our ecosystem has inherited from Bitcoin is very weak. Here’s an illustration:
  Dorian happens to be passionate about blockchains. He writes a Medium article that ends with a “please tip me” section and a “please follow me on Twitter.” You guessed it: it has a BTC address in it, the same one he included in his signature on his favorite forum, which you assume would only compromise his privacy. You tip him (because you like his work) and send him a private message on Twitter to thank him for his efforts. He wants to return the favor and tells the world how generous you are. He tweets, “Thank you @xxxxxxxxxxxxxxxxx for your tip.” Thanks to Dorian, now you’re vulnerable too. A simple algorithm looks for incoming transactions to Dorian’s tip address. It filters them through a time range — say, between his article and his tweet — and flags senders with your identity. Today, sophisticated tools that use machine learning and clustering techniques can be built to de-anonymize most blockchains.

  **Example 1** – As a business, when you make a payment to one of your suppliers for the goods they have provided to you, they can now access all your bitcoin transaction history and see which other suppliers you are dealing with. Knowing this information, they might raise the price of their goods and take away your power to negotiate since your public ledger is already available to them.

  **Example 2** – You visit a country or part of a country that has high crime rate. You make several purchases while visiting different places there—maybe to collect souvenirs on your way back home. Now, every shop or individual you have done a transaction with knows the frequency of your transactions, their sizes and the current bitcoin balance you have. This puts you in a dangerous situation.

  **Example 3** – You are a service provider where you charge your clients on a per-project basis. Being a reputable entity in the industry you not only charge clients for your services, but also for the value you bring to the table. However, looking at your past records in the public ledger your customers might never pay you the value of your service and end up negotiating your service fees most of the times.

  ## **How can we send money to a friend?**

  Meet Maria and her best friend George, who decide to meet up for a vacation. George’s budget is tight, so Maria offers to send some money to help pay for the flight, hotel room, and food.

  If Maria sends the money to George through the traditional banking system, they trust two intermediate parties (their respective banks) to symbolically move the funds for them.

  There is no actual movement of physical bills or assets, both banks simply edit their respective database to show that the funds have been moved. When Maria submits the transaction to her bank (whether that's online, on her bank app, or a check), her bank subtracts $2,500 from her account balance on their ledger, then contacts George’s bank and requests that they add $2,500 to George’s balance, so that he can withdraw the funds to pay for travel expenses.

  This process is shown in Figure X.1:

  [Figure X.1](https://github.com/monerobook/monerobook/blob/Ch-1-changes/chapters/soon)

  There are a few drawbacks and risks to this system, and it requires total trust of banks. Maria, George, and the banks must act on faith that transactions are legitimate and that the ledgers are kept honestly. This trust in the intermediate third parties poses a risk, since the banks or a nefarious actor may create unlimited money by fraudulently editing the ledger balances or transaction database.

  Furthermore, Maria does not actually have possession of $977241, only an IOU from her bank that she must trust is redeemable. She has no way to audit her bank to verify whether they actually have $977241.

  In fact, they may not hold that much, since most banks legally operate on “fractional reserve” - meaning that their actual assets are allowed to be significantly less than the total balance promised to account owners.

  Depending on how the funds were sent, it could take anywhere from minutes to days before the $2,500 shows up in George’s bank account. Since George is not privy to the banks’ ledgers or communications, the entire process is opaque and cannot be monitored.

  Many people that have not personally experienced economic disruption take functioning banks and the validity of their IOUs for granted. Few individuals consider the unsettling ramifications of handing their lifelong savings to opaque corporations, often putting all their eggs in a single institutional basket. Losses can occur due to:

  - negligence (the bank makes a mistake),
  - financial issues (the bank overextends their assets or goes out of business),
  - malice and corruption (the bank or a rogue employee steals your money)
  - hostile third parties (the bank is robbed or a hacker thieves electronic funds)

  Thankfully, an emerging new technology called blockchain is capable of mitigating literally all of the above risks by creating a decentralized database that all parties can equally use, view, and verify.

  ## **Introduction to blockchains**

  Anybody can learn all about Monero and how the blockchain works without having to understand the underlying mathematics and cryptography (similar to how anybody can become internet-savvy without first studying DNS servers and the IPv6 protocol). This chapter focuses on the key concepts and vocabulary without digging into all of the technical details - you can jump ahead to chapter 6 [crosslink to the 6th chapter] if you want to dive into the cryptographic framework.

  The term “blockchain” refers to a new method for securing records in a database that all network users share. It is groundbreaking for being a “trustless” system, where individuals retain full autonomy over their funds, there is no central authority, and each participant can easily verify and audit the system.

  Anyone in the world is welcome to act as a network maintainer, and each participant keeps the others honest by verifying the blockchain. When users broadcast information to be placed on the blockchain, network maintainers group these transmissions into “blocks” and use cryptographic tools to finalize the records and permanently link them onto the blockchain.

  Once data is sealed onto the blockchain, it cannot be deleted, moved, or altered in any way. ​The records are immutable and each participant on the network has matching copy of the blockchain for their own verification. The blockchain uses a clever “mining” model that encourages network participation and keeps all of the records honest and synchronized. These types of “decentralized” systems are incredibly robust since there is no single server or central database that can be maliciously attacked or manipulated.

  These decentralized systems are also “trustless” since each participant in the network maintains and verifies their own copy of the records instead of relying on any third party. Given that blockchains provide a system for global tamperproof recordkeeping, they are extremely well-suited for storing financial data. In fact, the very first distributed blockchain was conceptualized and launched for the Bitcoin cryptocurrency!

  In 2008, an anonymous individual or group known as Satoshi Nakamoto published a whitepaper describing “Bitcoin: A Peer-to-Peer Electronic Cash System”. This worldchanging document laid out the framework for the open-source decentralized cryptocurrency and the revolutionary blockchain technology that makes it possible.

  Figure X.1 in the first section highlighted that sending money through the traditional banking system requires multiple, transactions, ledgers, and trust in multiple banks. Figure X.2 (below) shows how Maria could send money to George using an imaginary cryptocurrency (XYZ) that uses a typical transparent open ledger. Maria will to 10.5 XYZ from her account (1BuUygisXY) to an address controlled by George (PeK5FSykwp).

  A few of the blockchain benefits are immediately apparent:

  - **Simplicity (& speed)**: Maria’s money is sent to George in a single step to update a single ledger. Whereas bank and wire transfers can take days or weeks, cryptocurrency ledgers typically update in seconds or minutes (the transaction time varies for different cryptocurrencies).
  - **No third-party risks**: Maria and George rely on their own cryptographically-secured and self-maintained system instead of placing their money and trust in the hands of a chain of third parties.
  - **Pseudo-anonymity**: Unlike the banks, cryptocurrency ledgers never learn names like “Maria” and “George” with the accounts. In fact, personal information is never necessary for generating an cryptocurrency address. George will access the funds pseudonymously, using his key for the “PeK5FSykwp” address to which Maria broadcasted the money (from her account, “1BuUygisXY”).

  Bitcoin and the other cryptocurrencies that followed have launched a financial revolution that is still unfolding. With these new decentralized networks, anybody can personally store and globally transfer funds at their own discretion. Prior to cryptocurrencies, it was difficult to store large amounts of wealth securely without trusting your savings to banks or credit unions. Likewise, transferring money to another individual or business required reliance on third-party payment processors for checks, wire transfers, or credit/debit cards.

  Thanks to cryptocurrencies, for the first time, anybody can exercise their basic financial rights without requiring access to a bank and approval from external institutions! In mere moments, any device (computer, phone, tablet) can be used to initialize a new cryptocurrency wallet that is fully functional for sending, storing, and receiving funds. Setting up a wallet does not require any kind of identification, fees, or authorization, and the system identifies users by addresses that look like random strings of numbers and letters instead of personally identifiable details such as street address or city.

  ## **Blockchain Drawbacks**

  Most cryptocurrencies are “pseudo-anonymous”, since their users are identified by unintelligible strings rather than personal identifiers. When you receive a cryptocurrency payment, you do not learn the sender’s name, instead you receive the funds from an address such as: 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa

  While this preserves privacy in some ways, it also exposes some sensitive information. Recall, every participant in a decentralized blockchain possesses a complete copy of the entire record. In the context of cryptocurrencies, this ledger is used to ascertain the account balance for any (e.g. Bitcoin) address.

  This transparent ledger means that every account balance is public! In fact, several helpful websites allow you to easily search the blockchain for any address or transaction. Suppose you run a shop, and one of your customers pays for a loaf of bread from the Bitcoin address 3P3QsMVK89JBNqZQv5zMAKG8FK3kJM4rjt. You can instantly check the blockchain and see that this account has received more than 5,000 Bitcoins! Knowing that your customer handled $50,000,000 recently, you might be inclined to charge more in the future, or simply rob them now. This privacy issue presents a personal security risk.

  In addition to knowing your customer’s balance, you can also see every transaction that they have received or sent: the amount, the timestamp, and both participants’ addresses. Analysis of transaction histories and patterns can be used to profile your spending patterns, wealth, income, and with whom you interact. A great amount of your personal information is exposed if your blockchain history is linked to your identity (for example, during an online purchase or while registering for a cryptocurrency exchange). Often the owner of an account can be revealed with a little bit of research; for instance, you might have already searched for the two Bitcoin addresses listed above to learn that they belong to Satoshi Nakomoto and the Pineapple Fund charity, respectively.

  Several companies exist solely to track and deanonymize transparent blockchains. For example, Elliptic offers an interactive explorer that shows the flow of funds between Satoshi, payment processors and exchanges, forums, marketplaces, gambling services, charities, known individuals, and other services. Figure Y shows a screenshot detailing significant Bitcoin transactions in the early 2010s, including connections between mining pools, Mt. Gox, and the Silk Road marketplace.

  Figure X: Elliptic’s blockchain analysis of Bitcoin flow in the early 2010’s, from the interactive Bitcoin Big Bang explorer [link: [https://www.elliptic.co/bigbang-v1.html](https://www.elliptic.co/bigbang-v1.html)]

  Take a moment to consider the valuable sensitive information that you generate each day: credit card transactions, every phrase that you search, products you view or purchase, social media sites that you interact with, etc… Almost all of it is recorded, profiled, and monetized by your banks, payment processors, giant tech/data industries, and governments.

  This mass collection of your data results in centralization of your personal and private information in vast troves of sensitive material that are juicy targets for hackers and blackmarket resale. It is quite probable that your personal details (such as name, address, email, phone number, etc) are already in the public domain without your knowledge, perhaps connected with your demographic and/or marketing dossier.

  Consider the recent Equifax, Target, Home Depot , Uber, and Panera data breaches. In many cases, both personal and financial information were compromised, putting individuals and their cards at risk.

  Accidental data breaches are not the only concern. Big data and tech companies carefully record your activities online, in order to provide better services. Often, this refers to targeted marketing and ads; however, this data can also be leveraged for more questionable uses such as manipulating your feelings or your voting behavior.

  Anything that a company tracks about you may be used maliciously or stolen/resold. You should exercise great caution regarding your digital footprint, since information cannot be “unleaked” after your personal details are exposed.

  Right now, privacy is conspicuously absent from mainstream economic and commercial systems. Traditional payment processors, banks, and cryptocurrencies leave very clear trails that are used to study, surveil, and profit from you. Once collected, you often have no way to control or track the proliferation of your data, or the privacy and personal security risks that arise from its sale to unknown parties.

  The only guaranteed way to exercise your right to financial privacy is to avoid revealing personal information in the first place! To stay safe, we need a way to interact securely - where transactions cannot be linked to your identity, your wealth, or other transactions. The Monero cryptocurrency is your best tool for taking all of these matters into your own hands!

  ## **Introducing Monero**

  [infographic]

  Monero (pronounced /mōnĕrō/, plural “Moneroj”) is a leading cryptocurrency with a focus on private and censorship-resistant transactions. The openly verifiable nature of most cryptocurrencies (such as Bitcoin and Ethereum) allows anybody in the world to track your money. Furthermore, links between your financial records and personal identity may jeopardize your safety.

  To avoid these dangers, Monero uses powerful cryptographic techniques to create a network that allows parties to interact without revealing the sender, recipient, or transaction amounts. Like other cryptocurrecies, Monero has a decentralized ledger that all participants can download and verify for themselves.

  However, a series of mathematical tricks are used to conceal all of the sensitive details and styme any blockchain tracking. Monero users reap all the benefits of a decentralized trustless financial system, without risking the security and privacy downsides of a transparent blockchain.

  One of Monero’s crucial defining features is enforced privacy by default​. Users are specifically prevented from initializing transactions that are accidentally or intentionally insecure. This provides Monero users with peace of mind since the network will not accept a revealing transaction!

  Figure X.3 (below) shows how Maria sends George funds for booking flights using Monero. The process is functionally the same as the cryptocurrency transaction shown in Figure X.2, however the sensitive information is cryptographically obscured. Information like account balances and transaction amounts are secretly encrypted, in contrast to the transparent public record that most cryptocurrencies are built on.

  Monero’s privacy features allow the network to assess the validity of a transaction and determine whether or not the sender has a sufficient account balance, without the actually knowing the transaction amount or account balances! Nobody can view others’ account balances, and transactions don’t reveal the source of the funds being transferred.

  These are marked with “???” in the diagram, since an no outside observer can ascertain the values. The mechanics behind these unique privacy features are discussed in chapter X.

  [Figure X.3]

  ## **Principles of Monero**

  Monero is designed with the following principles in mind:

  - **Network Decentralization**: The Monero network and ledger are globally distributed. This means that there is no single server or database that can be maliciously controlled or censored. If one government were to shut down Monero nodes in their country, or attempt to limit who can send/receive Monero, the effort would be in vain! The rest of the world will carry on the network and process any valid transactions.
  - **Financial Security**: The globally-distributed Monero has no central weak point that can be hacked to steal your funds. Your Moneroj are secured by immutable cryptographic techniques, so there is no need to trust a third party with responsibility over your funds. Every single Monero participant can verify the validity of the ledger themselves, so you do not even have to trust the node operators! (You can learn more about the cryptographic techniques that secure Monero in chapter X)
  - **Financial Privacy**: Most blockchain projects increase security at the expensive of privacy, however Monero prioritizes your privacy. Transaction amounts, sender identity, and recipient identity are all obfuscated on the blockchain, so your Moneroj storage and spending activities are not trackable.
  - **Fungibility**: The term “fungibility” means that some type of asset is considered interchangeable. For example, imagine that you let your neighbor borrow 1 kilogram of flour for a cake. When they return flour the next week, of course it will be 1 kilogram of flour from a different source (since they used your original flour for baking). This is not a problem, since flour is fungible. However, vehicles are not fungible; if you let your neighbor borrow your car, you probably want the same one back!

  In the case of Monero, its fungibility is a feature of its sophisticated privacy practices, and refers to how the obfuscated transaction record means that it is impossible to ascertain the history of any particular Moneroj. If you let your friend borrow 1 Monero, they can return any 1 Monero, since they’re indistinguishable. This particular quality may seem like a minor nuance, however fungibility crucially necessary for something to be practically used as a currency (see examples below). This characteristic is absent from most cryptocurrencies, with transparent ledgers and trackable histories.

  ## **Real-life "use-case" for Monero**

  This section talks about some of the difficulties and risks that arise from using insecure cryptocurrencies. For simplicity, the examples refer to “Bitcoin” as the prototypical transparent-blockchain currency. However, these drawbacks are present in essentially all cryptocurrencies; not Bitcoin in particular.

  - **Price manipulation**: Sofia is the only mechanic in a small town. One of her customers paid for an oil change with Bitcoin. Sofia later looked up his address on the ledger and saw that the customer’s wallet contained enough Bitcoin for a new Lamborghini. Next time he needed a repair, she doubled her prices. If the customer had used Monero, Sofia would have been unable view his balance or use such information to manipulate prices.
  - **Financial surveillance**: Oleg’s parents send him some Bitcoin to pay for textbooks, and then continue to snoop on his Bitcoin address and activity. A few months later, Oleg sends some leftover Bitcoin to the public donation address for an organization that does not align with his parents’ political views. He does not realize that they are still monitoring his Bitcoin activity until he receives a furious email from his parents, berating him. If Oleg had used Monero, his family would not have been upset from prying into his transaction activity.
  - **Supply chain privacy**: Kyung-seok owns a small business providing family catering services for local events. A large food company uses blockchain tracing to identify most of his regular clients. The corporation uses this list to contact Kyung-seok’s customers, offering similar deals for 5% less. If Kyung-seok’s business used Monero instead, its transaction history could not have been exploited by rival businesses seeking to steal his customers.
  - **Discrimination**: Ramona finds her dream apartment, conveniently close to her new job in a great neighborhood. She pays her rent on time every month, but the landlord notices that she often receives Bitcoin from a legal online casino. The landlord personally despises gambling, and unexpectedly chooses to not renew Ramona’s lease. If rent was paid in Monero, the landlord would not be able to review and discriminate based on Ramona’s sources of income.
  - Transaction security/privacy: Sven sells a guitar to a stranger, and gives the buyer a Bitcoin address from his long-term savings wallet. The buyer checks the blockchain, sees the large sum of money that Sven has saved up, and consequently robs him at gunpoint. If Sven had instead given a Monero address for payment, the buyer would not have been able to view Sven’s wealth. Censorship: ​Makalah purchases some Bitcoin from an online exchange that verified her identity, then transfers a portion to a charity supporting human rights in her country. Two years later, her government analyzes the blockchain and notes the transaction from a known exchange to a blacklisted activist group. The government subpoena the exchange for Makalah’s identity and arrests her the next day. If Makalah used Monero for the donation, her government would never have known the source or destination of that contribution.
  - Tainted coins: Loki sells some of his artwork online to save up for college. When he pays tuition, he is shocked to receive a “payment INVALID” email from the school. Unbeknownst to Loki, one of his paintings was purchased using some Bitcoin that were stolen during an exchange hack the previous year. Since the school rejects any payment from a blacklist of “tainted” Bitcoins, they refuse to mark the bill “paid.” Loki is in an extremely difficult position: the Bitcoin that he saved has already been spent from his account, yet the tuition bill is still unpaid. This entire situation would have been avoided if Loki sold his paintings for Monero instead, since its fungibility precludes tracking or blacklists.

  ## **Monero: open-source decentralized community and software**

  Monero is an open-source project actively developed by cryptography and distributed systems experts from all over the world. Many of these developers freely donate their time to The Monero Project, while others are funded by the Monero community so that they can focus entirely on the project.

  The decentralized nature of Monero’s development team brings several benefits over a consolidated corporation or organization. The Monero Project is a living entity, greater than any individual or group. Since both the network and development team are spread across the globe, it cannot be shut down by any single country, or controlled within any particular legal jurisdiction.

  The term “open-source” means that the source code (software blueprints) are made publicly available for anybody to inspect. The alternative is “closed-source” software, where developers only deliver the final compiled product (“binaries” like .exe files) that cannot be opened and studied. If you use closed-source software, you are trusting the developer and distributor. The problem is that even a developer with the best intentions may make a mistake that hackers later discover and exploit. Only use open-source cryptocurrency software that has been audited by independent parties to verify the absence of that malicious code, accidental mistakes, and implementation weaknesses.

  The cryptocurrency community has embraced open-source software from the very start: Bitcoin was released as a public white paper and open-source community-built code, which stood in stark contrast to the opaque and proprietary decision structure endemic to fiat (government-backed) currencies. Of course, the open-source philosophy has been around much longer than cryptocurrencies! Over 25 years, more than 5,000 coders have contributed to the open-source Linux kernel, which is widely considered to be one of the most secure operating systems.

  The trust and security benefits of open-source software are of key importance for any cryptocurrency, so The Monero Project is entirely open-source. The developers uses Git [link: [https://github.com/monero-project/monero](https://github.com/monero-project/monero)] for version control, which allows anybody to easily review every single line of code proposed to be added, removed, or modified. Over 240 developers have contributed to, reviewed, and tested the Monero code, which drastically lowers the likelihood that any errors have been overlooked. Developers can find more information about interacting with Monero’s codebase in chapter X.

  Development team transparency is very important for community trust, especially in the context of cryptocurrencies. In addition to posting code for public scrutiny, The Monero Project also conducts all development team meetings on open IRC channels, [link: [https://getmonero.org/community/hangouts/](https://getmonero.org/community/hangouts/)] and all of the logs are archived on the public Monero website. [link: [https://getmonero.org/blog/tags/dev%20diaries.html](https://getmonero.org/blog/tags/dev%20diaries.html)]

  ## **History of Monero**

  In 2013 Nicolas van Saberhagen published the “CryptoNote” protocol, which became the foundation for many coins, starting with Bytecoin. Like the unknown Satoshi Nakamoto, the creator of Bytecoin remained anonymous and promoted their coin through a Bitcointalk thread.

  Some aspects of Bytecoin appeared dubious under close scrutiny. Bitcointalk member “thankful_for_today” investigated the emissions curve and noted that approximately 82% of the coins had already been emitted, so the circulating coin supply was potentially dangerously centralized.

  Ultimately, this greedy premine undermined Bytecoin’s credibility and practicality. Thankfully, thankful_for_today recognized the value in CryptoNote’s features, and incorporated them into a new project centered around a strong, community-driven development team. The Monero cryptocurrency, spearheaded by thankful_for_today, launched in April 2014. The coin was originally named “BitMonero,” however the community quickly elected to shorten it to “Monero.”

  ## **Ethical Discussion**

  Monero was carefully engineered to provide characteristics like fungibility and transaction privacy that are necessary for any currency (crypto- or otherwise) to be feasible for general use. As discussed in the section on use cases [internal link], there are significant practical issues that arise with financial systems that do not protect users’ privacy.

  The very features necessary to keep Monero safe for day-to-day users and businesses are unfortunately also appealing to those wishing to conceal illicit activity. Because of Monero’s privacy features and ease of mining, it has been utilized by criminals, ransomware, and covert mining (employing “botnets” of many victims’ hijacked devices).

  Monero is not intended to facilitate illegal activity, which has plagued every currency since the idea of money was conceived thousands of years ago. The scale of illegal transactions conducted using cryptocurrencies is dwarfed by the staggeringly-vast amount of criminal activity that occurs every day denominated in fiat currencies like Euros, Rupees, Yen, or Dollars.

  The creators of “Mastering Monero” and the entire Monero Community do not condone illegal activities, and we do not wish to assist criminals. If you wish to use Monero for exploitation or dark purposes, please close this book now, and do not use our project for harmful ends.

- What is a private transaction

  Privacy standards depend on the industry and also the tradeoffs we are willing to make. For asset transfers — cryptocurrencies, ERC-20 tokens — proper privacy means preserving the transaction graph confidentiality. Transactions should be unlinkable and untraceable, and participants should remain anonymous. The following definitions from the [CryptoNote white paper](https://cryptonote.org/whitepaper.pdf) help clarify the standards that a privacy-preserving scheme should meet:

  - **Unlinkability**: for any two outgoing transactions, it is impossible to prove they were sent to the same person.
  - **Untraceability**: for each incoming transaction, all possible senders are equiprobable.

  Let’s port that to the ledger metaphor. We would see lines appearing (debit, credit, balance), without knowing who is involved. One way to achieve that would be through a mixing service (more on that later). Still, the information from these “lines” can be linked with a non-blockchain data source, and the privacy shield may not hold. We need more. We need to conceal the amounts. This “line appearing” should disclose neither participants nor amounts, yet it should contain data that ensures a consistent ledger state.

  The system should enforce that we neither create assets out of the blue nor double spend. An anonymous crypto scheme that does exactly that is Zerocash. From a blockchain perspective, it means that we don’t store the world state anymore. We store proofs that the world state is consistent and that state transitions are valid. It becomes the user’s responsibility to maintain their own **world state.

  It is important to note that a lot of work goes into concealing transaction amounts: mixing services, confidential transactions, zero knowledge proofs. Unfortunately, these constructs don’t generalize well to arbitrary computation.

2. Protocols

**Zerocoin: [zerocoin.org](http://zerocoin.org/) September 28 2013**

- Zero coin projects

  Zcoin (XZC) 2016 28 september

  Zoin ZOI 2016 November, fork of Zcoin

  PIVX, proof of stake zerocoin implementation, October 16th, 2017 + May 8th private staking Why did they not take up 

  ZeroVert (ZER)[10] is a Scrypt-N algorithm coin, merge-mineable on the VTC chain with a total circulation of 8.4 million ZER. 

  [https://ipfs.io/ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/Zerocoin.html](https://ipfs.io/ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/Zerocoin.html)

  # Dark Wallet

  Cody Wilson's [project](https://darkwallet.unsystem.net/) with Amir Taaki and the anarchist group unSystem launched last Thursday with two particular methods for protecting its users' identities. One is what it calls "CoinJoin." Every time a user makes a payment with Dark Wallet, the program is set by default to combine the transaction with that of another Dark Wallet user attempting to make a payment around the same time. The communications to set up that multiparty transaction are encrypted, so that detecting who paid whom becomes far more difficult. Eventually, Dark Wallet plans to expand CoinJoin to combine payments of three or more users, creating an even more tangled web of money flows.

  On top of protections for senders, Dark Wallet adds another one for receivers that it calls "stealth addresses." When a user publishes a stealth address instead of a normal bitcoin address as his or her public P.O. box for receiving funds, any money sent by another Dark Wallet user to that address goes through an extra obfuscating process. Instead of appearing in the blockchain as being sent to that stealth address, Dark Wallet encrypts the address in such a way that only the recipient can recognize it and sends the money to that encrypted address. The receiver's Dark Wallet app scans the blockchain for payments encrypted to his or her stealth address and decrypts them to claim the funds. Crucially, no evidence remains in the blockchain that ties the sender and recipient.

**Zerocash: November 16 2013**

- Zerocash projects

  Improvements to the second generation of mixers include further decentralization of the mixing process by outsourcing the processing load to the altcoin's distributed network, rather than relying only on the mixing server and vastly increasing the total size of the user 'anonymity set'.

  Leading the charge of anonymous altcoins is the Zerocoin team, which includes cryptographers Matthew Green and Ian Miers. After [deciding](http://coinchomp.com/2014/03/10/zerocoin-zero-knowledge-infinite-anonymity/) to avoid the engineering complications of implementing Zerocoin on top of bitcoin, Green and his team began working on a standalone altcoin implementation dubbed '[Zerocash](https://www.youtube.com/watch?v=FXU65XsLiFk)'.

  Miers presented the Zerocash [paper](https://bitcoinfoundation.org/blog/wp-content/uploads/2014/03/bitcoin14_submission_12.pdf), "Rational Zero: Economic Security for Zerocoin with Everlasting Anonymity", at the IFCA Bitcoin Workshop. Another privacy-enhancing [paper](https://bitcoinfoundation.org/blog/wp-content/uploads/2014/03/bitcoin14_submission_19.pdf), "Increasing Anonymity in Bitcoin", was presented by Amitabh Saxena.

  The improved version of the protocol "that reduces proof sizes by 98% and allows for direct anonymous payments that hide payment amount" was announced on 16 November 2013.[[11]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-13) The developers presented their technical paper[[12]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-14) at the 2014 IEEE Security & Privacy Symposium[[13]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-15) along with launching the site.[[14]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-16)

  The new protocol was called Zerocash. It is now not an extension to the bitcoin, but rather an independent technology with the same basic principles as blockchain and transactions, which was planned to implement in alt-coin.[[15]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-17) Zerocash utilizes succinct non-interactive zero-knowledge arguments of knowledge (also known as [zk-SNARKs](https://en.wikipedia.org/wiki/SNARK)), a special kind of [zero-knowledge](https://en.wikipedia.org/wiki/Zero-knowledge_proof) method for proving the integrity of computations.[[16]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-18) Such proofs are less than 300 bytes long and can be verified in only a few milliseconds. However, zk-SNARKs require a large initial database for verifying (about 1.2 GB) and long time for producing a proof (spending the coin): 87 seconds to 178 seconds.[[17]](https://en.wikipedia.org/wiki/Zerocoin#cite_note-19)

  Zcash: 28 October 2016; 18 months ago

  [https://en.wikipedia.org/wiki/Zcash#cite_note-Southurst-2](https://en.wikipedia.org/wiki/Zcash#cite_note-Southurst-2)

  Zclassic was released in November 2016 by Rhett Creighton, a blockchain developer and minor Bitcoin core contributor in the San Francisco Bay Area.[15] Creighton used the same code as Zcash, with a lack of a founders fee required to mine a valid block.[6][16][10] This promotes a fair distribution, preventing centralized coin ownership and control.[10]  [https://zclassic.org](https://zclassic.org/) Zclassic is a fork of Zcash: (@HeyRhett) decided to take another path by removing the 20% fee. Miners are simply earning their fair reward, we believe they deserve it, and the coin development can be supported by the community. ZCL also differs from ZEC by removing the slow start (source), we are not trying to deliberately engineer scarcity: The Market decides the price.

  Hcash (HSR): [https://h.cash](https://h.cash/) takes zk proofs from zcash

  Komodo (KMD) Komodo’s Native Privacy Feature: Jumblr: [https://www.komodoplatform.com/en](https://www.komodoplatform.com/en) [https://komodoplatform.com/wp-content/uploads/2018/05/2018-05-09-Komodo-White-Paper-Full.pdf](https://komodoplatform.com/wp-content/uploads/2018/05/2018-05-09-Komodo-White-Paper-Full.pdf) Jumblr is a Komodo technology that enables users to anonymize their cryptocurrencies. At its foundational level, Jumblr takes non-private funds from a transparent (non-private) address, moves the funds through a series of private and non-traceable zk-SNARK addresses—which disconnects the currency trail and anonymizes the funds—and then returns the funds to a new transparent address of the user’s choosing. Through a connected Komodo technology, BarterDEX, Jumblr can provide this service not only for Komodo’s native coin, KMD, but also for any cryptocurrency connected to the Komodo ecosystem. - optional privacy - Our Jumblr technology solves these issues through a two-layered approach, relying on connected technologies in the Komodo ecosystem—BarterDEX, our native Komodo coin (KMD), and the upstream Zcash parameters. The Jumblr process is managed locally on the user’s machine and requires no third parties, human coordination, or other mixing services.

  This coin began as a fork of the popular privacy coin, Zcash15. As such, KMD retains the same inherent privacy features. Notable among these features are the Zcash parameters and zk-SNARK technology. These enable users to move funds on a public blockchain without leaving a data trail for later analysis. This is one of the most powerful forms of blockchain privacy in existence, as the provided privacy is effectively permanent. The Zcash parameters and zk-SNARK technology provide the initial foundation for users to take transparent KMD funding and make it anonymous (with the assistance of Komodo’s Jumblr technology) without leaving behind a cryptocurrency trail. The Zcash project itself is a fork of Bitcoin. Thus, all the features designed by Satoshi Nakamoto in the Bitcoin protocol are also available in Komodo.

  2017 May [https://zencash.com](https://zencash.com/) [https://zencash.com/assets/files/Zen-White-Paper.pdf](https://zencash.com/assets/files/Zen-White-Paper.pdf) 

  Our team realized that Zclassic could be further extended as a fully encrypted network
  with an innovative economic and governance model that better aligns with Satoshi’s original vision for a decentralized global community. We view Zclassic as a fundamentally pure open-source, all-volunteer cryptocurrency project, while Zen extends into a platform with internal funding to facilitate a broader set of communications, file-sharing, and economic activities. Some of the foundations of our project come from Bitcoin, Dash,
  Decred, and Seasteading.

**Cryptonote: 2012 December 12**

- Cryptonote projects

  ## **Bytecoin (BCN)[[edit](https://en.wikipedia.org/w/index.php?title=CryptoNote&action=edit&section=6)]**

  *Main article: [Bytecoin (cryptocurrency)](https://en.wikipedia.org/wiki/Bytecoin_(cryptocurrency))*

  Bytecoin (BCN), not to be confused Bitcoin (BTC), was the first implementation of the CryptoNote protocol launched to the public on July 4th 2012[[5]](https://en.wikipedia.org/wiki/CryptoNote#cite_note-5). Since launching, several improvements have been introduced including [multisignature](https://en.wikipedia.org/wiki/Multisignature) transactions[[6]](https://en.wikipedia.org/wiki/CryptoNote#cite_note-6) and several security updates. In 2013, the original CryptoNote Java implementation was rewritten using [C++](https://en.wikipedia.org/wiki/C%2B%2B).[[7]](https://en.wikipedia.org/wiki/CryptoNote#cite_note-7)[[dubious](https://en.wikipedia.org/wiki/Wikipedia:Accuracy_dispute#Disputed_statement) – [discuss](https://en.wikipedia.org/wiki/Talk:CryptoNote#Dubious)]

  ALL FORKS OFF BYTECOIN

  ~~2013 Jun: Buddhacoin BDC~~

  ~~2013 Sep: Paladincoin PLD~~

  2014 Apr: Boolberry BBR, wild keccack POW

  2014 May: Monero XMR

  [https://getmonero.org/resources/research-lab/](https://getmonero.org/resources/research-lab/)

  [https://downloads.getmonero.org/whitepaper_annotated.pdf](https://downloads.getmonero.org/whitepaper_annotated.pdf)

  2014 May: DarkNote XDN, quazarCoin QCN, ~~Mountcoin MNT~~, Fantomcoin FCN [https://forum.cryptonote.org/viewtopic.php?f=6&t=172](https://forum.cryptonote.org/viewtopic.php?f=6&t=172)

  2014 June: AEON AEON fork of XMR, Moneta Verde MCN, DarkNote (ex-duckNote) XDN [https://forum.cryptonote.org/viewtopic.php?f=6&t=203](https://forum.cryptonote.org/viewtopic.php?f=6&t=203)

  20144 July: Dashcoin DSH, ~~OneEvilCoin OEC renamed to XMN~~, CryptonoteCoin CNC

  2014 August: *~~ALL FORKS OFF cryptonote coin: Asapcoin ASAP, Cheerynote CRR, infininium-8 INF8~~*

  2014 Septemer/october: Dosh Kapital DOSH, ~~Forks off DOSH DiamondBack DBK, Silverback SBK~~ 

  2014 OCtober: Darknetcoin DNC Wild keccack PoW

  2014 Dec/ 2015 Jan: Forks off cryptonotecoin CNC: doctorbyte DB, Redwind RD

  2015 May: Pebblecoin XPB Boulderhash PoW

  2015 July: Tavos XTV [https://forum.cryptonote.org/viewtopic.php?f=6&t=676](https://forum.cryptonote.org/viewtopic.php?f=6&t=676)

  2015 [XMN] Magnatoj. Untraceable payments [https://forum.cryptonote.org/viewtopic.php?f=6&t=828](https://forum.cryptonote.org/viewtopic.php?f=6&t=828)

  May 2016: karbo KBR

  Aeon (AEON): [http://www.aeon.cash/](http://www.aeon.cash/) 

**Coinjoin: 2013**

- Coinjoin projects

  COINJOIN [https://bitcointalk.org/index.php?topic=279249](https://bitcointalk.org/index.php?topic=279249) August 2013 CoinJoin is an anonymization method for bitcoin transactions proposed by Gregory Maxwell. It is based on the following idea: “When you want to make a payment, find someone else who also wants to make a payment and make a joint payment together.”.[1] When making a joint payment, there is no way to relate input and outputs in one bitcoin transaction and thus the exact direction of money movement remains unknown to third parties. 2013 dark wallet bitcoin There are several implementation of anonymous bitcoin transactions inspired by CoinJoin: SharedCoins,[2] Dark Wallet,[3] CoinShuffle [http://crypsys.mmci.uni-saarland.de/projects/CoinShuffle/coinshuffle.pdf](http://crypsys.mmci.uni-saarland.de/projects/CoinShuffle/coinshuffle.pdf),[4] PrivateSend feature of Dash and JoinMarket.[5] CoinJoin requires that users negotiate transactions they wish to join. The first services to handle this (such as blockchain.info's SharedCoin) used centralized servers and required users to trust the operator of the service not to steal the bitcoins or allow others to do so. Centralized services may also compromise participants' privacy by keeping logs of the transactions they negotiate.[[9]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-9) Decentralized implementations of CoinJoin such as JoinMarket attempt to circumvent various issues related to centralization.[[5]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-joinmarket-bitcointalk-5) The level of anonymity offered by CoinJoin can also be diminished if the protocol is implemented incorrectly. One such flaw was identified in blockchain.info's SharedCoin mixing service. Security consultant Kristov Atlas,[[10]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-10) author of the book Anonymous Bitcoin,[[11]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-11)detailed the flaw in an article entitled Weak Privacy Guarantees for SharedCoin Mixing Service.[[12]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-12) In this article he states “the SharedCoin service should be used only as a light protective measure for financial privacy”. As part of his research, the author developed a tool called 'CoinJoin Sudoku'[[13]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-13) that could identify SharedCoin transactions and detect relationships between specific payments and payees.[[14]](https://en.wikipedia.org/wiki/CoinJoin#cite_note-14) Only a proof-of-concept implementation of CoinShuffle protocol was made available, written purely to evaluate the feasibility and performance.[8] It was followed by further research leading to the CoinShuffle++, ValueShuffle and PathShuffle proposals. ValueShuffle was presented at Scaling Bitcoin 2017 by Tim Ruffing (Saarland University): video recording. Comparison with other coins [http://crypsys.mmci.uni-saarland.de/projects/CoinShuffle/#prototype](http://crypsys.mmci.uni-saarland.de/projects/CoinShuffle/#prototype) [http://crypsys.mmci.uni-saarland.de/projects/CoinShuffle/coinshuffle.pdf](http://crypsys.mmci.uni-saarland.de/projects/CoinShuffle/coinshuffle.pdf)

   Vulnerabilities in sharedcoin [http://www.coinjoinsudoku.com/advisory/](http://www.coinjoinsudoku.com/advisory/)

  [https://en.bitcoin.it/wiki/CoinJoin](https://en.bitcoin.it/wiki/CoinJoin)

**Dash - 2014 January**

- Dash info

  Das

  Dash uses zcash's [https://bitcointalk.org/index.php?topic=421615.0](https://bitcointalk.org/index.php?topic=421615.0)

  Dash was originally released as XCoin on January 18, 2014. The founder, Evan Duffield, proposed a series of improvements to Bitcoin's protocol[[9]](https://en.wikipedia.org/wiki/Dash_(cryptocurrency)#cite_note-9), including:

  - a two-tier incentivized network of Masternodes and miners
  - instant transaction confirmations without a centralized authority
  - a system for increasing fungibility of coins and anonymity of users
  - an improved hashing algorithm (X11)

  XCoin was renamed to Darkcoin on January 28th, reflecting a focus on user anonymity, then on March 25, 2015, rebranded as Dash (a [portmanteau](https://en.wikipedia.org/wiki/Portmanteau) of "Digital Cash") to reflect a shift in focus towards mainstream payments.[[10]](https://en.wikipedia.org/wiki/Dash_(cryptocurrency)#cite_note-rebrand-10)

  In addition to Bitcoin's feature set, Dash offers instant transactions (InstantSend),[2] private transactions (PrivateSend)[3] and operates a self-governing and self-funding mechanism that fosters the creation of independent entities that serve the network[4]. This decentralized governance and funding system makes it one of the first decentralized autonomous organizations (DAO)[5] and the first DAO recognised by international law[6].

  [https://github.com/dashpay/dash/wiki/Whitepaper](https://github.com/dashpay/dash/wiki/Whitepaper)

Darkwallet - ???? Pioneers

- Darkwallet info

  # Dark Wallet

  Cody Wilson's [project](https://darkwallet.unsystem.net/) with Amir Taaki and the anarchist group unSystem launched last Thursday with two particular methods for protecting its users' identities. One is what it calls "CoinJoin." Every time a user makes a payment with Dark Wallet, the program is set by default to combine the transaction with that of another Dark Wallet user attempting to make a payment around the same time. The communications to set up that multiparty transaction are encrypted, so that detecting who paid whom becomes far more difficult. Eventually, Dark Wallet plans to expand CoinJoin to combine payments of three or more users, creating an even more tangled web of money flows.

  On top of protections for senders, Dark Wallet adds another one for receivers that it calls "stealth addresses." When a user publishes a stealth address instead of a normal bitcoin address as his or her public P.O. box for receiving funds, any money sent by another Dark Wallet user to that address goes through an extra obfuscating process. Instead of appearing in the blockchain as being sent to that stealth address, Dark Wallet encrypts the address in such a way that only the recipient can recognize it and sends the money to that encrypted address. The receiver's Dark Wallet app scans the blockchain for payments encrypted to his or her stealth address and decrypts them to claim the funds. Crucially, no evidence remains in the blockchain that ties the sender and recipient.

- **Particl 2015/2016**

  Shadow is a truly unique project, spawned from Bitcoin, over 6 months of development has transformed the pseudonymous Bitcoin into the first true anonymous decentralized cryptocurrency – Shadowcash. In traditional financial terms, other cryptocurrencies represent the trackable check or card option, while Shadow is cash. ShadowSend‘s unique zero-knowledge, dual-key stealth address and ring signature protocol enables near-instant, untraceable, unlinkable and trustless transactions.

  Yes. ShadowSend‘s unique zero-knowledge, dual-key stealth address and ring signature protocol enables near-instant, untraceable, unlinkable and trustless transactions.

  [https://github.com/shadowproject/whitepapers/blob/master/shadowcash_anon.pdf](https://github.com/shadowproject/whitepapers/blob/master/shadowcash_anon.pdf) [https://shadowproject.io/en](https://shadowproject.io/en) Team moved onto building [https://particl.io](https://particl.io/) 23 Mar 2017 [https://github.com/particl/whitepaper/blob/master/decentralized-private-marketplace-draft-0.1.pdf](https://github.com/particl/whitepaper/blob/master/decentralized-private-marketplace-draft-0.1.pdf)

bit tumble [https://eprint.iacr.org/2016/575.pdf](https://eprint.iacr.org/2016/575.pdf)

blindcoin [http://fc15.ifca.ai/preproceedings/bitcoin/paper_3.pdf](http://fc15.ifca.ai/preproceedings/bitcoin/paper_3.pdf)

[https://scalingbitcoin.org/papers/mimblewimble.pdf](https://scalingbitcoin.org/papers/mimblewimble.pdf)

Mix coin then [https://eprint.iacr.org/2014/077.pdf](https://eprint.iacr.org/2014/077.pdf) then blindcoin [http://fc15.ifca.ai/preproceedings/bitcoin/paper_3.pdf](http://fc15.ifca.ai/preproceedings/bitcoin/paper_3.pdf)

- Other mentions

  [https://github.com/ZcashFoundation/GrantProposals-2018Q2/issues/29](https://github.com/ZcashFoundation/GrantProposals-2018Q2/issues/29)

  [https://blog.z.cash/bolt-private-payment-channels/](https://blog.z.cash/bolt-private-payment-channels/)

  [https://github.com/trinity-project/trinity](https://github.com/trinity-project/trinity)

  Enigma (ENG): [https://www.enigma.co/](https://www.enigma.co/) 

  [https://wiki.parity.io/Private-Transactions.html](https://wiki.parity.io/Private-Transactions.html)

  Other mentions:

  [https://s3.amazonaws.com/enigmaco-website/uploads/pdf/enigma_full.pdf](https://s3.amazonaws.com/enigmaco-website/uploads/pdf/enigma_full.pdf)

  Hcash 

  For Ethereums EVM

  - Secure Multiparty Computation (SMPC)
  - Trusted Execution Environment (TEE)
  - Computation verification
  - Fully Homomorphic Encryption (FHE)
  - Indistinguishability Obfuscation
  - Zero knowledge proofs

  # **Secure multiparty computation (SMPC)**

  In an [SMPC](https://en.wikipedia.org/wiki/Secure_multi-party_computation), a given number of participants, p1, p2, …, pN, each have private data, respectively d1, d2, …, dN. Participants want to compute the value of a public function on that private data: F(d1, d2, …, dN) while keeping their own inputs secret. A way that can be applied to smart contract execution is to express the computation as a boolean circuit using AND and NOT gates. The circuit would work with encrypted data and produce a result that’s readable by a single party. Techniques under this umbrella include secret sharing schemes, Enigma, Hawk, or Fully Homomorphic Encryption. TrueBit aims for computation correctness via economics incentive, but it doesn’t actually do much for privacy.

  # **Off-chain constructs**

  One way to tackle privacy is to *not* use the mainnet to do confidential transactions. Logic is implacable. If many parties want to transact privately, they do so in a private network and settle on the mainnet if needed. State channels, plasma, sharding, private consortium networks, or sidechains could fit this description. The computation happens on a separate network and the result ends up on the mainnet. As [uPort](https://www.uport.me/) has pointed out, [off-chain constructs also derisk future attacks.](https://medium.com/uport/privacy-preserving-identity-system-for-ethereum-dapps-a3352d1a93e8) A blockchain is permanent: data encrypted with today’s algorithms may be at risk in a decade!

- Shitcoins

  2017 November Litecoin Dark [http://litecoindark.org/roadmap/](http://litecoindark.org/roadmap/)

  2018 Febuary 26 Litecoin Private [https://bitcointalk.org/index.php?topic=3025236.0](https://bitcointalk.org/index.php?topic=3025236.0) 

  2018 Feb 11 Bitcoin Hush [http://btchush.org](http://btchush.org/)

  Bitcoin Private is a merge fork of Bitcoin and Zclassic.[10][11][12][13] Zclassic is a fork of Zcash, an implementation of the Zerocoin whitepaper. The Zclassic team announced interest in creating a private Bitcoin fork days later.[18] Bitcoin Private's fork snapshot occurred on 28 February 2018, and the mainnet was launched 3 days later. Bitcoin Private (BTCP) is an open-source, peer-to-peer cryptocurrency with the optional ability to keep the sender, receiver, and amount private in a given transaction.[1] This is in contrast to many cryptocurrencies such as Bitcoin, which have a fully transparent transaction history.[3][4][5] [White paper](https://en.wikipedia.org/wiki/White_paper)[btcprivate.org/whitepaper.pdf](https://btcprivate.org/whitepaper.pdf)Initial release1.0.10 / 16 March 2018

  First it was DARKCOIN DRK then becacme DASH [https://en.wikipedia.org/wiki/Dash_(cryptocurrency)](https://en.wikipedia.org/wiki/Dash_(cryptocurrency))

  Zclassic fork: Anonymous Bitcoin is an advancement of the technology of both the Bitcoin and ZClassic blockchain through a co-fork of both cryptocurrencies. [https://www.anonymousbitcoin.io](https://www.anonymousbitcoin.io/)

  [http://blackcoin.co](http://blackcoin.co/)

  Quantum Bitcoin [http://qbtc.world/zh/](http://qbtc.world/zh/)

  BCX [https://www.bcx.org/#applycations](https://www.bcx.org/#applycations)

  Bitcoin Diamond: [http://btcd.io/#/](http://btcd.io/#/)

  Bitcoin Faith [http://www.bitcoinfaith.org](http://www.bitcoinfaith.org/)

  CloackCoin (CLOAK): [https://www.cloakcoin.com](https://www.cloakcoin.com/) 

  StealthCoin (XST): [https://www.stealthcoin.com/](https://www.stealthcoin.com/) 

  Hush (HUSH): [https://myhush.org](https://myhush.org/) 

  Crave Project (CRAVE): [https://craveproject.net](https://craveproject.net/) 

  Bulwark (BWK): [https://bulwarkcrypto.com](https://bulwarkcrypto.com/) 

  InnovaCoin (INN): [https://innovacoin.info](https://innovacoin.info/) 

  Phore (PHR): [https://phore.io](https://phore.io/) 

  Pura (PUR): [https://pura.one/](https://pura.one/) 

  SpectreCoin (XSPEC): [https://spectreproject.io/](https://spectreproject.io/) 

  Sumokoin (SUMO): [https://www.sumokoin.org/](https://www.sumokoin.org/) 

  DeepOnion (ONION): [https://deeponion.org/](https://deeponion.org/) 

  Grin ([http://grin-tech.org/](http://grin-tech.org/)) 

  SolarisCoin (XLR): [https://solariscoin.com/](https://solariscoin.com/) 

  Pure (PURE): [https://purealt.org/](https://purealt.org/) 

  Digital Note (XDN) 

  Shield (XSH) 

  SagaCoin (SAGA) 

  Electroneum (ETN) 

  Platforms & networks

  Verge (VXG): [https://vergecurrency.com](https://vergecurrency.com/) 

  Aion (AION): [https://aion.network/](https://aion.network/) 

  Obsidian (ODN): [https://obsidianplatform.com/](https://obsidianplatform.com/)  based off stratis

[http://mapofcoins.com/bitcoin#](http://mapofcoins.com/bitcoin#)

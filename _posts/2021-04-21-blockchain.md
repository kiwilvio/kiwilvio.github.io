---
layout: article
title: "Notes on Blockchain and Money (MIT 15.S12 Blockchain and Money, Fall 2018)"
tags: blockchain bitcoin finance MIT-OCW
author:
  Quilvio Hernandez
aside:
    toc: true
---

_Disclaimer_: All thoughts are my own. None of the material is mine. Please refer to MIT OpenCourseWare for more details. For this class specifically check out [Blockchain and Money](https://ocw.mit.edu/courses/sloan-school-of-management/15-s12-blockchain-and-money-fall-2018/) for all resources. 

### Introduction (04/21/21)

Readings:  
‘IMF World Bank Comment’ Gensler, The Banker (September 2018).  
‘The blockchain catalyst for change’ Vox (July 16, 2018) 

1. What is blockchain technology and why might it be a catalyst for change for the financial sector?  
Blockchain technology is a software system that powers a "decentralized peer-to-peer form of shared record keeping” [1]. It might be a catalyst for change in the financial sector because of its ability to eliminate unnecesary reconciliations, allow for greater economic activity between individuals without the need for an intermediary, and potential use cases yet to be discovered.


2. What do you as a student wish to learn from this course, ‘Blockchain and Money’?  
An understanding of this new technology and foresee potential effects of it in the financial industry and beyond. 


selected quotes from readings:  
- a new software system that powers a consensus-driven form of shared record keeping – enabling the digital transfer of value in a decentralised manner.
one digital ledger prevents ‘double spending’
- A blockchain is a consensus protocol used to create an append-only log (in the case of Bitcoin, a transaction ledger) that can then be used to form an auditable database (in Bitcoin, a record of who owns which coins). This database is constructed by multiple, possibly distrusting participants and is secured using cryptography so that every entry can be audited and verified.
- In theory, such a system could end the need for costly, time-consuming reconciliation across separate, centralized ledgers run by multiple entities.
 It could also enable new forms of economic activity that were previously impossible in the absence of reliable, intermediating record-keepers.
- We believe this technology could reduce the ingrained ‘cost of trust’ that currently adds friction to commerce and enriches trust-intermediating gatekeepers across the economy.
- They are conceiving of a host of new potential uses: for cross-border payments, in clearing and settlement for financial transactions, for supply-chain management, for device-to-device transactions in the Internet of Things, to create more reliable property and asset registries, to forge portable digital identities, and to improve record-sharing in sensitive areas such as health care.

[1] ‘The blockchain catalyst for change’ Vox (July 16, 2018) 

### Money, Ledgers & Bitcoin (04/22/21)

1. What do the roles (medium of exchange, store of value, & unit of account) and characteristics (durable, portable, divisible, uniform, acceptable & stable) of money mean historically and in today’s digital economy?
Historically, it allows for different forms of trade to develop. There was barter and there were credit systems. Some stone methods allowed for a simple unit of account and medium of exchange to develop, while not being too overly easy to mine. The sticks were also a convenient way to measure credit. As we shift, to a more digital economy (ie. digital yuan and norway) the medium of exchange begins to shift from fiat paper money to fiat digital money. This increases the necessity for strong cryptography fundamentals behind the money because it is no longer something tangible with verifiable factors; but rather, digital indicators. If all goes well, it vastly increases all characteristics of money. A main drawback of digital currency could be that poorer people get left behind. Without a phone, or mean of internet access, it might be hard for them to enable mobile payments or similar methods. 

2. What is fiat currency, what are its ledgers, and how does it fit within the history of money? How does Bitcoin fit within the history of money, the emergence of the Internet and failed attempts of cryptographic payment systems?
Fiat currency is money that is not backed by a commodity. Specifically, it derives its value from government decree. It is the basis of money as a social contract. Ledgers are a record of events. They have become synonymous with accounting records to record transactions. Bitcoin looks to disrupt the traditional ledger system because of its unique distributed ledger system. Because it is a trusted, peer-to-peer network it can potentially cut out the need for a centralized ledger. The bane of many prior attempts of digital currency was the issue of double spending, enterprise buy-in, and the need for centralized ledgers. Blockchain solves all of these. 

- Money is a social and economic consensus
- Ledgers are used record economic activity (transactions and balances)
- Many efforts in ditial currency have failed

### Blockchain Basics & Cryptography (04/29/21)

[Bitcoin: A Peer-to-Peer Electronic Cash System’](https://bitcoin.org/bitcoin.pdf) (PDF) Nakamoto (October 31, 2008)

[‘Blockchain Technology Overview’](https://csrc.nist.gov/CSRC/media/Publications/nistir/8202/draft/documents/nistir8202-draft.pdf) (PDF) National Institute of Standards and Technology (January 2018)  (pages 9 – 23, sections 1 & 2)

['Blockchain 101 — A Visual Demo'](http://blockchain.mit.edu/how-blockchain-works/) Brownworth, MIT (November 5, 2016)

1. What are the design features—cryptography, append-only timestamped blocks, distributed consensus algorithms, and networking—of Bitcoin, the first use case for blockchain technology?  
Bitcoin uses cryptography (hash functions) to map the data contained in the block to generate a hash.  
Benefits of hash functions (paraphrased from Gensler's slides) 
-  extremely efficient 
- deterministic meaning every input maps to exactly one output
- infeasible to determine the data from the hash (preimage resistant, can't brute force)
- infeasible to find x and y such that hash(x)=hash(y)
- slight changes in x cause drastic changes in hash(x).  

Append-only timestamped blocks is why Bitcoin can be trusted (immutability) and helps with the double spending problem. 
The newwork distributed consensus algorithm allows for a peer-to-peer network to validate and protect against any potential attackers. As long as the attacker's CPU doesn't outnumber the hoesnt nodes, the likleihood of success is extremely low. Again, enphasizing the security and trust of Bitcoin without an intermediary.  

2. What are cryptographic hash functions, asymmetric cryptography and digital signatures? How are they utilized to help make blockchain technology verifiable and immutable?  
See above for details on hash functions. Asymmetric cryptography is when data is encrypted with a public key and can only be decrypted with a private key. Digital signatures are generated from the hash and a private key. The signature can be verified with the sender's hash and public key.  
They are used to make blockchain technology because it becomes impracticle to reverse engineer the data contained in the block, and as a result the data is immutable. 

3. What is the double-spending problem and how it is addressed by blockchain technology?  
The double-spending problem is when someone tries to spend a coin twice. This can be by spending it and retrieving it to spend it again, or it can be spending a digital coin when servers are down and trying to spend it again before servers come back online. This is addressed by blockchain because it is a distributed peer-to-peer network. That means each transaction is publicly broadcasted to all nodes. In layman terms, everyone has a copy of the information and through consensus agreement they decided what the right answer (hash) should be and this system protects against double spending.

- Hash function tie blocks together (pointers)
- Change any of the underlying data, the hash changes so easy to see if the data has been tampered with.
- Timestamped append-only logs: immutable record of transactions

### Blockchain Basics & Consensus (05/01/21)

[‘21st Geneva Report on the World Economy - The Impact of Blockchain Technology on Finance: Catalyst for Change’ Chapter 1](https://voxeu.org/content/impact-blockchain-technology-finance-catalyst-change) (pages 1 – 7); Casey, Crane, Gensler, Johnson, and Narula  (July 2018)

[‘Blockchain Technology Overview’](https://csrc.nist.gov/CSRC/media/Publications/nistir/8202/draft/documents/nistir8202-draft.pdf) (PDF) National Institute of Standards and Technology (January 2018)  (pages 23 – 32, sections 3 & 4)

[‘The Byzantine Generals Problem’](https://dl.acm.org/citation.cfm?id=357176) Lamport, Shostak, & Pease; ACM Transactions on Programming Languages and Systems (TOPLAS), 4(3), (July 1982) (required 382-387)

[‘A (Short) Guide to Blockchain Consensus Protocols’](https://www.coindesk.com/short-guide-blockchain-consensus-protocols) CoinDesk (March 4, 2017)

Terms: 
- full node: computer with full blockchain copy and able to validate all transactions
- pruning nodes: prune nodes after validation
- lightweight nodes: store blockchain headers only
- miners: perform proof-of-work and create new blocks (don't need to be full nodes)
- wallet: create key pairs & store, view, send, and receive transactions

1. What is the Byzantine Generals problem? How does proof-of-work and mining in Bitcoin address it? More generally by blockchain technology?  
The heart of the Byzantine Generals problem is determining how to coordinate with unanimous agreement when potential "malicious" agents exist within the network.  
Proof-of-work and mining address it by chaining proof-of-work solutions such that the previous hash, transaction hash, timestamp and an unknown nonce are hashed together to retain the infomration contained in the previous blocks in an efficient manner. Any change in the latest transaction is easy to spot because the hash will be different and the block will be deemed invalid.

2. What other consensus protocols are there? What are some of the tradeoffs of alternative consensus algorithms, proof-of-work, proof-of-stake, etc.?
- Proof-of-stake: There is no coin creation. Validators invest coins in the system and are paid in transaction fees. Potential for double signing.
- Proof-of-activity: Hybrid of proof-of-work and proof-of-stake. Begins as proof-of-work then validators are randomly assigned. Same criticisms as proof-of-work and proof-of-stake.
- Proof-of-burn: People "burn" coins to earn right to mine, and then they're randomly chosen. Constant burn ensures constant decay.
- Proof-of-elapsed time: Essentially a random lottery system. 



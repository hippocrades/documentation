# 🐦 Nightingale

## What is Nightingale? <a href="#what-is-nightingale" id="what-is-nightingale"></a>

#### [Try Demo App](https://emr.hippocrades.com) <a href="#try-demo-app" id="try-demo-app"></a>

Nightingale architecture is designed to be the decentralized, secured, and trusted Health Information Exchange (HIE) platform. It acts as the ‘smart health contract’ where pre-specified rules are set.

It utilizes the zk-SNARKs in a Zero-Knowledge Proof enabled cloud. This is one part of the Nightingale that runs outside of the blockchain. Typically, smart contracts are also stored ‘on chain’ thus concerns on privacy, storage, and run-time constraints arise. Having this setup eliminates mentioned issues while maintaining the integrity and validation the blockchain provides.

Since this is outside the blockchain, the setup allows the chain to be scalable without compromising security and privacy. It remains auditable as transactions, recorded as ‘zk proofs’, are submitted and timestamped in the blockchain.

## Zero-Knowledge <a href="#zero-knowledge" id="zero-knowledge"></a>

![](<../.gitbook/assets/image (8).png>)

### **Zero-Knowledge Proof**

Zero-knowledge (zk) techniques are mathematical methods used to verify things without sharing or revealing underlying data. Zero-knowledge protocols are probabilistic assessments, which means they don't prove something with complete certainty. Instead, they provide small pieces of unlinkable information that can accumulate to show that the validity of an assertion is overwhelmingly probable.

### **zk-SNARKs**

zk-SNARK stands for “Zero-Knowledge Succinct Non-Interactive Argument of Knowledge,” and refers to a proof construction where one can prove possession of certain information, e.g. a secret key, without revealing that information, and without any interaction between the prover and verifier.

### **ZEXE Protocol**

Zexe is a new blockchain design that enables both data privacy and function privacy in addition to succinctness. In other words, not only can transactions be generated offline and efficiently verified on-chain, the time needed to verify the transaction is independent of the time required to do the offline computation to which the prover attests to. It achieves this by introducing a new cryptographic primitive called a Decentralized Private Computation (DPC).

![](<../.gitbook/assets/image (2).png>)

## Two Parts <a href="#two-parts" id="two-parts"></a>

Hippocrades will have two (2) parts, the off-chain, and the on-chain. In doing so, the three components - Decentralization, Privacy, and Programmability are attainable in the setup.

![](<../.gitbook/assets/image (7).png>)

## Off-Chain <a href="#off-chain" id="off-chain"></a>

Fleming information intended for verifying (which was previously accomplished by sharing said information!) will be processed into a zero-knowledge proof (specifically, a zk-SNARK). This is done in a separate RPC-controlled server with access to cryptographic primitives and libraries required to produce the zero-knowledge proof.

Verifiers can use this zero-knowledge proof publicly to affirm truths about the information without requiring the data itself to be shared with them.

For example, a pharmacist may verify that a patient indeed has a prescription for a certain medicine without ever receiving a copy of the prescription. An insurance company may verify that a patient indeed received treatment for a certain diagnosis without ever receiving a copy of either the diagnosis or the invoice for the treatment procedures.

The ZK server then sends this zero-knowledge proof via RPC to the on-chain component of Nightingale.

![](<../.gitbook/assets/image (1).png>)

## On-Chain <a href="#on-chain" id="on-chain"></a>

Zero-knowledge proofs from the off-chain component of Nightingale are received via RPC and encoded into a transaction on the blockchain. This step confers blockchain’s advantages of integrity, immutability, decentralization, and resilience to forgery to all zero-knowledge proofs generated for Fleming information.

Nightingale’s blockchain is flexible in its requirements, only requiring Turing- complete smart contracts to be supported (of which there are numerous available on the market today, such as Ethereum or Cardano). To prepare any blockchain for connection to Nightingale, there are two components:

A thin RPC-ready layer to expose blockchain operations via RPC (such as creating transactions and finding their blocks on the chain) A set of general smart contracts to cover Nightingale’s use cases and domain

Because of the clear separation of concerns between the off-chain and on-chain components (communicating only via RPC), Nightingale may be deployed onto any chain (and even several chains!) by developing only the above two (2) components, instead of re-outfitting the entire architecture from scratch.

## Status: POC DONE <a href="#status-poc-done" id="status-poc-done"></a>

Proof of Concept (POC), DONE. Request Access at [Hippocrades Community](https://github.com/hapihumans/hippocrades-community/blob/main/README.md).

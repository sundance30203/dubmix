dubmix
========

Ubiquitous Decentralized Bitcoin Mixing Implementation

The invention of Bitcoin has brought new forms of financial practices, actors, and services. There is often sensitivity (in the form of operational risks and risks to client confidentiality and personal financial privacy) related to the information that is both directly available on the blockchain and deducible through transaction graph analysis by unrelated third parties (adversaries). The many examples include the following:
- Bitcoin exchanges, payment processors, and some online wallets have custodial responsibilities, whereby they receive control of bitcoins from clients and are responsible for holding or performing actions on behalf of the client. 
- Companies that pay its employees in bitcoins will want to obscure the amounts given to particular employees. 
- Political and membership-based organizations may want to keep their membership lists private while receiving fees/donations from members' Bitcoin addresses.

The Bitcoin protocol, aptly, neither hinders nor directly supports this type of transactional obfuscation. Additional technical mechanisms are needed in order to give these new practices the necessary confidentiality protection. Bitcoin mixing is a technique introduced by the community to mechanize such protection with the aim to render deductible information less useful and/or more expensive to obtain. This work aims to build on this approach by introducing a new mixing algorithm based on existing Bitcoin functionality. 

This work aims to make it easier for actors to engage in mixing with large anonymity sets, where the input amounts are not apriori known or controlled. The known decentralized bitcoin mixing algorithms either require the input amounts to be equal or their anonymity strongly depends on that being the case. For example, CoinSwap  and CoinShuffle  assume equal bitcoin amounts. CoinJoin  is subject to subset-sum attacks if the amounts are different. It should be noted that transactions resulting from mixing operations {\em are distinguishable} from regular transactions (with non-negligible advantage), despite the historical aim to mask mix transactions as regular transactions. The size of the anonymity set of a mix operation is therefore limited by the number of addresses {\em that participate in the mixing operation} and not the total number of addresses that are active on the Bitcoin network at the time of the operation. Therefore, the effectiveness of mixing depends on our ability to perform mixes on large numbers of addresses. We present an algorithm that facilitates large-scale mixing on disparate inputs amounts so as to allow actors to engage more readily with large anonymity sets than previously possible.

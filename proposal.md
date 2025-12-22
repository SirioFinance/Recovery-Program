# Recovery Methodology Proposal

## INDEX

* Introduction
* Impact Summary
* HBAR, HBARx, SAUCE, xSAUCE, NFT Holders Distribution
* HSuite Distribution
* Recovery Methodology
* Nysa: The New Protocol
* TL;DR

---

## 1. Introduction

Dear Sirio Community,

On February 1st, 2025, Sirio Finance experienced a severe security incident that resulted in the unauthorized exploitation of user funds. A comprehensive forensic analysis was conducted by both our internal team and external auditors. The full post-mortem report is available here: [link].

With this DAO proposal, we aim to present a transparent, equitable, and legally sound Recovery Plan for all affected participants. The proposed approach takes into account the technical constraints arising from the incident, the ethical implications for the community, and the most relevant principles of applicable law.

The primary objective is to distribute the remaining recoverable assets wherever technically feasible. Where direct restitution is not possible due to execution-level constraints, affected users will receive an allocation of Nysa Tokens, the native token of Nysa, Sirio’s successor protocol, calculated proportionally to their Net Loss.

This includes:

* users who supplied assets to the protocol, and
* holders of Cosmic Cyphers and Nebula Genesis NFTs.

This proposal will remain open for voting for 20 days, starting on **December 22th, 2025**, and will be considered approved only upon reaching the required **85% quorum**.

Upon approval, the Recovery Portal will be deployed, enabling users to claim the leftover assets in accordance with the DAO-approved methodology and the Terms of Service (ToS) published on the portal.

---

## 2. Impact Summary

The remaining asset pool currently consists of:

* **HBAR:** 48,290
* **HBARX:** 2,430
* **SAUCE:** 378,000
* **HSUITE:** 78,433,000
* **XSAUCE:** 713

On April 25th, approximately 78 million HSUITE tokens were successfully recovered through a technical workaround. These tokens are securely held in wallet `0.0.9296474-fncev`, the same wallet used for minting Sirio DAO Access NFTs.

By contrast, the withdrawal and supply execution logic of the remaining pools was irreversibly compromised by the exploit.

---

## 3. HBAR, HBARx, SAUCE, xSAUCE, NFT Holders

### Distribution Execution Constraints

While we can ensure a more flexible and DAO-aligned distribution strategy for HSUITE (as detailed in the next section — HSUITE Distribution Logic), we are technically unable to apply the same logic to the other tokens.

The exploit irreversibly compromised the protocol’s withdrawal and settlement execution logic, which previously governed how redeemable balances were converted into on-chain transfers. While the accounting layer remains reconstructable off-chain, the smart contract mechanisms responsible for enforcing proportionality, sequencing, and invariant preservation are no longer reliable.

When provided with the full list of supplier wallet addresses, an off-chain script can compute the exact redeemable balances for HBAR, HBARx, SAUCE, USDC, PACK, and xSAUCE. These balances will be publicly disclosed in the Results section and represent each user’s maximum theoretical entitlement at the time of the exploit.

However, due to the objective impossibility of guaranteeing a correct, deterministic, and interference-free execution of withdrawals at the smart contract level, Sirio cannot warrant that any direct on-chain redemption mechanism would preserve balance coherence or equitable outcomes for all participants.

Due to the incident, it is no longer possible to guarantee the same withdrawal process that existed before the exploit. Even though the protocol was developed following reasonable diligence and industry standards, the attack irreversibly affected the way withdrawals are executed.

Sirio is a non-custodial and permissionless protocol. This means that the team does not have direct control over user funds and cannot modify, override, or rebuild the compromised withdrawal logic on behalf of users.

Where some assets are still available on-chain, users will nonetheless be able to attempt to withdraw them directly from the protocol. These attempts will be based on reconstructed and verified balance data, which is publicly available in the following snapshot:
[https://github.com/SirioFinance/Recovery-Program/blob/main/redeemable_results.json](https://github.com/SirioFinance/Recovery-Program/blob/main/redeemable_results.json)

It is important to clearly state that, due to the compromised state of the system, Sirio cannot guarantee that every withdrawal attempt will be successful, fully accurate, or fair across all users. Withdrawals are therefore made voluntarily and at the user’s own risk.

By participating in the recovery process — whether by submitting a claim, interacting with the Recovery Portal, or attempting a withdrawal — users explicitly accept these conditions under the Terms of Service that will be published on the Recovery Portal and can be accepted or declined once live.

By doing so, users acknowledge that their balances have been correctly reconstructed off-chain, that the original withdrawal mechanism is no longer technically reliable, and that attempting to withdraw remaining assets represents the only realistically available path to withdraw leftover funds.

Finally, should additional actions be successfully carried out in the future that result in the recovery or withdrawal of further remaining funds after the Recovery Portal phase, such funds will be subject to a new DAO proposal, through which the community will decide whether they should be used for.

---

## 4. HSUITE Distribution Logic

The issue of distributing HSUITE tokens involves significant legal complexity, as it lies at the intersection of traditional Italian insolvency law and DeFi—a domain that currently lacks a comprehensive and dedicated regulatory framework.

Indeed, the moment of the protocol’s insolvency (i.e., the occurrence of the exploit) differs from the moment the protocol formally declared its state of failure (by freezing smart contracts and disabling the front-end interface). The legal question therefore arises: how should the remaining funds be distributed under Italian law?

Before addressing this matter, it is essential to clarify several preliminary aspects:

1. Italian jurisprudence, in the absence of an organic legislative framework, tends to qualify crypto-assets (including tokens) either as intangible goods or financial instruments, depending on their function. Within a lending protocol, deposited tokens may be assimilated to an irregular deposit (**Article 1782 of the Italian Civil Code**), whereby the depositary (i.e., the protocol) acquires ownership of the fungible items and is obliged to return an equivalent amount of the same type and quality.
2. A DeFi protocol is not a company or a traditional legal entity. It is often governed by a DAO (Decentralized Autonomous Organization) or directly by smart contracts. The absence of a central legal personality makes the direct application of business crisis laws challenging. However, a judge may reasonably attempt to identify the individuals or entities (e.g., developers, the DAO, or associated legal entities) who de facto manage the protocol, in order to assign responsibility.
3. The so-called "bankruptcy declaration" is a unilateral act issued by the project team, and not a formal bankruptcy under Italian law—which can only be declared by a judicial authority. The legally relevant moment is the actual onset of insolvency, meaning the inability to regularly meet one’s obligations. In this case, insolvency most likely occurred at 8:00 a.m., the time of the exploit, when the protocol's asset base became insufficient to guarantee the repayment of creditors.
4. The relevant Italian legislative framework in cases of business crisis and insolvency is the **Code of Business Crisis and Insolvency (Legislative Decree No. 14/2019)**. While designed for traditional enterprises, its general principles may be analogically applied in this context.

The core principle governing asset distribution in insolvency proceedings is the **Par Condicio Creditorum (Article 2741 of the Italian Civil Code)**, which establishes that all creditors have an equal right to be satisfied from the debtor's assets.

Applying this principle to the present case leads to the following plausible outcome:

* If a judge were to analogically apply the rules governing judicial liquidation (the modern equivalent of bankruptcy), all creditors who arose prior to the formal opening of the insolvency procedure should be treated equally.
* **All Suppliers Qualify as Unsecured Creditors:** Both those who supplied liquidity prior to the exploit and those who deposited tokens afterward are, for all intents and purposes, unsecured creditors of the protocol. They hold a claim for the restitution of their tokens.
* **Irrelevance of the Deposit Timing (Pre- or Post-Exploit):** In determining the order of creditor satisfaction, the precise moment when a claim arises is generally irrelevant. What matters is that the claim existed prior to the commencement of the insolvency procedure. Therefore, residual funds should be distributed proportionally among all suppliers based on the amount of their respective claims (i.e., the value of tokens deposited). No legal distinction exists between "pre-exploit" and "post-exploit" creditors.

**Relevant Legal References:**

* **Article 2741 of the Italian Civil Code** (Concurrence of Creditors and Priority Rights): "Creditors have an equal right to be satisfied from the debtor’s assets, without prejudice to legitimate causes of preference. Legitimate causes of preference include privileges, pledges, and mortgages."
* **Articles 150 et seq. of the Code of Business Crisis and Insolvency**: These govern the verification of claims and the formation of the schedule of liabilities, listing all claims admitted to the procedure.

Given the current state of Italian legislation—and in the absence of DeFi-specific regulations—the most probable and legally sound interpretation is the analogical application of the principle of Par Condicio Creditorum.

As a result, the distribution of the remaining assets should be conducted among all liquidity providers, regardless of whether their deposit occurred before or after the exploit. The allocation should be proportional to the value of each creditor’s claim.

There is no legal basis under Italian law to favor “post-exploit” providers or to grant them a greater share to the detriment of others. All are considered unsecured creditors (chirografari) with equal standing in relation to the protocol’s remaining asset pool. The only exception that could potentially favor post-exploit suppliers would be if it could be demonstrated that their contributions qualify as super-priority claims (crediti prededucibili)—that is, claims arising in connection with the preservation or management of the asset pool during the insolvency process. However, this exception is unlikely to apply in the case of a DeFi protocol that was already compromised at the time of those contributions.

Furthermore, to maximize the legal robustness of the recovery process and align with the procedural safeguards provided by Italian law, the distribution will not be immediate. We voluntarily adopt the principles set forth in **Article 220 of the Code of Business Crisis and Insolvency (CCII)** regarding the distribution of assets.

This article mandates that, before any payment is made, a distribution project must be communicated to all creditors, who are then granted a statutory term of 15 days to submit any observations or complaints. Only after this period has elapsed without objections does the plan become final and executable.

Consequently, the actual distribution of funds will occur approximately 30 days after the publication of the final allocation list. This timeframe accounts for the 15-day objection window mandated by the principles of the CCII, combined with the necessary technical and administrative time to finalize calculations and verify wallet addresses, ensuring a transparent and compliant process.

The eventual distribution of HSUITE tokens to suppliers, based on these principles, will be executed according to the specific Terms of Service (ToS) published on the Recovery Portal, that users will be able to accept or decline once live.

Finally, should additional actions be successfully carried out in the future that result in the recovery or withdrawal of further remaining funds after the Recovery Portal phase, such funds will be subject to a new DAO proposal, through which the community will decide whether they should be used for.

---

## 5. Recovery Methodology

As many of you are already aware, the malicious attack we suffered drained the vast majority of the liquidity we were managing. We fully understand the frustration felt by all investors, suppliers, and partners involved in this unfortunate situation. As previously mentioned, we were victims of this attack just as much as everyone else.

As has been the case for many other DeFi protocols, losing the support of certain partners—who completely abandoned us during the most critical moments—could have led us to take the easier path: distribute the remaining funds and shut down the platform. However, after months of careful thought and hard work on an alternative, we decided that we could never abandon our users or disregard the powerful technological foundation behind Sirio.

For this reason, we have chosen to deploy on a new ecosystem and proceed with a full rebranding.

All unrecoverable user funds (i.e. whatever users are not able to redeem from the current Recovery Portal) will be converted into an allocation of tokens from the new platform proportionally to the amount lost among suppliers and NFT Holders. This represents, in our view, the most meaningful way to show our gratitude to the community. All asset claims (HBAR, HSUITE, SAUCE, etc.) will be managed exclusively through the dedicated Recovery Portal following the Terms of Service made available therein.

The methodology for distributing the remaining assets and allocating tokens from the new project, called Nysa, depends on each user's snapshot at the time of the exploit (Supply & Borrow Balance) and the amount of assets they will be able to withdraw. For this reason, the following factors are identified for each user:

* **TOTAL_SUPPLIED:** The total value of supplied assets in HBAR.
* **TOTAL_BORROWINGS:** The total value of borrowed assets in HBAR.
* **TOTAL_WITHDRAWALS:** The total value of withdrawn assets in HBAR, at the time the Recovery Portal eventually goes live.
* **TOTAL_NFT_VALUE_HELD:** The total value of NFT Held by the account at the time of the snapshot, dated at 10 November 2025, calculated as the HBAR Mint Price.
* **NET_LOSS:** The total loss in HBAR for each user, calculated as follows:

### Calculation and Allocation of the NET Loss

The NET Loss is the quantity of HBAR tokenized via NFT that will be used to proportionally define the allocation of the new Nysa tokens and the distribution of remaining assets for all protocol assets.

Specifically, the value of the NET Loss will be the combination of the Total Balance from the snapshot of every token (HBAR, HBARx, USDC, PACK, SAUCE, xSAUCE), valued at the price of HBAR at the moment of the exploit.

Furthermore, the NET Loss calculation will also account for the Holders of the Cosmic Cyphers and Nebula Genesis NFT collections. For each of these holders, the initial mint value of each NFT held will be considered as part of their NET Loss.

The NET LOSS will be tokenized through an NFT on Hedera, which users will be able to use in two ways:

1. Hold the NFT and receive an allocation of tokens or revenues, based on the outcome of a new proposal that will be shared later.
2. Immediately profit on the value by selling their NFT on a secondary marketplace such as SentX at the price given by the market. For this purpose, we propose to apply a 5% royalty, which revenues will be used to fund the proper deployment and maintenance of the new Protocol.

---

## 6. New Protocol - Nysa

Sirio Finance is evolving into Nysa, a new and enhanced lending protocol that will be deployed on Linea, based on an Aave V3 fork and enhanced by AI-Agents.

We aim to be the first Lending protocol to list the native LINEA token. Moreover, we will feature a wide variety of Tokens (Both Native and Liquid Staking Versions) and Stablecoins to be listed right from launch.

Security is our absolute priority. The Protocol will undergo rigorous Audits, Penetration Tests, and will implement a Sentinel Mechanism. The latter is an advanced security feature which, upon the occurrence of specific critical events, will automatically block certain categories of operations to prevent losses.

Moreover, to increase revenues and support financial sustainability of the protocol, we are going to promote a suit of AI Agents able to run your Web3 Project. We are going to promote a referral system where everyone can sell those services and get a generous fee on top of the sale.

We are proud to announce that, once we receive the final audit report, we will have direct support from the official Linea channels. Until then, we are working intensively to build our Networking and fundamental partnerships within the ecosystem. The rebrand will happen after the Recovery Portal launch.

---

## 7. TL;DR

On February 1st, 2025, Sirio Finance suffered a major security exploit that irreversibly compromised the protocol’s withdrawal logic and led to significant user losses. This DAO proposal defines a transparent and legally grounded recovery plan for all affected users and NFT holders.

Some assets are still available on-chain. Users will be able to attempt to withdraw these remaining assets directly from the protocol, based on reconstructed balance data published publicly. However, due to the compromised state of the system, withdrawals are not guaranteed to work correctly or fairly and are performed voluntarily, at the user’s own risk.

Approximately 78 million HSUITE tokens were successfully recovered and will be redistributed according to Italian insolvency principles. All suppliers are treated equally as unsecured creditors, regardless of whether they deposited before or after the exploit, and HSUITE will be allocated proportionally after a transparency and objection period.

Any unrecoverable value — meaning assets users are unable to withdraw through the Recovery Portal — will be compensated through an allocation of tokens from Nysa, Sirio’s successor protocol. Losses are calculated via a clear NET LOSS formula that accounts for supplied assets, borrowings, withdrawals, and NFT holdings, all valued in HBAR at the time of the exploit.

The NET LOSS will be tokenized via an NFT on Hedera, which users can either hold for future allocations or sell on secondary markets. A small royalty will fund the deployment and maintenance of the new protocol.

If additional funds are recovered in the future after the Recovery Portal phase, their use will be decided through a new DAO proposal, allowing the community to choose between further refund processes or supporting the development of Nysa.

Nysa will launch on Linea as a new, audited, and more secure lending protocol enhanced with AI agents, marking the long-term continuation of the project after the recovery process.

---

**Desideri che io verifichi la correttezza della formula LaTeX o che esporti questo testo in un altro formato?**

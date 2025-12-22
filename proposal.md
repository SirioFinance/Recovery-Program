# Recovery Methodology Proposal

## INDEX

1. [Introduction](https://www.google.com/search?q=%231-introduction)
2. [Impact Summary](https://www.google.com/search?q=%232-impact-summary-)
3. [HBAR, HBARx, SAUCE, xSAUCE, NFT Holders](https://www.google.com/search?q=%233-hbar-hbarx-sauce-xsauce-nft-holders)
4. [HSUITE Distribution Logic](https://www.google.com/search?q=%234-hsuite-distribution-logic)
5. [Recovery Methodology](https://www.google.com/search?q=%235-recovery-methodology)
6. [New Protocol - Nysa](https://www.google.com/search?q=%236-new-protocol---nysa)
7. [TL;DR](https://www.google.com/search?q=%237-tldr)

---

## 1. Introduction

Dear Sirio Community,

On **February 1st, 2025**, Sirio Finance experienced a severe security incident that resulted in the unauthorized exploitation of user funds. A comprehensive forensic analysis was conducted by both our internal team and external auditors. The full post-mortem report is available here: [link].

With this DAO proposal, we aim to present a transparent, equitable, and legally sound Recovery Plan. The primary objective is to distribute the remaining recoverable assets wherever technically feasible. Where direct restitution is not possible due to execution-level constraints, affected users will receive an allocation of **Nysa Tokens** (Sirio’s successor protocol), calculated proportionally to their **Net Loss**.

**This includes:**

* Users who supplied assets to the protocol.
* Holders of Cosmic Cyphers and Nebula Genesis NFTs.

> **Voting Details:** This proposal will remain open for voting for 20 days, starting on **December 22nd, 2025**, and will be considered approved only upon reaching an **85% quorum**.

---

## 2. Impact Summary 📉

*Note: All net losses are calculated in HBAR, using the exchange rate at the time of the exploit.*

**Remaining Asset Pool:**

* **HBAR:** 48,290
* **HBARX:** 2,430
* **SAUCE:** 378,000
* **HSUITE:** 78,433,000
* **XSAUCE:** 713

On April 25th, approximately 78 million **HSUITE** tokens were successfully recovered and are securely held in wallet `0.0.9296474-fncev`. By contrast, the withdrawal and supply execution logic of the remaining pools was irreversibly compromised by the exploit.

---

## 3. HBAR, HBARx, SAUCE, xSAUCE, NFT Holders

### Distribution Execution Constraints & Technical Risks

The exploit irreversibly compromised the protocol’s withdrawal and settlement logic. While the accounting layer remains reconstructable off-chain, the smart contract mechanisms responsible for enforcing proportionality and invariant preservation are no longer reliable.

**Important Notice on Manual Withdrawals:**
Where assets are still available on-chain, users will be able to attempt to withdraw them directly. These attempts will be based on reconstructed and verified balance data available here: [Redeemable Results JSON](https://github.com/SirioFinance/Recovery-Program/blob/main/redeemable_results.json).

**However, Sirio cannot warrant or guarantee:**

* That every withdrawal attempt will be successful.
* That the outcome will be fully accurate or deterministic.
* That equitable outcomes will be preserved for all participants at the smart contract level.

### Legal Standpoint

* **Non-Custodial Nature:** Sirio is a permissionless protocol; the team does not have technical control to override or rebuild the compromised logic on behalf of users.
* **Voluntary Action:** Withdrawals are made voluntarily and at the **user’s own risk**. By interacting with the Recovery Portal, users acknowledge that the original mechanism is unreliable and that this represents the only feasible path available.
* **Terms of Service:** Participation implies acceptance of the ToS, confirming that balances have been correctly reconstructed off-chain.

---

## 4. HSUITE Distribution Logic

The distribution of HSUITE tokens follows the principles of **Italian insolvency law** (*Par Condicio Creditorum*).

* **Legal Qualification:** Deposited tokens are assimilated to an **irregular deposit (Art. 1782 Civil Code)**.
* **Insolvency Timing:** The legally relevant moment is the onset of insolvency (8:00 a.m. on the day of the exploit).
* **Equal Treatment:** Under the *Code of Business Crisis and Insolvency (Legislative Decree No. 14/2019)*, all suppliers (pre- and post-exploit) qualify as **unsecured creditors** (*chirografari*). There is no legal basis to favor "post-exploit" providers.

**Distribution Process:**
Following **Article 220 of the CCII**, we adopt a transparency period.

1. **Communication:** A distribution project is shared with all creditors.
2. **Objection Window:** A **15-day term** to submit observations.
3. **Execution:** Distribution occurs approximately **30 days** after the final list publication.

*Note: Any further funds recovered after this phase will be subject to a new DAO proposal.*

---

## 5. Recovery Methodology

All unrecoverable user funds (assets that users are unable to redeem from the Recovery Portal) will be converted into an allocation of **Nysa tokens**.

### Net Loss Calculation

Factors identified for each user:

* **TOTAL_SUPPLIED / TOTAL_BORROWINGS / TOTAL_WITHDRAWALS** (at the time the Portal goes live).
* **TOTAL_NFT_VALUE_HELD:** Mint price of NFTs held on November 10, 2025.

**Formula:**


### Tokenization via NFT

The **NET LOSS** will be tokenized through an NFT on Hedera, allowing users to:

1. **Hold:** Receive an allocation of tokens or revenues from Nysa.
2. **Trade:** Sell on secondary markets (e.g., SentX). A **5% royalty** will fund the new protocol’s maintenance.

---

## 6. New Protocol - Nysa

Sirio Finance is evolving into **Nysa**, a next-generation lending protocol on **Linea**.

* **Tech Stack:** Based on an Aave V3 fork, enhanced by **AI-Agents**.
* **Assets:** Support for native LINEA, Liquid Staking tokens, and Stablecoins.
* **Security:** Rigorous Audits, Penetration Tests, and a **Sentinel Mechanism** to block critical operations during anomalies.
* **Sustainability:** AI Agents services with a referral system to generate protocol revenue.

---

## 7. TL;DR

* **On-Chain Assets:** Users can attempt to withdraw remaining assets "as-is" from the compromised contracts at their own risk.
* **HSUITE:** Successfully recovered and redistributed proportionally among all suppliers based on Italian insolvency principles.
* **Compensation:** Unrecoverable losses are calculated via a **NET LOSS** formula and tokenized via **NFTs**.
* **Nysa:** Holders of the Loss-NFT will receive tokens of the new AI-enhanced protocol on Linea.
* **Future Recovery:** Any additional funds recovered post-portal will be managed via a new DAO vote.
* **Voluntary:** Participation is voluntary via the Recovery Portal and subject to the published Terms of Service.

---

**Vuoi procedere con la creazione di una bozza per i Terms of Service (ToS) menzionati nel documento?**

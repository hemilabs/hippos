# HIPPO-002

```
HIPPO: 2
Title: Hemi Economic Model
Author: Jeff Garzik <jeff@hemi.xyz>
        Max Sanchez <max@hemi.xyz>
Comments-Summary: No comments yet.
Status: Active
Type: Network
Created: 2025-10-24
```

## Background and Motivation
The Hemi blockchain connects Bitcoin and Ethereum - enabling new  
economic opportunities for assets across the two largest blockchain  
ecosystems.

The economic model outlined in this HIPPO is designed to:
- Connect $HEMI to the economic value created by the Hemi ecosystem
- Ensure veHEMI provides adequate economic security to support  
  network decentralization
- Stimulate BTC-based economic activity and produce sustainable yield
- Increase liquidity across Hemi's DeFi protocols
- Build long-term protocol-owned liquidity
- Promote incentive alignment between Hemi and users seeking BTC yield

Fundamentally, the Hemi protocol has **inflows** of fees that are generated  
across a variety of features, and **outflows** that are costs paid by the  
protocol for successful operation.

As Hemi evolves, there will be many sources of protocol fees:
- Gas/transaction fees
- hBitVM covenant emulation and operator fees
- PoP security inheritance fees
- Chainbuilder shared sequencing & DA fees
- Cross-chain liquidity system fees
- 3rd party economic security fees

Most of the above systems will share the collected fees between the  
participants running the service and the protocol itself; for example  
a portion of PoP security inheritance fees paid by L3s, etc. will go to  
the sequencer who builds the Hemi block that includes the PoP publication.

This design is concerned with the allocation of the **net** (or excess)  
fees of the protocol to maximize value for the Hemi ecosystem; building   
long-term sustainable and predictable economics.

In this pursuit, this economic model is primarily centered around veHEMI  
(the native staking system for $HEMI), which consists of participants  
incentive-aligned with the long term success of the Hemi protocol and who  
will play an increasingly critical role in Hemi's decentralization.

As part of Hemi's focus on BTC DeFi, this economic model also incentivizes  
hemiBTC staking, and introduces a dual-staking (veHEMI + staked hemiBTC)  
system to further increase incentive alignment between BTC yield and the  
Hemi protocol.


## Design Components
The complete design consists of the following components:
- **Short-Term Pool (STP)**: A pool of assets that collects fees  
  and smooths out the distribution of these fees to other components,  
  while earning yield with short-term / liquid strategies
- **Protocol-Owned Liquidity (POL) Treasury**: A pool of assets owned  
  by the protocol, which serves to provide liquidity to Hemi and earn  
  sustainable yield with the ability to engage with long-term strategies
- **Protocol Governance**: Voting system based on veHEMI stake weight to  
  handle decentralized management of the protocol
- **Economic Governance**: Voting system based on veHEMI stake weight  
  specifically for directing incentives and allocations of the POL treasury
- **Vote Marketplace**: Marketplace for users/protocols/etc. to  
  incentivize economic governance participants to vote for specific  
  allocations of incentives or POL assets

And this system ultimately powers the following economic outcomes:
- **$HEMI Burns**: A portion of net fees is converted to $HEMI and burnt  
  similar to the EIP-1559 mechanic of Ethereum
- **veHEMI Base Staking Incentives**: Fees for all veHEMI position  
  holders, distributed based on veHEMI stake weight
- **Governance Incentives**: Incentives for users to participate in  
  protocol governance, either directly or by or delegation
- **Vote Marketplace Incentives**: Incentives provided by third-parties  
  in exchange for users voting for specific economic model outcomes  
  in the economic vote marketplace
- **hemiBTC Staking Incentives**: Incentives directed towards stakers  
  of hemiBTC to attract BTC liquidity to Hemi
- **Dual-Staking Incentives**: Incentives directed towards stakers of  
  both hemiBTC and $HEMI (as veHEMI) to promote additional incentive  
  alignment
- **Liquidity Incentives**: Incentives directed towards parties that  
  deploy liquidity in specific assets to specific protocols; determined  
  by veHEMI stakers' votes in the economic governance system

Collectively, these components create a sustainable economic system  
that captures value created by the Hemi ecosystem and redirects it towards  
building sustainable yield sources and providing incentives that encourage  
behaviors that generate more value creation.

## veHEMI Background
Vote-escrow $HEMI (veHEMI) is the protocol-native $HEMI staking system,  
used for governance, economic security for decentralized components of  
the protocol, and directing protocol asset flows within this economic model.

Users stake $HEMI for a period of 12 days to 4 years, and receive an NFT  
representing their staked position. Longer lockups receive higher weight  
in the system, representing the increased incentive alignment with the  
long-term success of Hemi.

The weight of a position is calculated based on its remaining lockup time;  
for example, a position with 4 years remaining has twice the weight of a   
position with 2 years remaining, etc. Users can extend the lockups on  
existing positions to increase their weight and incentives.

As Hemi evolves, owners of veHEMI positions will earn additional incentives for:
- Participating in governance votes (or delegating)
- Operating decentralized infrastructure:
    - Block sequencing
    - Data publication to Ethereum (DA & state roots)
    - hBitVM covenant emulation and vault operation
    - Providing shared sequencing and DA services to Chainbuilder chains
- Providing cross-chain liquidity
- Providing economic security to third-party protocols
- Receiving yield from the vote market for directing incentives

When veHemi positions are used for economic security (decentralized  
infrastructure, cross-chain liquidity, and securing third-party  
protocols), they are subject to being slashed for misbehavior.  
Depending on the specific security needs of each protocol, the  
underlying $HEMI in the slashed position may be burnt, sent to  
either the STP or POL, and/or distributed to other protocol  
participants.

## Phases of Hemi Economic Model
The Hemi Economic Model will be implemented across several different  
phases, each building upon the last to further decentralize control of  
the economic model, as well as introduce new mechanics that serve to  
incentivize more types of activity and create more incentive alignment  
between the participants in the Hemi ecosystem.

The phases of the economic model will be:
- **Phase 1 (Today):** Protocol Fees as veHEMI Incentives & Burn
    - **Mechanics:**
        - Protocol fees are converted into $HEMI and hemiBTC
        - Portion of $HEMI is burnt
        - Remainder of $HEMI and all hemiBTC is distributed to veHEMI  
          stakers based on their relative vote weight
    - **Outcomes:**
        - Connect value creation of the Hemi network to $HEMI
        - Long-term incentive alignment of $HEMI holders with  
          success of the protocol
        - Begin increasing veHEMI staking to grow available economic  
          security in preparation of launching features
- **Phase 2:** Automated Short-Term Pool (STP) and  
  Protocol-Owned-Liquidity (POL) Treasury
    - **Mechanics:**
        - Every two weeks:
            - Net protocol fees after $HEMI purchase & burn is sent
              to STP
            - 1/13th of STP's total assets are distributed amongst:
                - Governance Participation Incentives
                - veHEMI Staking Incentives
                - Liquidity Incentives
                - POL Treasury
            - Portion of POL Treasury yield is distributed amongst:
                - Reallocations back into POL Treasury positions
                - STP
    - **Outcomes:**
        - STP smooths out short-term protocol fee variability, creating  
          stability/predictability for incentives
        - Protocol accrues permanent liquidity and an evergreen yield  
          source, which returns value to the STP and ultimately future
          incentives
- **Phase 3:** Decentralized Incentive Voting & Vote Market
    - **Mechanics:**
        - Every two weeks:
            - Anyone can add vote market incentives to be distributed to:
                - veHEMI stakers who vote for a particular POL Treasury allocation
                - veHEMI stakers who vote for a particular liquidity incentives
                  allocation
            - veHEMI stakers vote on:
                - POL Treasury allocations (and receive vote market rewards)
                - liquidity incentive allocations (and receive vote market rewards)
    - **Outcomes:**
        - Allocation of POL treasury and liquidity incentives generates
          additional yield for veHEMI
        - Control of POL Treasury and Liquidity Incentives becomes more decentralized
- **Phase 4:** Dual-Staking
    - **Mechanics:**
        - Anyone can stake hemiBTC, which is used to increase BTC DeFi liquidity
        - Every two weeks:
            - A portion of the STP outflow is distributed to hemiBTC stakers
            - A portion of the STP outflow is distributed to hemiBTC + veHEMI stakers,   
              based on the stakign ratio of hemiBTC : veHEMI
    - **Outcomes:**
        - Increases BTC liquidity in Hemi's BTC DeFi ecosystem
        - Creates sustainable yield for BTC
        - Economically aligns BTC stakers with the success of Hemi

## Phase 1 Specification Details
As of October 30 2025, approximately 8.26 ETH in excess protocol fees have been  
converted to approximately 0.2445 hemiBTC and approximately 100,320.689 $HEMI  
which will be distributed to veHEMI stakers active from August 30th at 12:00am GMT  
(unix epoch 1756512000) to October 30th at 12:00am GMT (unix epoch 1761782400),  
inclusive.

Those rewards will be claimable by users through a claim contract, based on the  
user's veHEMI position's weight relative to the total veHEMI staking weight on each  
day (86400 seconds) starting at timestamp 1756512000 through timestamp 1761782400;  
a total of 62 days. These rewards will be distributed linearly over the 62 days.

Additionally, approximately 1.51 additional ETH has been converted to 98,216.75  
$HEMI which has been burnt.

The details for these transactions can be found here:
 - Conversion of 7 ETH to 0.2445 hemiBTC:
   - [https://explorer.hemi.xyz/tx/0x205482fccd22cb2996699d0784174c2384452c197cb348116a82b4b9fbd81d78](https://explorer.hemi.xyz/tx/0x205482fccd22cb2996699d0784174c2384452c197cb348116a82b4b9fbd81d78)
   - [https://explorer.hemi.xyz/tx/0xbf973ecfcc9d44987adff604d97c4642e8f10e9f92ae7c2c7f08243e111d2fc5](https://explorer.hemi.xyz/tx/0xbf973ecfcc9d44987adff604d97c4642e8f10e9f92ae7c2c7f08243e111d2fc5)
   - [https://explorer.hemi.xyz/tx/0xec4fe936a5f6f737cb32584f96274abe96f13137ce67a56c00daa028c9d96644](https://explorer.hemi.xyz/tx/0xec4fe936a5f6f737cb32584f96274abe96f13137ce67a56c00daa028c9d96644)
 - Conversion of 2.77 ETH to 198,537.44 HEMI:
   - [https://explorer.hemi.xyz/tx/0xf8e13b27f9085f48d66bde0ba68827c0382e9bade37aabef29ed01bb5ca81e39](https://explorer.hemi.xyz/tx/0xf8e13b27f9085f48d66bde0ba68827c0382e9bade37aabef29ed01bb5ca81e39)
   - [https://explorer.hemi.xyz/tx/0xdb2d914bc31b8c52109180550a53115dcb752bb16a7d8c2b5acd9be9fa383861](https://explorer.hemi.xyz/tx/0xdb2d914bc31b8c52109180550a53115dcb752bb16a7d8c2b5acd9be9fa383861)
 - Burning of 98,216.75 HEMI:
   - [https://etherscan.io/tx/0x7aa573ea8dbf20ace5477d2631609cce53990aba7f5dfbe9b336b9c22a7c751c](https://etherscan.io/tx/0x7aa573ea8dbf20ace5477d2631609cce53990aba7f5dfbe9b336b9c22a7c751c)

Moving forward, excess protocol fees will be routinely collected and converted  
to $HEMI and hemiBTC to be distributed as veHEMI rewards, and $HEMI which is burnt.

Only the owner of a veHEMI NFT position can claim the rewards, and the rewards  
must be claimed per NFT; holders of multiple veHEMI positions will need to perform  
one claim for each position.

UI components will be added to the Hemi Portal to allow users to clai mrewards on  
their veHEMI positions, and a future update will show APY estimations.

## Compatibility
This upgrade only requires smart contract deployments and configuration; it  
is not a change to the Hemi protocol and does not require node operators to  
update their software.

## Changelog

2025-10-24 Initial version.
2025-10-30 Converted to full Hemi Economic Model details.
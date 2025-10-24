
# HIPPO-002

```  
HIPPO: 2  
Title: Initial veHEMI Staking Rewards  
Author: Max Sanchez <max@hemi.xyz>  
Comments-Summary: No comments yet.  
Status: New  
Type: Network  
Created: 2025-10-24  
```  

## Background and Motivation

veHEMI is the native staking system for $HEMI on the Hemi network, with  
staking periods between 12 days and 4 years supported in 6-day epochs.

Depositing $HEMI into veHEMI mints an NFT which represents the staked  
position. Each NFT has a weight based on the total tokens staked and  
the time remaining in the lockup. This weight increases linearly with  the
amount of remaining time, such that a lockup with 1 year remaining  
has twice the weight of a lockup with 6 months remaining.

In the future, veHEMI will serve as the economic security system behind  
many of the protocol's features including governance, decentralized
sequencing,  data publication to Ethereum, hBitVM covenant emulation,
cross-chain  liquidity systems, and more.  In order to properly incentivize
staking in preparatiion for these features, this HIPPO proposes the initial
rewards to be distributed  to veHEMI holders.


## Specification
The initial quantity of $HEMI to be distributed to veHEMI stakers for  
the period of August 30th, 2025 to October 24th, 2025 will be 500,000  
$HEMI.

The tokens will be claimable based on a weighted average of each NFT's  
weight on a daily snapshot.

These snapshots will start at unix epoch 1756512000 (August 30th, 2025  
at 12:00am GMT) and run through 1761264000 (October 24th, 2025 at   
12:00am GMT) inclusive, which is a total of 56 days.

The total 500,000 $HEMI will be split equally across each of the 56  
snapshots; equaling approximately 8928.5714 $HEMI per day.

This will be implemented by a reward contract with a claim function which
calculates the relative weight of a claimant's veHEMI position compared to
the total weight of all positions at each snapshot, and distributes the
proportional amount of rewards to the owner.

Only the owner of a veHEMI position can claim the rewards, and rewards
must be claimed per NFT; holders of multiple veHEMI positions in the same
address will need to perform one claim for each veHEMI position.

All active veHEMI positions are treated equally for this reward distribution.

UI components will be added to the Hemi Portal to allow users to claim rewards
on their veHEMI positions, as well as show estimated APY.


## Compatability
This upgrade only requires smart contract deployments and configuration; it
is not a change to the Hemi protocol and does not require node operators to
update their software.

## Changelog

2025-10-24 Initial version.
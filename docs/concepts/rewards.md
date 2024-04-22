---
sidebar_position: 6
sidebar_label: Reward Program
---

# Reward Program

## TLDR:

- Liquidity Providers are automatically scored and ranked on performance
- Scoring based on: Total Fees accrued over the Epoch duration
- Scoring is conducted over Epochs that last 1 week
- A streak-based incentive bonus for active liquidity provider
- All rewards are distributed following the end of an Epoch 
- Partners can also utilize the program as an efficient way to distribute emissions

## What is the Rewards Program?
The LB Rewards program offers additional token rewards, such as Massa, to incentivize Liquidity Providers to provide liquidity. To qualify for these extra rewards, Liquidity Providers need their liquidity to generate fees. The program is a incentive scheme to encourage efficient liquidity management.
Now, Makers compete to capture the most trading fees, thereby enhancing the efficiency of the rewarded Liquidity Pools.

## Detailed overview of the LB rewards program
### How to Earn Rewards

Liquidity Providers are scored and given a MakerScore. The MakerScore is calculated using the fees collected by the Liquidity Pool over a defined epoch. Therefore, as a Liquidity Provider when participating in this program, the more fees you earn over the duration the higher your MakerScore will be.

### How is the MakerScore calculated?
MakerScores are calculated independently off-chain for each rewarded market over the epoch duration. As an example, if an Epoch lasts for 7 days, the MakerScore will be calculated over that specific period. Rewards are distributed based on each participant’s relative performance against all eligible LPs (for each market).

<p align="center">
  <img src="/img/maker_score.png" alt="Relation between maker score & maker fee" width="500px" />
</p>

## How do you qualify for rewards?
TLDR: You must accrue trading fees during each epoch. The more fees you accrue and the higher your score relative to other Makers, the more rewards you will earn.

### MakerScore Breakdown: MakerFees
TLDR: By accruing fees, you will increase your MakerFee score and thereby if you accrue more Fees versus other Liquidity Providers, you will rank higher and unlock more rewards.


The most important market contribution of an LP is the volume that it supports/generates. LPs are rewarded with fees on swaps against the liquidity that they provide so that fees can be used in place of volume as a participation metric. Further, the dynamic fee mechanics incorporated in LB increase fee rates during volatile conditions (ie for filling large orders). Therefore, LB fees themselves are an excellent measure of the market activity for an LP. Fees represent volatility-weighted volume and serve as the first term in the MakerScore calculation.

<p align="center">
  <img src="/img/maker_fee.png" alt="Maker Fee formula" width="500px" />
</p>

### Epoch Durations and Rewards
Participation is evaluated over Epoch-defined periods, such as 1 week - 4 weeks. Epoch start/end dates will be announced before they begin, along with the reward amounts allocated to each Epoch and participating Liquidity Pool.


### Maker Rewards
LB Rewards are siloed by the market for each epoch. Reward amounts will be announced before the epoch’s start. MakerScores are calculated independently for eligible LPs and rewards are distributed based on their proportional MakerScore in each market.

<p align="center">
  <img src="/img/maker_reward.png" alt="Maker reward formula" width="500px" />
</p>

### Partner Rewards
Partner rewards may also be used to incentivize liquidity in LB markets. The LB Reward program provides a market-maker scoring rubric and generic reward distribution for those incentives. Contact Dusa to explore partnerships.


### Reward Claiming
LP rewards will be calculated off-chain and distributed by a smart contract, users will be able to claim their rewards directly from the UI on the DEX in a similar process to collecting farm rewards. Any rewards distributed will vest over a specified duration, typically this will be the same duration that the epoch ran over. EG If the epoch was 1 week, the rewards will vest over 1 week. Maker scoring and rewards calculations will be completed off-chain but will be published for community review.


### Streak Mechanism:
The following mechanism was developed to encourage users to keep their liquidity active over time: 

A streak-based incentive system to motivate individuals to maintain active liquidity by offering a 5% bonus on their rewards for each consecutive week their liquidity generates fees. This bonus will increase weekly and max out at 30% after a continuous 6-week period. Such a mechanism aims to encourage liquidity providers to manage their liquidity efficiently, leveraging the win aversion tied to keeping the streak of accumulated weeks and the bonus.

They can be seen in the leaderboard/Reward section of the liquidity pool.

<p align="center">
  <img src="/img/streak.png" alt="Streak machanism on Dusa" width="500px" />
</p>

## Eligible Liquidity Pools
All Liquidity Pools that are marked with 'Rewards' are part of the rewards program for the current epoch.


<p align="center">
  <img src="/img/liquidity_pool.png" alt="Eligible liquidity pools" width="500px" />
</p>

## Rewards and the Leaderboard Feature
Epoch rewards can be viewed by clicking on the 'Leaderboard/Rewards' tab located on each Liquidity Pool page. The total rewards allocated per day are highlighted in the UI. For rewards designated for Liquidity Providers, this page also serves as the collection point for vested tokens.


### The Leaderboard
This feature tracks the top Liquidity Providers based on total fees earned. The Leaderboard serves as a performance indicator for each Epoch, helping you monitor the top Liquidity Providers' positions.


<p align="center">
  <img src="/img/leaderboard.png" alt="Incentives leaderboard" width="500px" />
</p>

### Disclaimer
The following citizens/residents are strictly prohibited from interacting with the Dusa Protocol, in this sense, any address that participates in the Dusa Liquidity Incentive program by claiming $Mas Tokens or $Dusa Tokens hereby declares that it is not from and/or does not currently reside in any of the following countries United States of America, Canada, Iran, Cuba, North Korea, Syria, Myanmar (Burma), the Crimea, Donetsk or Luhansk regions, or any other country or region subject to comprehensive country-wide or region-wide economic sanctions by the United States (collectively, the "Restricted Areas");
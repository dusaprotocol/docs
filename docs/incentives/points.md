---
sidebar_position: 7
sidebar_label: Points Program
---

# Point Program

## TLDR:

- All actions on the protocol, if the necessary conditions are met, whether they are direct or indirect, will enable users to earn points on Dusa. The distribution of points is based on three aspects: on-chain activities, off-chain activities, and referee actions.
- The calculation of points is conditionally based on the on-chain points. Coefficients are applied to these points for other actions.
- These points will be utilized for the distribution of future Dusa tokens.

## Rewards vs Points Distribution?

While rewards are designed to incentivize Liquidity Providers to supply liquidity, the points distribution system incentivizes all users, from those who engage with the community to those who interact with the protocol. However, to be eligible for points distribution, users must participate in at least some on-chain actions: from providing liquidity to executing swaps, users must utilize the protocol to accumulate points.

## Direct actions

### On-chain point

This is the foundation upon which the point system is calculated. It's based on:

- Liquidity Providing : fees generated, streak score.
- Trading activities : swap fees, volume.

Farming points by sybils or by doing volume in a bin where you control most of the volume or any other means will result in a ban.

## Indirect actions

Those actions will be a coefficient applied to the based points.

### Community role

Points can be earned based on your completion of Zealy quests, or through your active participation and assistance in Telegram or Discord server. Upon completion of these tasks, you receive a role or an upgrade.

Each role grants a special bonus every week:

- Legendary Dusers: **30 % bonus**
- OG Dusers: **20 % bonus**
- Early Dusers: **15 % bonus**

### Referral

Referring a friend allows a user to boost their points. Every time your referee earns on-chain points, **you receive a 10% bonus** of those points. Similarly, your referee also gets a **10% bonus on their own on-chain points** . Therefore, the more active your referee is, the more points you both earn.

**Disclaimer**: We discourage sharing the referral link indiscriminately. This mechanism is designed to be a win-win situation, so it's better to share the link with people you know to fully enjoy the bonus points.

**Quick Example:**
Let's say Vitalik refers Nakamoto. Now, every time Nakamoto earns on-chain points, Vitalik gets a 10% bonus of those points. For example, if Nakamoto earns 100 on-chain points, Vitalik gets an additional 10 points. Similarly, every time Nakamoto earns on-chain points, Nakamoto gets a 10% bonus on those points. So, if Nakamoto earns 200 on-chain points, Nakamoto gets an additional 20 points.

## Points Distribution Formula

The points are distributed based on the following formula:

$$
Total Points = On Chain Points + (Community Role Bonus * On Chain Points) + (Referral Bonus * On Chain Points)
$$

This formula ensures that all your on-chain activities, and off-chain activities contribute to your total points.
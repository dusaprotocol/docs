---
sidebar_position: 3
sidebar_label: Liquidity Strategies, Basics
---

# Contents
- Overview of Spot Shapes
- Different Spot Strategies
- Using Curve
- Using Bid-Ask
- Your Risks

# Overview of Spot Shapes
Spot is the most popular Liquidity Shape available as it is the easiest to deploy and manage. Using the Spot shape will deploy your liquidity in a uniform distribution ensuring that you have an equal proportion of your liquidity spread over your chosen range. This ensures that your liquidity formation remains versatile and risk-adjusted to suit any type of asset in a liquidity pool and market conditions.
Below are example strategies using Spot, covering popular deployment ranges. Scroll down further as we dive into the details covering advantages, drawbacks, and considerations when deploying these strategies.

<p align="center">
  <img src="/img/spotExemple.png" alt="Exemple of a spot position" width="500px" />
</p>

# Spot: Concentrated
The Concentrated shape is designed for risk-takers who know what they are doing and want to maximize their rewards.
This is the most concentrated shape, which makes it suitable only for stablecoin pairs. It offers the highest capital efficiency, as all liquidity is concentrated within one to three bins.
The Concentrated shape can generate extensive fees in the right conditions but carries the highest risk of IL and requires rebalancing on every price move.

<p align="center">
  <img src="/img/spotConcentrated.png" alt="Concentrated spot position" width="500px" />
</p>

# Spot: Wide
The Wide Shape is perfect for liquidity providers who are new to the Liquidity Book and those who are looking to rebalance not more often than every few days.
Deploy a Wide Shape, which can be defined as a range of approximately 20 to 50 bins, this strategy carries a lower amount of risk as it gives you a wide coverage to capture any volatility in the price of the assets, helping you to earn fees during volatility.
The spot will uniformly distribute liquidity across your chosen range and provide a steady stream of fees for the liquidity provider, even when the price changes significantly (providing it sticks within your deployed range).

<p align="center">
  <img src="/img/spotWide.png" alt="Wide spot position" width="500px" />
</p>

# Spot: Ultra Wide
The Ultra Wide shape is made for those who are looking to absolutely minimize the amount of rebalances they have to perform.
The Wide shape taken to the extreme, Spot - Ultra Wide is the ultimate “set and forget” strategy for the Liquidity Book. It uniformly distributes liquidity across hundreds of bins, ensuring that the price stays within range no matter what.
To accommodate for a wider range, which makes this shape the closest to the “traditional” x*y=k distribution, liquidity for the Ultra Wide is deployed in multiple “batches”, with each batch represented by a separate transaction.

<p align="center">
  <img src="/img/spotUltraWide.png" alt="Ultra wide spot position" width="500px" />
</p>

# Curve
The Curve is a great shape for those who aren’t afraid of frequent rebalances but still want to manage their exposure and aren’t prepared to bet everything on one bin.
The Curve shape offers a middle ground between Concentrated and Spread shapes. It still concentrates the bulk of liquidity around the single price point but distributes a portion of it in the surrounding bins.
This shape allows users to continue to earn fees from short-term price volatility while taking maximum advantage of the LB’s capital efficiency. It is the most suitable for stable pairs with soft pegs but can also be used at key price levels of volatile pairs.

<p align="center">
  <img src="/img/curve.png" alt="Curve position" width="500px" />
</p>

# Bid-Ask
Liquidity Providers who are prepared to take their experience to the next step and are ready to take some risks will find Bid-Ask shape to be a powerful tool.
The Bid-Ask shape is the most complex out of all the Basic ones. It is designed to capture volatility around the defined price, maximizing the fees as long as the market fluctuates within your deployed range.
Similar to the Curve strategy, this shape requires continuous rebalances to remain effective – if there is no volatility or the price leaves the range, the shape needs to be adjusted.

<p align="center">
  <img src="/img/bidAsk.png" alt="Bid-Ask position" width="500px" />
</p>

## Risks when managing liquidity
Engaging in providing Liquidity using the Liquidity Book protocol involves risks, including but not limited to impermanent loss, smart contract vulnerabilities, systemic failures, liquidity crunches, regulatory changes, market volatility, and operational errors. Your capital is at risk; only invest funds you can afford to lose. No assurance or guarantee is provided, and LPs assume all responsibility for their investments. Seek independent financial advice as needed.

---
sidebar_position: 5
sidebar_label: Rebalancing your position
---

# Contents
- The Active Bin and how to earn fees
- Your liquidity is Out of Position
- Your choices to rebalance
- Your risks

## The Active Bin and how to earn fees
The main aim for any Liquidity Provider is to earn fees captured by the trading activity that occurs in a Liquidity Pool. To earn fees using the Liquidity Book, your liquidity must be within range. If your liquidity is in range, you will see the active bin which is visualized on the UI as being split by two colors, see the image below for further clarity on how the active bin will appear on the UI.

<p align="center">
  <img src="/img/earnFee.png" alt="How to earn fees" width="500px" />
</p>

To enhance your earning potential, you are expected to manage your liquidity keeping it balanced and within range. Liquidity Shapes and the strategies you deploy and how you go about managing your liquidity, are all key to how you earn fees. In this article, we'll explore what to do if your liquidity is Out of position

## Your Liquidity is Out of position
When the price of the assets in the liquidity pool moves, this may cause your liquidity position to become out of position. Your liquidity is always fixed when you deposit it into a Liquidity Book Pool. When your Liquidity is out of position this means that the price of the underlying assets in the Liquidity Pool has moved outside of your chosen range.
In the example below, you can see that the position is all green, indicating that the price of MAS has moved outside of the range. The UI will indicate when this happens to your own position. You will either see your Liquidity all green or purple, depending on the price change.
This means you are no longer earning fees and you now have some decisions to make for your next steps which are discussed further below.

<p align="center">
  <img src="/img/rebalancing.png" alt="Position out of range" width="500px" />
</p>

### What should I do when my Liquidity is out of position?
Here are scenarios that explore the possible actions an LP might consider when remedying an out-of-position range:
Scenario:
Assume you, as an LP, have provided liquidity to a pool for the MAS/USDC pair, placing your liquidity in the price range of $0.10 to $0.12.
The current price of MAS is $0.11, so your liquidity is active, and you're earning fees from trades occurring within your range.
The market shifts and the price of MAS rises to $0.15 due to a bullish trend, moving your liquidity out of range.

### Decisions to consider:

1. Do Nothing (Passive Management):
You could choose to do nothing, leaving your liquidity out of range.

Pros:
- Avoid transaction fees (gas costs) associated with rebalancing or repositioning.
- If the price comes back into your range, you'll automatically begin to earn fees again without any action required.

Cons:
- You won't earn fees when the price is out of your selected range.
- If the price continues to rise, your position will increasingly consist of more USDC and less MAS, which may not be optimal if you believe MAS’s price will keep rising.

2. Reposition Liquidity (Active Management):
You might decide to move your liquidity to a higher range, say $0.14 to $0.2. To do this must withdraw your liquidity and re-deposit it. When doing that you may need to swap into the other token to deploy with both tokens, or you can redeposit at a new range, with a single side of the market, and wait for a retracement.

Pros:
- Begin earning fees again if the price remains within the new range.
- Maintain exposure to MAS if you believe the uptrend will continue.

Cons:
- Incurs transaction costs
- If the price quickly reverts back to the original range, you might miss out on fees and incur additional costs to move back.

3. Withdraw and Hold (Exiting the Pool):
Another option is to withdraw your liquidity entirely and either hold the assets or reallocate them elsewhere.

Pros:
- No longer subject to potential impermanent loss if you believe MAS will continue to rise.
- Flexibility to invest your assets in a different opportunity.

Cons:
- No longer earning trading fees from this liquidity pool.
- May incur transaction fees and a taxable event upon withdrawal.

4. Add More Liquidity (Doubling Down):
If you have additional capital, you could choose to add more liquidity at higher price ranges without touching your original position.

Pros:
- Potentially earn fees across a broader price range if you expect volatility.
- Diversify your positions within the pool.

Cons:
- Increases your exposure to the pool, which might not be optimal if the price falls.
- Additional capital is tied up in the liquidity pool.

Each of these decisions carries trade-offs and risks, and the best course of action will depend on your own assessment of the market, your risk tolerance, and your goals as a liquidity provider. You must consider factors like market trends, the cost of gas fees, the potential for impermanent loss, and their desire for passive vs. active management when deciding how to manage your liquidity position.

## Your Risks
Managing concentrated liquidity involves significant risk and is not suitable for all DeFi participants. The nature of concentrated liquidity positions can lead to increased exposure to market volatility, impermanent loss, and other financial risks. This activity should only be undertaken by those who have a comprehensive understanding of decentralized finance (DeFi) protocols and are prepared to accept the possibility of substantial losses, including the potential loss of all invested capital. The information provided here does not constitute investment advice, financial advice, trading advice, or any other sort of advice and should not be treated as such.

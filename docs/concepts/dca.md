---
sidebar_position: 7
sidebar_label: Dollar Cost Averaging (DCA)
---

# Dollar Cost Averaging (DCA)

## Introduction

Dollar Cost Averaging (DCA) is a strategy where a fixed investment is made at regular intervals regardless of the asset's price at each purchase. On-chain, this approach is automated via a smart contract, allowing users to set up recurring trades that convert one token into another based on a pre-defined swap path. This system minimizes the impact of market volatility by averaging the entry price over time. Automation is achieved through smart-contract deferred calls, scheduling trades automatically.

## DCA Strategy Overview

The DCA feature enables automated execution & automated rescheduling.

Users can start, update, or stop a DCA order. Once initiated, the system uses deferred calls to schedule future executions at defined intervals. If a DCA order is due immediately or in the future, the contract automatically schedules the corresponding call.

Since the system is entirely on-chain, all trades and operations are publicly verifiable, ensuring transparency and reducing counterparty risk. It also requires minimal manual intervention once the order is set up.


**Trade Execution with Risk Management:**  

  For each scheduled trade, the contract checks that the user has sufficient token balance and allowance. It then consults an on-chain quoter and oracle to determine the best swap path and verifies that price volatility is within a set threshold before executing the trade. If market conditions aren’t favorable, the execution is rescheduled.

  The DCA order uses a defined token swap path that may involve multiple liquidity pairs. The system finds the best available swap route and performs necessary intermediate swaps.

  A fixed amount is invested at set intervals, smoothing out the purchase price over multiple trades. By averaging out the purchase price over time, DCA helps reduce the impact of short-term market volatility, making it an attractive strategy for long-term investors.

  The system handles multi-hop token swaps (if the swap path has more than two tokens) and ensures that enough funds are reserved for autonomous gas fees. A fee of 0.7% is deducted during the swap, plus around 0.6 MAS for gas fees (depending on swap complexity).

  Users can update or cancel their DCA orders at any time. This flexibility allows investors to adjust their strategies based on changing market conditions or personal preferences, while still benefiting from the automation and regularity that DCA offers.

## How to Use the On-Chain DCA

Using the DCA system is designed to be straightforward. Follow these steps to set up and manage your automated trading strategy:

<p align="center">
  <img src="/img/dca_front.png" alt="DCA frontend" width="900px" />
</p>

1. **Set Up Your DCA Order:**  
   Determine the following parameters for your DCA order:
   - **Token In and Out:** The token used to pay for the DCA and the token that will be bought. If the DCA is starting from MAS tokens, they need to be wrapped beforehand.
   - **Amount Per Trade:** The fixed token amount to be swapped at each interval.
   - **Interval:** How often the trade should occur (must be between 1 minute and 2 months).
   - **End Time:** Specify the end of the DCA. It can be infinite.

<p align="center">
  <img src="/img/dca_endTime.png" alt="DCA setting endtime" width="500px" />
</p>

   - **Slippage:** Set a slippage percentage (greater than 1%) to control acceptable price volatility during swaps. Slippage checks are performed against the price oracle.

<p align="center">
  <img src="/img/dca_slippage.png" alt="DCA setting slippage" width="500px" />
</p>

2. **Monitoring and Adjustments:**  
  By clicking on the DCA, a performance graph and history of previous swaps is shown.
   - **Update:** If market conditions change or you wish to adjust the parameters of your strategy, use the `updateDCA` function to modify your DCA order.
   - **Stop:** To cancel the DCA order, call the `stopDCA` function. This stops further scheduled trades and cancels any pending deferred calls.

<p align="center">
  <img src="/img/dca_monitoring.png" alt="DCA graph" width="800px" />
</p>

   The contract automatically manages fees and ensures that a portion of funds is reserved for gas fees. 
  
   Make sure your account maintains enough token balance for the next DCA swap.

## Limitations

When using the on-chain DCA system, there are several key limitations to be aware of:

- The interval between trades must be **at least 1 minute** and **no more than 2 months**.  
- The swap path must not include **more than 4 tokens**.  
- The token path **must include either WMAS or USDC** to ensure proper pairing and liquidity during swaps.
- Each execution of a DCA order verifies that the user has sufficient token balance and has approved the contract to spend the required amount. If these conditions are not met, the DCA order is canceled.
- If the DCA is starting from MAS tokens, they need to be wrapped beforehand.
- The contract relies on deferred calls for automation. In volatile markets or under high network load, the scheduling or execution might experience delays.
- If market conditions do not meet the oracle checks (for instance, if the price deviates beyond the allowed threshold), the trade is deferred and rescheduled.

---
description: Frequently Asked Questions - Borrow
---

# Borrow FAQ

## How Much Can I Borrow?

The amount you can borrow is determined by several factors, including the value of your supplied assets, your available credit, and the level of market liquidity. Borrowing may not be possible if there is insufficient liquidity or if your credit limit drops below the required threshold.

## Are Interest Rates Stable?

Unlike fixed-rate loans, interest rates in the Moonwell protocol are dynamic, adjusting in real time based on market demand. Interest rate curves define the relationship between supply, demand, and the resulting rates. These curves can be modified through governance proposals, enabling the community to refine them and adapt to changing market conditions.

Given the dynamic nature of these rates, borrowers must closely monitor their available credit. Neglecting to account for accumulating fees or fluctuating rates could put your loan at risk and potentially lead to liquidation.

## Why Can't I Borrow an Asset?

There are several reasons you may be unable to borrow a specific asset:

* **0% Collateral Factor**: Each asset has a collateral factor, which determines the percentage of its value that can be borrowed against. If an asset’s collateral factor is set to 0%, borrowing is disabled to mitigate risk.
* **Insufficient Liquidity**: If there isn’t enough liquidity (supplied assets) available in the market, borrowing may not be possible. This happens when demand for an asset exceeds the total amount supplied. You can either wait for more liquidity to enter the market or for existing borrowers to repay their loans.
* **Borrow Cap Reached**: Each market has a borrow cap, limiting the total amount that can be borrowed at any given time. If the borrow cap is reached, no further borrowing is allowed. Borrow caps are designed to maintain protocol solvency and are adjusted based on factors like liquidity and utilization rates. You’ll need to wait for repayments or for the borrow cap to be increased before borrowing from that market.

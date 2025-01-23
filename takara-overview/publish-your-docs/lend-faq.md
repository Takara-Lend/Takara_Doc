---
description: Frequently Asked Questions - Lending
---

# Lend FAQ

## How is the Supply APY Calculated?

The Supply APY (Annual Percentage Yield) of an asset on Takara consists of two components: [Base APY](lend-faq.md#base-apy) and [Rewards](lend-faq.md#rewards).

### Base APY

The Base APY is the interest rate that lenders earn through automatic compounding when supplying assets on Takaraa. It is determined by the fees collected from borrowers.

Here are the key points to understand about Base APY:

1. **Auto-Compounding**
   * The Base APY is automatically compounded back into the smart contract of the supplied asset.
   * No manual claiming is required, making the process seamless for users.
2. **Asset-Specific Rewards**
   * Earnings are distributed in the specific token that protocol is distributing.
   * For example, if the rewarding asset is SEI, you will get additional SEI rewards for supplyig assets.
3. **How Base APY Is Determined**
   * **Algorithmic Calculation:** Base APY is calculated based on the market's utilization rate.
   * **Interest Rate Curves:** Defined through Takara Governance, these curves establish the relationship between market utilization and Base APY.
   * **Utilization Impact:**
     * Higher market utilization (more borrowing) results in a higher Base APY.
     * Lower market utilization leads to a lower Base APY.
   * **Monitoring Base APY**
     * Users can track their Base APY earnings over time by reviewing the supplied value of their chosen asset.

### Rewards

Rewards are additional incentives that need to be manually claimed by the user.

**Key Aspects of Rewards:**

* **Manual Claiming**
  * Rewards need to be manually claimed through the "Rewards" page.
* **APR (Annual Percentage Rate)**
  * Rewards are calculated in APR and do not compound automatically.
* **Sources**
  * Rewards may come from various providers or grants.
  * For instance, supplying USDC may allows users to earn rewards in both SEI and USDC tokens.

## Market Utilization and Liquidity

Market utilization measures the proportion of borrowed funds compared to the total supply of assets within a given market.

* Utilization exceeding 100% means the total borrowed amount, including accrued interest, has surpassed the total supply.
* As utilization nears 100%, liquidity shortages may make it challenging to withdraw assets.


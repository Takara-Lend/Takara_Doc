# ‼️ Protocol Information

<figure><img src="../.gitbook/assets/prootocol infomation.png" alt=""><figcaption></figcaption></figure>

## Collateral Factor

The Collateral Factor represents the maximum percentage of an asset’s value that can be used as collateral for borrowing in the Takara protocol. This percentage determines how much can be borrowed against a specific asset.

For instance, if an asset’s Collateral Factor is 70%, up to 70% of its value can be utilized as collateral for borrowing other assets.

Here’s an example to illustrate:

• Suppose the Collateral Factor for ETH is set at 70%.

• If you supply $1,000 worth of ETH as collateral, you can borrow up to $700 in other assets based on the Collateral Factor.

{% hint style="info" %}
Important: It is strongly recommended to keep your borrowing below 80% of your limit. In the example above, with a borrowing limit of $600, it’s advisable to borrow no more than $480 ($600 × 80%). Exceeding 80% of your borrowing limit increases the risk of liquidation.

Liquidation occurs when the value of your collateral falls below a certain threshold, allowing a liquidator to seize the collateral to repay the borrowed amount. By maintaining your borrowing under 80% of the limit, you reduce the risk of liquidation and the associated consequences.
{% endhint %}

## Reserve Factor

The Reserve Factor refers to the percentage of interest paid by borrowers that is allocated to the protocol’s reserves. Each market has its own reserve, which helps maintain the protocol’s stability and long-term sustainability.

Here’s an example to illustrate:

• Suppose you borrow $1,000 USDC from the protocol.

• The USDC Borrow APY (Annual Percentage Yield) is 10%.

• Over one year, you would pay approximately $100 in interest.

• If the Reserve Factor is set at 20%, $20 of the $100 interest payment would go to the Takara USDC protocol reserve.

## Close Factor

The Close Factor specifies the maximum percentage of a borrower’s outstanding debt that can be repaid during a single liquidation event. This percentage also determines the portion of the collateral that can be seized by the liquidator.

Here’s an example to illustrate:

• Suppose your account’s credit limit is fully utilized (0%), making it eligible for liquidation.

• You have an outstanding borrow of 100 USDC.

• If the Close Factor for USDC.wh is set at 50%, the liquidator can:

• Repay 50% of your outstanding borrow (50 USDC).

• Seize an equivalent value from your collateral.

• Receive a reward in the form of a [Liquidation Incentive](protocol-information.md#liquidation-incentive).

## Liquidation Incentive

The Liquidation Incentive in the Moonwell protocol is designed to reward liquidators for executing liquidations, ensuring the protocol’s solvency and promoting efficient liquidation processes. This incentive is equal to 10% of the outstanding borrow amount of an account subject to liquidation and is split into two components:

1\. **7% Liquidator Bonus**: This portion is awarded to the liquidator as a reward for promptly and effectively carrying out the liquidation. By offering this bonus, the protocol encourages active participation and ensures the timely resolution of at-risk accounts.

2\. **3% Reserve Allocation**: This portion is directed to the protocol reserves of the liquidated collateral. By contributing to the reserves, the protocol mitigates the risk of insolvency caused by cascading liquidations, supports short-term liquidity needs, and maintains overall market stability.

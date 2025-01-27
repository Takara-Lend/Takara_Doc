---
description: Learn about credit limits and how to avoid liquidation
---

# Credit and Liquidations

## Understanding Credit Limit

The term "Credit Limit" in the context of Takara Lend refers to the maximum amount of funds that users can borrow based on the collateral they provide.&#x20;

When users activate the 'collateral switch' feature and provide assets as collateral, the value of these assets determines the credit limit that they can access. The higher the value of the collateral, the larger the credit limit will be.

The credit limit serves as a safeguard to ensure that borrowers have adequate collateral to secure their loans. It helps maintain the stability of the lending process and reduces the risk of default. By setting a credit limit, Takara can ensure a responsible borrowing and lending environment for all participants.

"Credit Limit" is calculated using the formula:

```
∑User Market Total Supplied in USD * Collateral Factor
```

{% hint style="info" %}
The [Collateral Factor](../../protocol-information/protocol-information.md#collateral-factor) represents the maximum percentage of collateral value that can be borrowed.
{% endhint %}

{% hint style="info" %}
Example:

* User deposits $1000 of USDC to the protocol as collateral.
* The collateral factor of USDC is 60%.
* Calculate the "Credit Limit"

Credit Limit = `∑User Market Total Supplied in USD * Collateral Factor`

Credit Limit = $1000 \* 0.6 = $600

* Therefore, in this example, the credit limit of $600. This means you can borrow up to $600.
{% endhint %}

### Understanding Credit Remaining

"Credit Remaining" refers to the amount of credit or funds that are available for a user to borrow.

A higher "Credit Remaining" indicates a healthier collateral ratio and provides a safer margin against potential liquidation. On the other hand, a lower "Credit Remaining" suggests a higher risk of liquidation. **When the "Credit Remaining" drops to $0 or 0%, the risk of liquidation becomes significant.**

Monitoring the "Credit Remaining" closely is crucial to avoid reaching a point where there is no remaining credit available. Maintaining a sufficient "Credit Remaining" is essential for managing loans effectively and mitigating the risk of liquidation. By ensuring a healthy margin between the borrowed funds and the collateral value, users can maintain a more stable and secure position.

The value of "Credit Remaining" is calculated using the formula:

`(∑User Market Total Supplied in USD * Collateral Factor) - User Total Borrowed in USD`



{% hint style="info" %}
**Example:**

* User deposits $1000 of USDC to the protocol as collateral.
* The user borrows $100 of USDC
* The collateral factor of USDC is 60%.
* Step 1: Calculate the "Credit Limit"

Credit Limit = `∑User Market Total Supplied in USD * Collateral Factor`

Credit Limit = $1000 \* 0.6 = $600

* Step 2: Calculate the value of "Credit Remaining"

Credit Remaining = `Credit Limit - User Total Borrowed in USD`

Credit Remaining = $600 - $100 = $500

* In this example, when the user borrowed $100 of USDC, their "Credit Remaining" decreased to $500. If the remaining credit drops to a value of $0, the user's position becomes vulnerable to liquidation.
{% endhint %}

The percentage of "Credit Remaining" is calculated using the formula:

`[(∑User Market Total Supplied in USD * Collateral Factor) - User Total Borrowed in USD] / (∑User Market Total Supplied in USD * Collateral Factor)`

{% hint style="info" %}
**Example:**

* User deposits $1000 of USDC to the protocol as collateral.
* The user borrows $100 of USDC
* The collateral factor of USDC is 60%.
* Step 1: Calculate the "Credit Limit"

Credit Limit = `∑User Market Total Supplied in USD * Collateral Factor`

Credit Limit = $1000 \* 0.6 = $600

* Step 2: Calculate the percentage of "Credit Remaining"

Credit Remaining = `[Credit Limit - User Total Borrowed in USD] / (Credit Limit)`

Credit Remaining = \[$600 - $100] / ($600) = 83.3%

* In this example, when the user borrowed $100 of USDC, their "Credit Remaining" decreased to a percentage of 83.3%. If the "Credit Remaining" drops to 0%, the user's position becomes vulnerable to liquidation.
{% endhint %}

### Avoiding Liquidation

Liquidation occurs when collateral assets are sold to repay a borrower’s debt after failing to meet loan obligations.

To avoid liquidation, borrowers should regularly check their “Credit Remaining” and ensure it stays above $0 and above 0%.

This can be accomplished by:

1. **Repaying Loans**: Making loan repayments helps maintain a positive “Credit Remaining,” reducing the risk of liquidation.
2. **Adding More Collateral**: Supplying additional collateral increases the credit limit and available “Credit Remaining,” further decreasing the risk of liquidation.

{% hint style="info" %}
Liquidators are essential to the lending and borrowing ecosystem, ensuring the stability and efficiency of the system by managing the liquidation process. They continuously monitor and identify undercollateralized loan positions. When a loan becomes undercollateralized—either due to a decline in collateral value or an increase in the borrowed amount—liquidators intervene to safeguard depositors and, in many cases, earn a profit.

To encourage liquidations and maintain the protocol’s solvency, liquidators are rewarded through a Liquidation Incentive, which includes two components:

* **7% Liquidator Bonus**: Rewarded to liquidators for successfully completing liquidations, promoting the protocol’s operational efficiency.
* **3% Reserve Allocation**: Dedicated to bolstering the protocol’s reserves, ensuring long-term sustainability.
{% endhint %}

### Factors Affecting Credit

Several factors influence a borrower’s remaining credit, including:

* **Borrowed Amount**: The amount already borrowed directly affects the remaining credit. As the borrowed amount increases, the available credit decreases. Borrowers should carefully evaluate their borrowing needs and risk tolerance to determine an appropriate loan amount.
* **Market Volatility**: Fluctuations in market conditions can impact the value of collateral assets, thereby affecting the available credit. Borrowers should consider market volatility and its potential impact on their collateral when determining how much to borrow.
* **Changes in Collateral Value**: The value of the collateral provided plays a key role in determining credit availability. Increases or decreases in collateral value can either expand or reduce the borrower’s remaining credit. Staying mindful of these changes is essential for borrowers to manage their borrowing effectively.

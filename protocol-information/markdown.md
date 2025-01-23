---
hidden: true
---

# Credit Limit & Liquidation

The term "Credit Limit" in the context of Takara Lend refers to the maximum amount of funds that users can borrow based on the collateral they provide.&#x20;

When users activate the 'collateral switch' feature and provide assets as collateral, the value of these assets determines the credit limit that they can access. The higher the value of the collateral, the larger the credit limit will be.

The credit limit serves as a safeguard to ensure that borrowers have adequate collateral to secure their loans. It helps maintain the stability of the lending process and reduces the risk of default. By setting a credit limit, Takara can ensure a responsible borrowing and lending environment for all participants.

"Credit Limit" is calculated using the formula:

∑_UserMarketTotalSuppliedi&#x6E;_&#x55;SD∗_CollateralFactor_

Let's consider an example where a user deposits $1000 worth of USDC as collateral in the Takara Lend protocol. The collateral factor assigned to USDC is 60%.

* To calculate the "Credit Limit", we use the following formula:

_CreditLimit_=(_UserMarketTotalSuppliedi&#x6E;_&#x55;SD)(_CollateralFactor_)

* In this case, the credit limit would be: Credit Limit = $1000 \* 0.6 = $600
* Therefore, based on this example, the credit limit for the user would be $600. This means that the user can borrow funds up to a maximum of $600, depending on their borrowing needs and the available collateral.
* It's important to note that the credit limit helps maintain a responsible borrowing environment and ensures that borrowers have sufficient collateral to secure their loans.



## Understanding Remaining Credit

"Credit Remaining" refers to the amount of credit or funds that are available for a user to borrow.

A higher "Credit Remaining" indicates a healthier collateral ratio and provides a safer margin against potential liquidation. On the other hand, a lower "Credit Remaining" suggests a higher risk of liquidation. When the "Credit Remaining" drops to $0 or 0%, the risk of liquidation becomes significant.

Monitoring the "Credit Remaining" closely is crucial to avoid reaching a point where there is no remaining credit available. Maintaining a sufficient "Credit Remaining" is essential for managing loans effectively and mitigating the risk of liquidation. By ensuring a healthy margin between the borrowed funds and the collateral value, users can maintain a more stable and secure position.

The value of "Credit Remaining" is calculated using the formula:

(∑UserMarketTotalSuppliedinUSD∗CollateralFactor)−UserTotalBorrowedinUSD

Let's consider an example where a user deposits $1000 worth of USDC as collateral in Takara. The collateral factor assigned to USDC is 60%. The user decides to borrow $100 of USDC.

*   Step 1: Calculating the "Credit Limit"

    The credit limit is determined by multiplying the total amount of collateral supplied by the user in USD with the collateral factor.&#x20;

Credit Limit = (User Market Total Supplied in USD) (Collateral Factor) Credit Limit = $1000 0.6 = $600

*   Step 2: Calculating the "Credit Remaining"

    The credit remaining is obtained by subtracting the total amount borrowed by the user in USD from the credit limit.&#x20;

Credit Remaining = Credit Limit - User Total Borrowed in USD Credit Remaining = $600 - $100 = $500

In this example, after borrowing $100 of USDC, the user's "Credit Remaining" decreases to $500. It's important to note that if the remaining credit drops to a value of $0, it puts the user's position at risk of liquidation. Therefore, monitoring the "Credit Remaining" is crucial to ensure a safe margin against potential liquidation and to maintain a stable borrowing position.

The percentage of "Credit Remaining" is calculated using the formula:

`[(∑User Market Total Supplied in USD * Collateral Factor) - User Total Borrowed in USD]`

Let's consider an example where a user deposits $1000 worth of USDC as collateral. The collateral factor assigned to USDC is 60%. The user decides to borrow $100 of USDC.

*   Step 1: Calculate the "Credit Limit"

    The credit limit is determined by multiplying the total amount of collateral supplied by the user in USD with the collateral factor.&#x20;

Credit Limit = (User Market Total Supplied in USD) (Collateral Factor) Credit Limit = $1000 0.6 = $600

*   Step 2: Calculate the percentage of "Credit Remaining"

    The percentage of credit remaining is obtained by dividing the difference between the credit limit and the total amount borrowed by the user in USD by the credit limit, and then multiplying by 100. Credit Remaining = Credit Limit - User Total Borrowed in USD / (Credit Limit) 100 Credit Remaining = \[$600 - $100] / ($600) 100 = 83.3%

In this example, after borrowing $100 of USDC, the user's "Credit Remaining" decreases to 83.3%. It's important to note that if the "Credit Remaining" drops to 0%, it puts the user's position at risk of liquidation. Therefore, monitoring the percentage of "Credit Remaining" is crucial to ensure a safe margin against potential liquidation and to maintain a stable borrowing position within the Rho Markets protocol.

To minimize the risk of liquidation, borrowers must prioritize certain measures and regularly monitor their "Credit Remaining." Liquidation occurs when a borrower fails to meet their loan obligations, leading to the sale of their collateral assets to repay the debt.

To avoid liquidation, borrowers should ensure that their "Credit Remaining" remains above a value of $0 and stays above 0% by implementing the following strategies:

1. Loan Repayments: Making timely and regular loan repayments is crucial as it helps maintain a positive "Credit Remaining." By repaying the borrowed funds, borrowers reduce their debt and increase their credit margin, lowering the risk of liquidation.
2. Supplying Additional Collateral: Borrowers can mitigate the risk of liquidation by providing additional collateral. Adding more collateral to the lending pool increases the credit limit and expands the available "Credit Remaining." This additional collateral acts as a buffer, providing a safer margin against potential liquidation.

By implementing these strategies, borrowers can actively manage their borrowing positions within the Rho Markets protocol, reducing the risk of liquidation and ensuring a more secure and stable borrowing experience. Regular monitoring of the "Credit Remaining" is essential to take proactive steps and maintain a healthy collateral position.

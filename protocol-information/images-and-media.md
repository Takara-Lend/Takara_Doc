# Interest Rate Model

Borrow APR

The interest rate model for borrowed assets can be calculated using the following formula:

```
= Base + Multiplier * min(UtilizationRate, Kink) + max(JumpMultiplier * UtilizationRate - Kink, 
```



Supply APR

The interest rate model for supplying assets can be calculated using the following formula:

```
= Distribute (Interest Paid by Borrowers Per Block - Reserve) to all suppliers, and convert it into APY

= Distribute [(1 + Borrow APY) ^ (1 / BlocksPerYear) - 1] * Total Borrow * (1 - Reserve Factor) to all suppliers, and convert it into APY

= {[(1 + Borrow APY) ^ (1 / BlocksPerYear) - 1] * Total Borrow * (1 - Reserve Factor) / Total Supply}, and convert it into APY

= {1 + [(1 + Borrow APY) ^ (1/BlocksPerYear) - 1] * Total Borrow * (1 - Reserve Factor) / To
```

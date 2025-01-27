---
hidden: true
---

# Takara Lend Contract Overview

### Introduction

Takara is a decentralized lending protocol that allows users to borrow and supply crypto assets. The core mechanisms include supply, borrowing, liquidation, and governance. Users earn interest by supplying assets or pay interest when borrowing assets.

## Core Contracts

### Comptroller

* The Comptroller is the main management contract in Takara Lend, responsible for:
* Managing the addition and removal of markets
* Setting borrowing and liquidation parameters
* Calculating user liquidity and health factor
* Distributing TKL token rewards
  * \[WIP]

### Global Factors

Global factors are common parameters that apply to the entire Takara Lend protocol. These are usually set at the governance level and affect all assets. The main global factors include:

### Reserve Factor:

* Determines the portion of each interest payment that is reserved into the protocol’s reserves.
* For example, if the reserve factor is 10%, then 10% of each interest payment is reserved, and the remaining 90% is distributed to suppliers.

### Close Factor:

* Determines the maximum portion of a borrower’s debt that can be repaid during liquidation.
* For example, if the close factor is 50%, then liquidators can repay up to 50% of the borrower’s debt.

### Collateral Factor

* Determines the proportion of an asset’s value that can be borrowed.
* For example, if the collateral factor is 75%, an asset worth $100 can be used to borrow up to $75 of other assets.

### Liquidation Incentive

* Determines the reward given to liquidators during liquidation.
* For example, if a token has a liquidation incentive of 110%, liquidators can buy collateral at a 10% discount during liquidation.

**Precision of Factors:** In smart contract programming, using fixed precision is a common practice to ensure the accuracy of numerical operations. All factor values are specified with a precision of **1e18**. This means that the factor values are multiplied by 1e18 to avoid precision issues that arise from floating-point arithmetic in smart contracts. For example, if the reserve factor is 10%, the value set in the contract would be **0.1 \* 1e18 = 1e17**



## tToken

**tToken** contracts represent the lending markets for each asset, such as rETH, rUSDC, etc. Key functions include:

1. **mint**: Supply underlying assets to the protocol and receive rTokens
2. **redeem**: Redeem underlying assets
3. **borrow**: Borrow underlying assets
4. **repayBorrow**: Repay borrowed assets



### Asset

**Per-Token Factors**

Each token has its own unique `factor` settings, which determine the behavior and risk parameters of that specific token within the protocol.

**Reserve Factor**

Each token can have its own reserve factor, determining the portion of its interest payments that go into the reserves.

**Collateral Factor**

* Determines the proportion of that specific token's value that can be borrowed.
* High-risk assets typically have lower collateral factors, while low-risk assets have higher collateral factors.

**Seize Share:**

* Determines the portion of seized collateral that is distributed to liquidators during the liquidation process.
* For example, if the seize share is 2.8%, it means that liquidators receive 2.8% of the seized collateral as a reward.

**Borrow And Supply Caps**

Borrow and supply caps are limits set on the amount of a specific asset that can be borrowed or supplied within the protocol. These caps help manage risk by preventing excessive borrowing or supplying of a particular asset, which can lead to liquidity or volatility issues.



## InterestRateModel

The InterestRateModel contract defines the interest rate model for each market. Rates adjust dynamically based on the utilization rate of the market to balance supply and demand.

**JumpRateModel**

The **JumpRateModel** is a specific type of interest rate model used in some of Takara Lend. It features a "jump" in the interest rate at a certain utilization point, which helps maintain liquidity. This model has three key parameters:

* **Base Rate:** The interest rate when the utilization is 0%.
* **Multiplier:** Determines the increase in the interest rate as utilization increases.
* **Jump Multiplier:** A higher rate that applies once utilization surpasses a certain threshold, incentivizing more liquidity supply.
* **Kink**: The utilization point at which the jump multiplier is applied

## Price Oracle

The PriceOracle contract provides price information for market assets, used to calculate borrowing and liquidation eligibility.

* **getGracePeriodTime:** Returns the grace period time set for price feeds.
* **getFreshCheck:** Returns the threshold time for considering a price feed as “fresh”.
* **getSequencerUptimeFeed:** Returns the address of the sequencer uptime feed used to check if the sequencer is up
* **getChainlinkPriceFeed:** Returns the Chainlink price feed address for a given tToken
* **getChainlinkPrice:** Fetches the latest Chainlink price for a given tToken
* **getPrice(RToken rToken):** Returns the current price for the specified tToken using the highest priority oracle
* **getUnderlyingPrice:** Returns the underlying asset’s price for the specified tToken


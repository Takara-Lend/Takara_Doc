---
description: Takara Smart Contract Addresses
---

# 📜 Contracts

<figure><img src="../.gitbook/assets/1224 1h.png" alt=""><figcaption></figcaption></figure>

### **Core Protocol Contracts**

| Name                   | Address                                      | Description                                       |
| ---------------------- | -------------------------------------------- | ------------------------------------------------- |
| **Comptroller**        | `0x56A171Acb1bBa46D4fdF21AfBE89377574B8D9BD` | Risk management and governance for Takara Lend.   |
| **Unitroller**         | `0x71034bf5eC0FAd7aEE81a213403c8892F3d8CAeE` | Proxy for the Comptroller contract.               |
| **MarketState**        | `0x323917A279B209754B32Ab57a817c64ECfE2AF40` | Tracks the current status of lending markets.     |
| **MRD Proxy**          | `0x68A92Be349d48766128C0Ae893Fc391859F9BC11` | Main proxy contract handling market interactions. |
| **MRD Implementation** | `0x059798f39461e17047B6D2AD6AAE4d3a0dd9Dc82` | Logic implementation for MRD Proxy.               |
| **MRD Proxy Admin**    | `0x8DF1265bFb778fFD08341c63e7C67367c0a60288` | Admin contract managing protocol upgrades.        |

***

### **Oracles**

| Name                  | Address                                      | Description                                          |
| --------------------- | -------------------------------------------- | ---------------------------------------------------- |
| **Price Feed Oracle** | `0xD6a275072dceC8a319c0C7178951A0CF9DCC0447` | Provides asset pricing for protocol risk management. |

***

### **Interest Rate Models**

| Name                          | Address                                      | Description                              |
| ----------------------------- | -------------------------------------------- | ---------------------------------------- |
| **Jump Rate Model (USDC)**    | `0xED908ab644212969249bc7B167e3A2DF30709E1e` | Interest rate model for USDC lending.    |
| **Jump Rate Model (USDT)**    | `0x692D0bF5112B221AB14C5DC8C2159DDD87FF196B` | Interest rate model for USDT lending.    |
| **Jump Rate Model (WSEI)**    | `0x52196Ff255aA200552B5d24d56A725B0e206a26b` | Interest rate model for WSEI lending.    |
| **Jump Rate Model (fastUSD)** | `0xc6c06859d6caEF79a6E750EBc43Dd2dF63291aA2` | Interest rate model for fastUSD lending. |
| **Jump Rate Model (iSEI)**    | `0xa282a20B9baB553D434faEC7D473C08B2e8D88FE` | Interest rate model for iSEI lending.    |

***

### **Lending Market Contracts (tTokens)**

| Name         | Address                                      | Description                                  |
| ------------ | -------------------------------------------- | -------------------------------------------- |
| **tSEI**     | `0xA26b9BFe606d29F16B5Aecf30F9233934452c4E2` | Interest-bearing token for SEI deposits.     |
| **tUSDC**    | `0xC3c9e322F4aAe352ace79D0E62ADe3563fB86e87` | Interest-bearing token for USDC deposits.    |
| **tUSDT**    | `0xc68351B9B3638A6f4A3Ae100Bd251e227BbD7479` | Interest-bearing token for USDT deposits.    |
| **tfastUSD** | `0x92e51466482146E71b692ced2265284968E8B3d6` | Interest-bearing token for fastUSD deposits. |
| **tiSEI**    | `0xda642A7821E91eD285262fead162E5fd17200429` | Interest-bearing token for iSEI deposits.    |

***

### **Underlying Assets**

| Name        | Address                                      | Description                      |
| ----------- | -------------------------------------------- | -------------------------------- |
| **USDC**    | `0x3894085Ef7Ff0f0aeDf52E2A2704928d1Ec074F1` | Circle’s USD stablecoin.         |
| **USDT**    | `0xB75D0B03c06A926e488e2659DF1A861F860bD3d1` | Tether’s USD stablecoin.         |
| **WSEI**    | `0xE30feDd158A2e3b13e9badaeABaFc5516e95e8C7` | Wrapped SEI.                     |
| **fastUSD** | `0x37a4dD9CED2b19Cfe8FAC251cd727b5787E45269` | Synthetic USD-pegged stablecoin. |
| **iSEI**    | `0x5Cf6826140C1C56Ff49C808A1A75407Cd1DF9423` | Interest-bearing SEI asset.      |

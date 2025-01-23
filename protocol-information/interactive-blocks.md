# Collateral and Reserves

In addition to the default Markdown you can write, GitBook has a number of out-of-the-box interactive blocks you can use. You can find interactive blocks by pressing `/` from within the editor.

<figure><img src="https://gitbookio.github.io/onboarding-template-images/interactive-hero.png" alt=""><figcaption></figcaption></figure>

### lToken

One important feature of Takara Lend is the "Takara Interest-Bearing Token" (also known as "tTokens"). When you deposit in Takara Lend, you receive a corresponding amount of tTokens, which are pegged 1:1 to the underlying asset. tTokens generate interest directly in your wallet, so you can see your balance growing every second. This means you can choose to receive this interest in any Ethereum address.

### Collateral and Reserve Mechanisms

Takara Lend has implemented the collateral and reserve mechanisms used by Compound Finance.

Each supported asset on Takara is integrated through tToken contracts. tTokens are tokens that comply with the EIP-20 standard and represent the user's asset balance provided in the protocol. By minting tTokens, users can (1) earn interest based on the tToken's exchange rate, which appreciates relative to the underlying asset, and (2) use tTokens as collateral.

tTokens are the primary means of interacting with the Takara Lend protocol. Users can perform operations such as minting, redeeming, borrowing, repaying borrowings, liquidating borrowings, or transferring...


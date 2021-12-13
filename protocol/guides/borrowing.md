---
id: borrowing
title: Borrowing
sidebar_position: 1
---

# Borrowing

To lend, access the "Borrow" tab in the [Hifi Interface](https://app.hifi.finance). You will need some collateral
tokens to do this (e.g. WBTC or WETH).

Borrowing on Hifi is a simple three-step process:

1. You choose an asset you want to borrow
2. You add collateral
3. You review and initiate the transaction.

The fixed interest rate you receive when borrowing is determined by our built-in [automated
market](../technical-reference/market-making/hifi-pool.md). The more you borrow, the higher your interest rate may be. All loans in Hifi require over-collateralization with a greater value of collateral than debt. If you do not maintain a sufficient amount of collateral in your vault at all times, your vault may be liquidated.

Hifi allows you to borrow at a fixed rate for a fixed term, but you may repay early if you choose. Repaying early may result in you not receiving your original fixed rate, so give some consideration to how long you plan to have the loan when determining which maturity to borrow.

## Borrowing Explained

To borrow, you deposit collateral in the protocol and draw new hTokens against the collateral. You may proceed to sell
the hTokens for the underlying token, locking in your borrowing rate. Hifi has a built-in automated market maker (AMM) to enable efficient selling of hTokens.

At maturity, you must repay the debt to reclaim your collateral. Of course, you may also repay your debt earlier than the maturity by returning the hTokens you have drawn. Interest rate changes may affect (positively or negatively) the amount of the borrowed asset you need to spend to obtain the needed hTokens. Be careful when repaying earlier as you may incur higher interest rates than paying at maturity.

:::caution
After maturity, if you don't close your borrowing position, anyone can liquidate your position even if you're
over-collateralized. Make sure to monitor your vault closely and repay your borrow before maturity.
:::

## Example

To borrow USDC, as a user you have to mint hUSDC (for users of the Hifi Interface, this step is abstracted away).
Assuming ETH is $4000:

1. You deposit 0.5 ETH of collateral (worth $2,000) in teh system. The usual collateral ratio for ETH is 125%, so you are allowed to
   borrow up to 1,600 hUSDC from any of the available maturities.
2. You decide on Jan 31, 2022 to borrow 1,000 hUSDCMar22 (an hToken expiring on Mar 31, 2022).
3. You sell the hUSDCMar22 on the open market for 987.9 USDC.

Effectively, you have borrowed 987.9 USDC today and have 1,000 USDC debt, due in 3 months. In other words, you have
borrowed at 5% APR.

After maturity is reached on Mar 31, 2021, you may return and pay the 1,000 USDC debt and get back your collateral.
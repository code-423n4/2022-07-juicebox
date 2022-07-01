# Juicebox V2 contest details
- $71,250 USDC main award pot
- $3,750 USDC gas optimization award pot
- Join [C4 Discord](https://discord.gg/code4rena) to register
- Submit findings [using the C4 form](https://code4rena.com/contests/2022-07-juicebox-v2-contest/submit)
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts July 1, 2022 20:00 UTC
- Ends July 8, 2022 20:00 UTC

Watch the [audit intro](https://youtu.be/FMMuuG-g3Ac) to learn more.

# Juicebox Protocol

## What is Juicebox?
The Juicebox protocol is a programmable treasury. Projects can use it to configure how its tokens should be minted when it receives funds, and under what conditions those funds can be distributed to preprogrammed addresses or reclaimed by its community. These rules can evolve over funding cycles, allowing people to bootstrap open-ended projects and add structure, constraints, extensions, and incentives over time as needed. The protocol is light enough for a group of friends, yet powerful enough for a global network of anons sharing thousands of ETH, ERC-20s, or other assets.

The protocol is nuanced, however. The goal of the [protocol docs](https://info.juicebox.money/) is for you to find any protocol related information that you're looking for. These docs should allow you to click around and get a real good deep dive, and should just as easily allow you to find overview information.

## How to approach the Juicebox Code4rena audit
The Juicebox protocol is entirely unique. To understand how the protocol works, we *highly* suggest you read through the extensive documentation on http://info.juicebox.money. First, get an overview of the docs in the [Learn](https://info.juicebox.money/dev/learn) section, then dive into the main functional routines in [Build/Basics](https://info.juicebox.money/dev/build/basics). 

Please note: As a flexible and extensible fundraising protocol, Juicebox is aware of many attack vectors that are part of its design. Please make sure when reporting bugs that you are *not* including known risks addressed on the [Risks](https://info.juicebox.money/dev/learn/risks) page of the documentation. If you are unsure if something you've found constitutes a known risk, please feel free to reach out to a member of our team or report it anyway and we will evaluate the validity of the reported bug during the post-contest review phase. 

If you have questions about the protocol or where to start, don't hesitate to reach out in our [Discord](https://discord.gg/juicebox) or DM our development team (see Contact Information below).

## Contact Information

| Contact| Discord | Telegram | Twitter|
| -------- | -------- | -------- | -----|
| Jango     | jango#0420     | [me_jango](https://t.me/me_jango)     | [me_jango](https://twitter.com/me_jango/)     |
|DrGorilla | DrGorilla.eth#8862 | [DrGorilla_md](https://t.me/DrGorilla_md) | [DrGorilla_md](https://twitter.com/DrGorilla_md) |
| LuckyKoala | LuckyKoala#1024 | |[twodam_eth](https://twitter.com/twodam_eth/)|
| Nicholas | nicholas#7777 | nnnnicholas | [nnnnicholas](https://twitter.com/nnnnicholas) |

## Contest Scope

The protocol is made up of 7 core contracts and 3 surface contracts. All of these contracts are **in scope**.

The [Risks](https://info.juicebox.money/dev/learn/risks) section of the documentation describes known risks. Everything listed on this page is **out of scope**. 

### Core contracts

Consult the [Juicebox Contracts here](https://github.com/jbx-protocol/juice-contracts-v2-code4rena).

Core contracts store all the independent components that make the protocol work. 

- JBTokenStore
- JBFundingCycleStore
- JBProjects
- JBSplitsStore
- JBPrices
- JBOperatorStore
- JBDirectory

### Surface contracts

Surface contracts glue core contracts together and manage funds. Anyone can write new surface contracts for projects to use.

- JBController
- JBPayoutRedemptionPaymentTerminal
  - JBSingleTokenPaymentTerminalStore
    - JBETHPaymentTerminal
    - JBERC20PaymentTerminal

For more information on these contracts and how they fit together, please visit the [Architecture](https://info.juicebox.money/dev/learn/architecture) page of the docs. The bonus utility contracts listed at the bottom of this page are out of scope.

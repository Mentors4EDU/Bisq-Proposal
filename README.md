> _This is a Bisq Network proposal. Please familiarize yourself with the [submission and review process](https://bisq.wiki/Proposals)._

<!-- Please do not remove the text above. -->

Background: In response to #330 having social trading, and me wanting to also do social trading for a while as well, I decided to work on this proposal. I think Bisq can utilize some variation of social trading and I have a general idea of features I would hope for.

# Overview
Bisq as a decentralized exchange has the potential for many social aspects and technological implementations. One of those aspects could be an integration of some form or variation of social trading. Social trading as a concept is open and transparent given the utilization of actual statistics and insights based off of skills or trading abilities. This proposal is on an open-source implementation of social trading on Bisq's network.

# Base Modules
There will need to be a series of modules and/or components integrated into this project. Having something modularly built will allow for easy upgrading, and I do take somewhat of an inspiration from the Bisq-2.0 proposals. If something isn't modularly built, not only is upgrading a hassle. For certain issues, debugging and mantaining over time can also be hectic.

## Profile
The profile needs to have just the basics. Optionally, it doesn't really have to have a profile picture but can denote some sort of icon given that a profile picture is just meaningless data storage. *(At least in this instance)*. It depends on the community's preference. What it will have will include a description, a link to website, and a button to view trade history. It will also include metrics in regards to percentages for YoY returns. There will be a follow trades button which the user can input a certain percentage such as the default commission being 5% or set a custom fee. The ability to chose between both fee and percentage can offer flexibility for many users.

## Trade History
Users can have the option between trading in real time or with a test network. Obviously, you only earn for real trades. There will be a tab for real time trades and test network trades. The tabs for trade history will only show entry and exit prices and percentages, it will not show how much money was put in order to encourage fair markets and a layer of anonymity.

## Simulation Modes
You will be able to see simulation charts for the different trading histories and have the option to follow user's trades. You can follow trades that users do with real money including test network strategies. You can also run simulation tests. When following test network strategies with real money, that means every time the user inputs a simulated trade, you are actually doing that trade with real money. This is similar to other social trading websites such as Collective2's TOS badge or eToro's hypothetical performance charts.

For charting and market data, we would use the default Bisq charts or build untop of them.

## Support for Scripts
I recommmend support for the [Julia programming language](https://julialang.org/), given it is suited for numerical analysis and perfect for quant traders. I think you can utilize some sort of [embedded API](https://docs.julialang.org/en/v1/manual/embedding/) for implementation. There are many things in regards to what support for Julia could do. People can not just make manually traded strategies, but also make trading strategies that are automated or custom indicators that people can trade with for a fee percentage or custom licensing fee. The support for both manual and robotraders is something many social trading networks have, and support for Julia can attract alot of quants and mathematicians. Optionally, we can add secondary support for Python as well, but the use of Python has already been overly utilized. 

In regards to Julia, packages such as the [decentralized-internet](https://github.com/Lonero-Team/Decentralized-Internet) SDK, [Gen](https://www.gen.dev/), [Quandl.jl](https://juliapackages.com/p/quandl), [TradingLogic.jl](https://juliapackages.com/p/tradinglogic), [FinMarkets.jl](https://juliapackages.com/p/finmarkets), [Ito.jl](https://juliapackages.com/p/ito), and [TradeModels.jl](https://juliapackages.com/p/trademodels) can come pre-installed to support custom developer environments.

## Ranking Mechanism
In regards to the ranking mechanism, I believe the UML below best illustrates how that will play out:



The ranking mechanism needs to support fairness and decentralization. That is why profiles are going to be ranked on performance-based metrics rather then how many people are following their trades.

## Test and Realtime Support

## Disclosures

# Roadmap 

# Project Goals

## Basic Community Acceptance

## Get Funding

## Design and Mockups

## Hiring Team

## Marketing

## MVP Built

## Project Launch

*For sake of transparency, in regards to issue edits based on consensus, you can see the draft history via the repo [here](https://github.com/Mentors4EDU/Bisq-Proposal). This is as of the writing of this proposal.*

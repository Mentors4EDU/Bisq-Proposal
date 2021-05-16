> _This is a Bisq Network proposal. Please familiarize yourself with the [submission and review process](https://bisq.wiki/Proposals)._

<!-- Please do not remove the text above. -->

**Background:** In response to #330 having social trading, and me wanting to also do social trading for a while as well, I decided to work on this proposal. I think Bisq can utilize some variation of social trading and I have a general idea of features I would hope for.

#### Table of contents

1. [Overview](https://github.com/Mentors4EDU/Bisq-Proposal#overview)
2. [Base Modules](https://github.com/Mentors4EDU/Bisq-Proposal#base-modules)
    - [Profile](https://github.com/Mentors4EDU/Bisq-Proposal#profile)
    - [Trade History](https://github.com/Mentors4EDU/Bisq-Proposal#trade-history)
    - [Simulation Modes](https://github.com/Mentors4EDU/Bisq-Proposal#simulation-modes)
    - [Support for Scripts](https://github.com/Mentors4EDU/Bisq-Proposal#support-for-scripts)
    - [Ranking Mechanism](https://github.com/Mentors4EDU/Bisq-Proposal#ranking-mechanism)
    - [Test and Realtime Support](https://github.com/Mentors4EDU/Bisq-Proposal#test-and-realtime-support)
    - [Disclosures](https://github.com/Mentors4EDU/Bisq-Proposal#disclosures)
        - [Regarding Privacy](https://github.com/Mentors4EDU/Bisq-Proposal#regarding-privacy)
3. [Roadmap](https://github.com/Mentors4EDU/Bisq-Proposal#roadmap)
4. [Project Goals](https://github.com/Mentors4EDU/Bisq-Proposal#project-goals)
    - [Basic Community Acceptance](https://github.com/Mentors4EDU/Bisq-Proposal#basic-community-acceptance)
    - [Get Funding](https://github.com/Mentors4EDU/Bisq-Proposal#get-funding)
    - [Design and Mockups](https://github.com/Mentors4EDU/Bisq-Proposal#design-and-mockups)
    - [Hiring Team](https://github.com/Mentors4EDU/Bisq-Proposal#hiring-team)
    - [Marketing](https://github.com/Mentors4EDU/Bisq-Proposal#marketing)
    - [MVP Built](https://github.com/Mentors4EDU/Bisq-Proposal#mvp-built)
    - [Project Launch](https://github.com/Mentors4EDU/Bisq-Proposal#project-launch)

# Overview
Bisq as a decentralized exchange has the potential for many social aspects and technological implementations. One of those aspects could be an integration of some form or variation of social trading. Social trading as a concept is open and transparent given the utilization of actual statistics and insights based off of skills or trading abilities. This proposal is on an open-source implementation of social trading on Bisq's network.

# Base Modules
There will need to be a series of modules and/or components integrated into this project. Having something modularly built will allow for easy upgrading, and I do take somewhat of an inspiration from the Bisq-2.0 proposals. If something isn't modularly built, not only is upgrading a hassle. For certain issues, debugging and maintaining over time can also be hectic.

## Profile
The profile needs to have just the basics. ~~Optionally, it doesn't really have to have a profile picture but can denote some sort of icon given that a profile picture is just meaningless data storage. *(At least in this instance)*. It depends on the community's preference.~~ What it will have will include ~~a description, a link to website, and~~ a button to view trade history. It will also include metrics in regards to percentages for YoY returns. There will be a follow trades button which the user can input a certain percentage such as the default commission being 5% or set a custom fee. The ability to chose between both fee and percentage can offer flexibility for many users.

*These features have been crossed out to preserve the privacy-preserving nature of the network (even though they are optional). This is as to not pressure someone into thinking they need to be included*

## Trade History
Users can have the option between trading in real time or with a test network. Obviously, you only earn for real trades. There will be a tab for real time trades and test network trades. The tabs for trade history will only show entry and exit prices and percentages, it will not show how much money was put in order to encourage fair markets and a layer of anonymity.

## Simulation Modes
You will be able to see simulation charts for the different trading histories and have the option to follow user's trades. You can follow trades that users do with real money including test network strategies. You can also run simulation tests. When following test network strategies with real money, that means every time the user inputs a simulated trade, you are actually doing that trade with real money. This is similar to other social trading websites such as Collective2's TOS badge or eToro's hypothetical performance charts.

For charting and market data, we would use the default Bisq charts or build untop of them.

## Support for Scripts
I recommend support for the [Julia programming language](https://julialang.org/), given it is suited for numerical analysis and perfect for quant traders. I think you can utilize some sort of [embedded API](https://docs.julialang.org/en/v1/manual/embedding/) for implementation. There are many things in regards to what support for Julia could do. People can not just make manually traded strategies, but also make trading strategies that are automated or custom indicators that people can trade with for a fee percentage or custom licensing fee. The support for both manual and robotraders is something many social trading networks have, and support for Julia can attract alot of quants and mathematicians. Optionally, we can add secondary support for Python as well, but the use of Python has already been overly utilized. 

In regards to Julia, packages such as the [decentralized-internet](https://github.com/Lonero-Team/Decentralized-Internet) SDK, [Gen](https://www.gen.dev/), [Quandl.jl](https://juliapackages.com/p/quandl), [TradingLogic.jl](https://juliapackages.com/p/tradinglogic), [FinMarkets.jl](https://juliapackages.com/p/finmarkets), [Ito.jl](https://juliapackages.com/p/ito), and [TradeModels.jl](https://juliapackages.com/p/trademodels) can come pre-installed to support custom developer environments.

## Ranking Mechanism
In regards to the ranking mechanism, I believe the UML below best illustrates how that will play out: \
![UML_SocialTrading](https://raw.githubusercontent.com/Mentors4EDU/Bisq-Proposal/main/Images/Social%20Trading.PNG) \
The ranking mechanism should support fairness and decentralization. That is why profiles are going to be ranked on performance-based metrics rather than how many people are following their trades. The metrics are going to be: Categories for YoY estimated ROI %, ROI % per Trade, and a Risk Tolerance subcatagory. Risk tolerance in regards to uncertainty is measured by drawdown percentage in relation to returns. The better one performs, the higher they are ranked in a certain category. Performance-based is the best type of ranking mechanism in the world of trading.

## Test and Realtime Support
As noted, both trades on a test network and realtime strategies can be followed. The same applies whether it is manual or automated. This is actually a good thing, because along with the ranking mechanism, traders can be rewarded on skills rather then them putting large amounts of money in their strategies upfront. Also, lower income traders might be higher skilled then some higher income traders. Leveling up the playing field is key.

## Disclosures
Likely some sort of risk disclosure will need to be implemented that is site-wide and usage specific. This is due to the nature of exchanges and social trading in general, and the disclosure text can be open-sourced or within the public domain.

## Regarding Privacy
~~I think users can have the option of being public to an extent *(description and site profile fields)*, or having some level of anonymity or pseudonymity.~~ There has been comments in the past regarding levels of pseudonymity, and I believe the network can still have privacy-centric aspects to it. This will be one of the key focuses or aspects to look at in regards to development.

*These comments have been crossed out to preserve the privacy-preserving nature of the network (even though they are optional). This is as to not pressure someone into thinking they need to be included*

# Roadmap 
There are lots of things to take into consideration in regards to building this platform. Most likely from acceptance and funding to MVP, the timeline is 4 to 5 month with around 4 to 7 part time and voluntary software developers. More details will be in the funding section. This is almost the equivalent of building a full scale exchange given the advancements needing to be in place, but it is a very ambitious and promising project.

# Project Goals
In regards to project goals, besides a basic *ACK*, we are trying to get funding, design, build and market the platform. My goal is to eventually maintain this and personally work on marketing this platform and bringing more awareness towards Bisq. There are already lots of mediums I have to market this as a career-long startup advisor, and I have a general idea of how I will be managing the technological implementations of this project.

## Basic Community Acceptance
We are hoping to receive an *ACK* for this proposal. Please keep in mind that proposals can be commented on, discussed and updated over time. Also, remember criticism is best handled with a degree of respect and politeness within the context of the idea being critiqued.

## Get Funding
The funding I am looking for is around 35k Bisq done through the Bisq DAO. Although this is negotiable, I calculated how much it would cost for the potential hiring of engineers + my time allocation. The actual [COCOMO model](https://www.javatpoint.com/cocomo-model) would suggest probably alot more. Also, I would want a 0.25% trading fee in regards to project maintenance over time *(from the social trading only)*. Keep in mind this will still be open-source. Again, the funding will likely be crucial given lots of time will be voluntary and the low volume of Bisq as well

## Design and Mockups
Part of this project will also include a design phase. We want to make sure that the design fits well with Bisq's current UI and UX. This includes everything from trade history and order books to its social aspects.

## Hiring Team
The team will be paid from the Bisq funding pool. I will be taking the role of mostly a PM and CTO during the development process. I won't be taking from the funding pool, but rather instead be taking trading fees as a form of managing the platform over time and sort of being its chief technologist and marketing strategist. Many marketing costs that may occur afterwards will be mostly on my own dime. Henceforth, this is why the minor fee is helpful.

## Marketing
I think marketing is a thing that Bisq lacks. You can still be decentralized and theoretically teamless while focusing on others to use your software. I believe that social trading provides the opportunity to tap into markets that Bisq has yet to enter. Also, with the rise of many DEX and supposed "DeFi" apps, I believe Bisq can offer a popular alternative to what is mainstream.

## MVP Built
Once the MVP is built, we will start garnishing some community feedback and preparing for the launch.

## Project Launch
Once all the milestones are met, the MVP has been built, and things are ready for full deployment, it will be officially launch time. My focus at that time will than be marketing, network growth and scalability.

*For sake of transparency, in regards to issue edits based on consensus, you can see the draft history via the repo [here](https://github.com/Mentors4EDU/Bisq-Proposal). This is as of the writing of this proposal.*

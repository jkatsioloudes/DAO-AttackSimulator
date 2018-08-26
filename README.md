# Simulator in Action through Examples

Running this simulator in Python 3.6, someone could understand the impact of a potential malicious attempt against Dash Decentralised Governance (please read the 'Concepts' part that follows for the necessary theory around the examples that follow).  The user is provided with the capability of customising a variety of parameters involved such as:
* Price ($)
* Price Increase Factor (1-10)(1: Aggressive, 10: Slow)
* Number of Active masternodes
* Coins in Circulation (in Millions)
* Masternodes under control

The simulator is then able to suggest further steps forward with goal to maximise the impact.  Below, we are going to view the output of two example attacks.

## Assumptions for the Examples that follow

* Dash current rules will remain the same. The most important are:
    – The collateral required is 1,000 DASH.
    – A budget to be initially accepted requires at least 10% net votes.
* We relax the assumption of budget proposal payments ordered by the percentage of net votes achieved if the super block contains sufficient funds to fully pay – partial payments are not accepted – every valid proposal.
* All of the existing masternodes are behaving honestly in all operations required.
* All of the existing masternode owners are voting, having 0% voting abstention; this is actually a very strong assumption.
* Only the adversary’s newly registered masternodes have malicious intentions.
* The timing of attack leaves the minimum possible window of reaction.

## Progressive Attack

The profile of this attacker is that is silently and progressively trying to establish a higher amount of masternodes. The initial goal is to stay undetected by avoiding a sudden coin price increase but more importantly a suspicious increased number of masternodes against all historical data by maintaining the average number of newly registered masternodes at any given time. Let us firstly buy 500 masternodes that is a very high number as well as it is a high fraction (around 12.5%) of the current network but purchasing this number is currently not enough to harm. Notice the suggestions at the end are customised on how to remain stealthy as the outcome of both attacks is the same because of the number of coins in circulation.

#### Simulation Output ####

`
-- DASH CORRUPTED GOVERNANCE ATTACK SIMULATOR --
-- Please provide customised information for any parameter OR -- Press enter to proceed with the real time values --

Customised Price($): (press enter for real time price)
Price Increase Factor (1-10)(1: Aggressive, 10: Slow): (press enter for default factor)
Number of Active masternodes: (press enter for real time active MN)
Coins in Circulation (in Millions): (press enter for real time circulation)
How many masternodes you want to control?: (press enter for net 10% malicious MN) 500

-- VALUES PROCEEDING WITH -- Price: $297.39
Price Increase Factor (in Decimal): 1.1195484842590947e-05
Number of Active Masternodes: 4827
Coins in circulation: 8096297.0

-- PROCEEDING TO THE PURCHASE OF 500 MN --
Dash Price before purchase: $297.39
Active Masternodes before purchase: 4827
Coins in circulations before purchase: 8096297.0
From which coins frozen for required collaterals: 4827000
Therefore, coins remaining unfrozen: 3269297.0
These are enough to purchase up to this number of MN: 3269

-- PURCHASE OUTCOME: POSSIBLE! --
New Dash Price after this investment: $302.9877
Total Cost of Purchase (including dynamic price increase): $150094432.80497262
Coins in circulations after purchase: 8096297.0
From which coins frozen for required collaterals: 5327000
Therefore, coins remaining unfrozen: 2769297.0
Which are enough to acquire more MN, actually: 2769 MN
Which as a percentage, takes this share from the total active MN: 67.7%
This percentage is high, but not enough to achieve a net 10% over honest masternodes Active Masternodes after purchase: 5327
From which malicious: 500 (9.38%)
Therefore, the honest nodes have the net majority!

-- PROCEEDING TO PLAN B: WHAT PROBLEMS CAN WE CAUSE RIGHT NOW? --
1) Prevent honest proposals to go through! (i.e: The salaries of Dash Core Developers) Explanation: We vote ‘‘no" for a proposal and we hope that net 10% can’t be achieved!
The number of MN we acquired above is: 500 MN
It means that for a proposal to get accepted, it would need these positive votes: 551 MN Maximum possible amount of MN we can acquire due to coins in circulation is: 3269 MN
It means that for a proposal to get accepted, it would need these positive votes: 3597 MN WHY: Anything below the required amount of votes will cause a proposal rejection.

2) Acts of Negligence -- Achievable? YES!
Explanation: We vote ‘‘yes" for a proposal and we hope in a high % of voting abstention!
With this amount of MN under our control, which is: 500 MN
A budget proposal will be approved even if this number of honest MN votes against: 454 MN
Given that the maximum votes ever recorded for funding a proposal is: 2147 MN (44.47%)
Assuming that a controversial proposal will drastically increase this,
we will consider a higher percentage of 60% voters, this means: 2896 MN
Which means that we would need this amount of MN to achieve net 10%: 3186 MN
Maximum possible amount of MN we can acquire due to coins in circulation is: 3269 MN
Remember that the remaining coins are enough to acquire more MN, actually: 2769 MN
OUTCOME: If we acquire them, then we achieve net 10% in case that 60% of honest MN vote.
WHY: Total number of malicious masternodes will become: 3269 MN
    and we previously needed at least this amount for majority: 3186 MN

3) Maintain a stealthy future
Current supply (% against total): 8096297.0 (42.8%)
Total (ever) coin supply: 18900000
Remaining Supply/Possible new MN: 10803703.0 / 10803
Below is the minimum number of coins expected per year along with (%) against total coin supply:
Expected mined coins until 04/2019(%)/Possible new MN: 8761092 (46.3%) / 664
Expected mined coins until 04/2020(%)/Possible new MN: 9486800 (50.14%) / 1390
Expected mined coins until 04/2021(%)/Possible new MN: 10160671 (53.7%) / 2064
Furthermore: 08/2029 (74.41%), 03/2043 (90.23%), 05/2073 (98.86%), 04/2150 (100%)

SUGGESTED APPROACH:
A stealthy attacker can slowly increase his/her army assuming a percentage gain of 50% mined DASH => MN per year. Towards this DASH required, the attacker might use Proof-of-Service rewards able to purchase 25 new MN per existing MN per year (assuming 7.14% Return
on Investment). An increase of 1K MN could take 4-5 years to be achieved and does not guarantee success! Notice that in the long term, more years would be needed to acquire further 1K MN!
`

## Suddent Counterattack

The profile of this attacker resembles a government or nation. The main characteristics of this malicious actor include greediness and capability to spend unlimited money any time to meet the end goal or ambition. To achieve a successful outcome, the adversary needs to acquire 5311 masternodes (in the simulator we do so by pressing *enter* when asked initially) because this is going to be 10% more than the current number of masternodes which we assumed is honest. But we see that this number is not achievable since the remaining coins in circulation are inadequate.

#### Simulation Output ####

`
-- DASH CORRUPTED GOVERNANCE ATTACK SIMULATOR --
-- Please provide customised information for any parameter OR -- Press enter to proceed with the real time values --

Customised Price($): (press enter for real time price)
Price Increase Factor (1-10)(1: Aggressive, 10: Slow): (press enter for default factor)
Number of Active masternodes: (press enter for real time active MN)
Coins in Circulation (in Millions): (press enter for real time circulation)
How many masternodes you want to control?: (press enter for net 10% malicious MN)

-- VALUES PROCEEDING WITH --
Price: $296.624
Price Increase Factor (in Decimal): 1.1195484842590947e-05 Number of Active Masternodes: 4827
Coins in circulation: 8096297.0

-- PROCEEDING TO THE PURCHASE OF 5310 MN --
Dash Price before purchase: $296.624
Active Masternodes before purchase: 4827
Coins in circulations before purchase: 8096297.0
From which coins frozen for required collaterals: 4827000 Therefore, coins remaining unfrozen: 3269297.0
These are enough to purchase up to this number of MN: 3269

-- PURCHASE OUTCOME: IMPOSSIBLE! --
WHY: The reason is because the coins required for this purchase are not enough as
    they exceed the total available coin supply!
New Dash Price after this investment: $356.0720
Total Cost of Purchase (including dynamic price increase): $1732907915.1941507
Coins in circulations after purchase: 8096297.0
From which coins frozen for required collaterals: 10137000 <------ (Problematic Result)
Therefore, coins remaining unfrozen: -2040703.0 <------ (Problematic Result)
The available coin supply was enough to buy this amount of MN: 3269 MN
But we requested the purchase of 5310 MN <------ (Problematic Result)

-- PROCEEDING TO PLAN B: WHAT PROBLEMS CAN WE CAUSE RIGHT NOW? --
1) Prevent honest proposals to go through! (i.e: The salaries of Dash Core Developers) Explanation: We vote ‘‘no" for a proposal and we hope that net 10% can’t be achieved! The maximum possible MN that we can acquire due to coins in circulation is: 3269 MN This means that for a proposal to get accepted needs these positive votes: 3597 MN WHY: Anything below the required amount of votes will cause a proposal rejection.

2) Acts of Negligence -- Achievable? YES!
Explanation: We vote ‘‘yes" for a proposal and we hope in a high % of voting abstention!
Given that the maximum votes ever recorded for funding a proposal is: 2147 MN (44.47%)
Assuming that a controversial proposal will drastically increase this,
we will consider a higher percentage of 60% voters, this means: 2896 MN
Which means that we would need this amount of MN to achieve net 10%: 3186 MN
Maximum possible amount of MN that we can acquire due to coins in circulation is: 3269 MN
`

# Essential Concepts

## Dash Decentralised Governance

Governments have been always in human’s life, started from local tribe leaders being responsible for interacting with other leaders or deciding on internal issues. In modern democratic governments, we have a small group of people elected to participate in the parliament which is responsible to represent and decide for a way larger group of people, most of the time as a result of someone’s interaction with political parties, and a government being responsible to lead. But what if the blockchain technology could also provide the alternative to centralized governance at least for the decisions affecting the future of a coin? What if coin holders could vote in a decentralized governmental fashion that allows more freedom and larger scale democracy to thrive?

Decentralised Autonomous Organisation (DAO) is here to solve two vital challenges in cryptocurrencies: governance and funding. The governance actions include a voting process held within one month where masternode holders decide the distribution of the budget with goal to trigger improvement in the coin and the community. As the official documentation informs us about budget voting, every 16,616 blocks (approximately 28 days), a super block is created that contains the entire 10% payout to the budget proposal winners. This 10% of the super block was the accumulated funding of all 16,616 blocks discovered during the previous 28 days from which each block contributed by 10% as seen before. Moreover, the documentation mentions that every masternode owner is allowed vote once (yes/no/abstain) for each proposal and for one to get accepted, a net of 10% more positive than negative votes is required plus the condition for budget to be enough for all proposals before the deadline which is considered to be two days before the next super block.

A key example was in early 2016, when Dash Core Team submitted a proposal to the network asking whether the block size should increase to 2 MB and within the next hours a decision had been achieved and block size changed compared to Bitcoin where the block size limit argument has unofficially started in 2010, it is still around and any decision would show centralisation.

## Masternodes

Masternodes are the backbone of Dash! Based on Dash Official Documentation on masternodes, they can be thought as dedicated full node servers that satisfy minimum collateral and power requirements as set by the Dash network which guarantees a certain minimum level of performance and functionality to execute InstantSend, PrivateSend and Decentralised Governance. 

Their existence is directly related to the level of security and speed of the whole network because more masternodes mean higher availability, stronger security through higher randomness and a faster and more scalable Dash network. Having so many servers holding a full copy of the blockchain and working honestly is the recipe of success. The reward system is the biggest incentive for masternode owners to remain active and honest at all times, otherwise a very low masternode availability poses severe security risks such as reduced randomness.

Currently there exist around 4,800 distributed servers and these act as an extra layer of protection above miners which means that Dash can scale more efficiently and deploy services more quickly than blockchains and full nodes hosted entirely by unpaid volunteers. As of mid June 2018, the Dash network has over 4,800 masternodes located in over 40 countries and hosted on 98 ISPs while masternode registration evolution from October 2014 to July 2017.

## Attack Simulation

Let me be unrealistic for a moment so that someone can understand the amount of influence that masternodes have in the network. Consider for example governance in case there exists a proposal to increase masternodes reward from 45% to 60% by decreasing miners reward to 30% of the block reward (remember that 10% goes to master block for budget funding). This decision will affect the integrity of the network, introduce friction and a possible miner withdrawal from the cryptocurrency. Masternodes have the responsibility to improve and make the network run smoothly but if an adversary has the power of controlling a net 10% of votes in favour of a malicious decision then the the model of honest governance breaks. Remember that this happens as for a successful proposal to go through, 10% more positive than negative votes are required before the deadline of approximately 28 days where a super block is found. Finalisation of what proposals are funded occurs 48 hours before super block and is stochastic. This is important for both the attacking and defending parties because the vote freeze can happen any time which includes uncertainty.

But why is the above proposal and scenario unrealistic then? Because proposals are scrutinised before votes cast and if the attacking party is not informed about it then great suspicion will be raised followed by measures against it. More importantly however, even if the proposal has not this nature of changing the reward percentages, what someone could do is to submit a scam for which no real benefit to the protocol is gained. But is this beneficial? What game theory suggests in the measurements explained below is that the amount of DASH shared in the super block is not bigger and is not going to be bigger for many years than the amount invested to acquire these 4-5K masternodes even if the whole block is paid for one proposal. But is this possible? From the below measurements and what was shown in the previous chapter where governance was initially explained, someone can see that the super block amount is paid by descending order of net votes acquired which means that the attacker needs way more masternodes that just a simple 10%.

In my opinion, the fact that a successful exploitation of this attack is sufficient to destroy Dash no matter how this cryptocurrency is defending against it is important and should be examined more carefully even if our measurements show that is protected. My reasoning is because we make very strong assumptions that there will be no voting abstention and that all masternode owners are rationale but once malicious majority is achieved, there is no legal way to avoid any proposal to go through. Nonetheless, as you are going to see shortly from my findings, Dash Sybil attack defence is effective at this point due to the number of coins in circulation and not because of cost, which I find totally subjective. Since the maximum number of masternodes that will be ever registered is not capped to a specific number, it can be in theory equal to the total number of DASH in circulation divided by the collateral of 1,000 DASH even if this means that no coins will be left unfrozen for anything else apart from collaterals.

---
title: "Less Is More: How I Learned to Simplify My Trading"
date: 2026-09-12
toc: true
giscus: true 
tags: ["technical analysis", "trading indicators", "volume analysis", "trading setup"]

---

## Setup: Winning Trades Without Understanding Why

I have been trading for a couple of years now, and like many traders, I started with support and resistance. I drew horizontal lines, watched how price reacted around them, and looked for opportunities to buy near support or sell near resistance.

Eventually, I discovered more tools: MACD, RSI, and divergence. Each concept gave me another way to interpret the chart. Sometimes, those signals led to winning trades.

But I still wasn’t consistently profitable.

What bothered me most was the uncertainty behind those wins. Had I identified something repeatable, or had the market simply moved in my favor? I could point to an indicator signal, but I could not confidently explain why that signal deserved a trade.

That pushed me to look deeper into how price moves and how indicators are calculated.

Gradually, my question changed from “Which indicator is best?” to “What information does this indicator actually give me?”

Understanding the calculation helped me understand the tool. It also exposed how often I was looking at the same information in different forms.

That became the starting point for simplifying my trading.

## Problem: More Confirmation Can Become More Confusion

At first, adding indicators felt like adding protection.

If support suggested a buy, perhaps RSI could confirm it. If RSI agreed, perhaps MACD could provide another reason. Then I could add a moving average, a chart pattern, and a volume signal.

The problem was that every extra condition created another decision.

What if four indicators agreed and two disagreed? Which deserved more weight? Was I evaluating a setup consistently, or choosing whichever signals supported the trade I already wanted?

A crowded chart gave me more explanations without necessarily giving me better evidence.

### Agreement Is Not Probability

I used to think about confluence as a percentage. If three out of five conditions supported a trade, that was 60%. If I reduced the checklist and two out of three agreed, that became approximately 67%.

The arithmetic is correct. The interpretation needs care.

**Those percentages describe checklist agreement, not the probability of a winning trade.**

Removing conditions does not automatically improve the odds. Two weak signals can agree, and several indicators can repeat the same underlying information.

For example, MACD and moving averages both derive information from price averages. Treating their agreement as two independent votes can exaggerate how much confirmation I actually have.

To estimate a win rate, I need results from consistently defined trades. Even then, win rate alone does not establish profitability.

A strategy winning 40% of trades can have positive expectancy if its average winner is twice its average loser:

**Expectancy = (0.40 × 2R) − (0.60 × 1R) = +0.20R per trade before costs.**

Here, *R* means the amount initially risked. Trading costs and execution can reduce that result.

### More Parameters Do Not Automatically Mean More Accuracy

My original intuition was that more variables make accuracy harder to achieve. A more precise explanation is that additional parameters create more opportunities to fit historical noise.

If I keep changing indicator settings until old trades look excellent, I may build rules that describe the past without working reliably on new data. That is overfitting.

Complexity can be useful when it adds meaningful information. But each additional condition should justify its place through testing.

Likewise, understanding an indicator does not mean every indicator will produce a profitable strategy. It helps me identify what the tool measures, where it might help, and where its limitations matter.

## Solution: Give Every Tool a Clear Job

I built my approach around two main questions:

**What is price doing, and what does the available volume information suggest about that movement?**

There are still many tools within those categories. My solution is to assign each selected tool a purpose.

| Tool | Its role in my process |
|---|---|
| Heikin Ashi | Make the prevailing trend easier to visualize |
| Stochastic | Assess price momentum within its recent range |
| Money Flow Index (MFI) | Examine pressure using both price and volume |
| Cumulative Volume Delta (CVD) | Examine accumulated volume delta |
| VWAP | Provide a volume-weighted price reference |
| Weighted moving average (WMA) | Provide a reference that emphasizes recent prices |

I still use six tools. For me, “less is more” means reducing redundant decisions and keeping a limited set of tools with understandable roles.

Their value depends on whether each contributes something useful.

### 1. Prepare the Context Before Looking for an Entry

Before the session starts, I use top-down analysis to review the broader market structure.

Is price trending or ranging? Is it approaching an important swing high or low? Would a potential entry follow the broader direction or attempt a reversal against it?

I also check the calendar for high-impact news. Gold can respond quickly to economic and political developments, so the context around a signal matters. [CME Group’s gold overview](https://www.cmegroup.com/markets/metals/precious/gold.html) discusses these influences.

In my historical review of gold, I noticed a possible weekly rhythm: strength on Monday, continuation on Tuesday, rotation or consolidation around Wednesday, a larger drop on Thursday, and recovery on Friday.

That is an observation from the data I reviewed—not an established weekly rule.

Without a documented sample and testing across other periods, I cannot attach reliable probabilities to it. News, changing market conditions, and the period selected could all influence that apparent pattern.


I treat it as a hypothesis to investigate, while letting current structure guide the setup.

### 2. Examine Volume-Related Evidence First

After establishing context, I look at MFI and CVD for signs that the current move may be weakening.

MFI combines price and volume into a bounded oscillator. It can highlight relatively strong or weak readings and potential divergence, but it does not directly identify buying and selling at the bid and ask. An oversold reading alone does not mean a reversal is imminent. [TradingView’s MFI documentation](https://www.tradingview.com/support/solutions/43000502348-money-flow-mfi/) explains its calculation.

CVD accumulates volume delta, but its meaning depends on its implementation and data source. TradingView’s built-in version estimates buying and selling pressure from lower-timeframe price and volume movement. It should therefore be understood as an estimate, rather than assumed to be direct trade-by-trade order flow. [TradingView’s CVD documentation](https://www.tradingview.com/support/solutions/43000725058-cumulative-volume-delta/) describes that method.

CVD also has no universal overbought or oversold threshold. I examine its behavior relative to price, using consistent settings and comparable swings.

For example, price might make a lower low while MFI or CVD makes a higher low. That is bullish divergence: the indicator does not confirm the new price low.

It can suggest weakening downside pressure. It does not prove buyers have taken control.

### 3. Wait for Price to Confirm the Idea

Volume-related evidence puts a possible trade on my radar. Price behavior determines whether the idea develops.

I look for an observable change, such as reclaiming a nearby swing level or breaking the sequence of lower highs.

Heikin Ashi helps me visualize whether directional movement is becoming more consistent. Stochastic helps me assess momentum by comparing the close with its recent price range. Neither tells me with certainty which trend comes next. [TradingView’s stochastic explanation](https://www.tradingview.com/support/solutions/43000502332-stochastic-stoch/) covers its role as a momentum oscillator.

Heikin Ashi also uses synthetic prices. I use actual market prices for entries, stops, targets, and backtest execution, because averaged candle values are not necessarily tradable prices. [TradingView’s documentation on non-standard charts](https://www.tradingview.com/pine-script-docs/concepts/non-standard-charts-data/) makes this distinction explicit.

When price and an indicator support the same directional interpretation, I call that confirmation. When they fail to confirm each other, I examine the divergence.

### 4. Define Risk Before Entering

VWAP and WMA help me identify areas worth watching. They provide references, not guaranteed barriers.

I want my stop to reflect structural invalidation: the point where the reason for taking the trade no longer holds. A moving average by itself does not establish that point.

Likewise, a potential target needs enough room relative to the stop. If nearby resistance leaves little upside, an attractive-looking signal may still be a poor trade.

### A Hypothetical Gold Buy Setup

Suppose gold approaches a previously identified support area.

Price makes a low near 2,497, rebounds, and then makes a lower low near 2,496. Over those corresponding swings, MFI and CVD make higher lows.

That divergence suggests downside pressure may be weakening. I have a reason to pay attention, but no entry yet.

Next, actual price reclaims a nearby swing level and reaches 2,500. Heikin Ashi begins showing stronger upward movement, while stochastic turns higher. These observations support the emerging price change.

For this hypothetical example:

- **Entry:** 2,500 after the reclaim.
- **Stop:** 2,495, below the recent low.
- **Target:** 2,510, assuming the next relevant resistance or reference area allows that objective.

The price risk is 5 and the potential reward is 10, giving **2R before costs**. Position size determines the monetary risk.

If price breaks below the setup low before confirmation, I abandon the proposed entry. If the trade is entered and subsequently hits the stop, I accept the invalidation rather than widening the stop to preserve my original opinion.

A sell example reverses the logic: price makes a higher high near resistance, MFI/CVD make lower highs, and actual price subsequently breaks a local support level. The stop belongs above the invalidating high, with a target offering sufficient downside room.

These examples illustrate a decision sequence. They do not establish that the sequence has an edge.

## Conclusion: Simplicity Makes My Decisions Easier to Evaluate

My biggest lesson is that a clearer trading process begins with understanding what each tool contributes.

I prepare the context, examine volume-related evidence, wait for price confirmation, and define the risk. That sequence gives me something concrete to record and review.

The next test is whether those rules produce positive expectancy across sufficient trades, different conditions, and unseen data after costs.

Simplicity does not guarantee profitability. It helps me identify what I am testing and whether I am following it consistently.

For me, less is more means keeping enough information to make an informed decision—and removing the repetition that makes that decision harder to understand.
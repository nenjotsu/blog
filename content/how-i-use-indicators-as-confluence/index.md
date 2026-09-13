---
title: "How I Use Indicators as Confluence: My “Less Is More” Approach"
date: 2026-09-13
toc: true
giscus: true 
tags: ["technical analysis", "trading indicators", "volume analysis", "trading setup", "price action"]

---

## The Setup: Volume + Price Action

I mentioned before that “less is more” means simplifying my trading setup. Part of that process is decreasing the number of indicators I use and understanding the purpose of each one.

My strategy revolves around a simple combination:

**Strategy = Volume + Price Action**

Price action helps me understand what the market is doing: breaking a level, rejecting a zone, forming a pattern, or continuing a trend. Volume helps me assess the activity supporting that movement.

My preference is to choose one indicator for each idea: one volume-based tool and one price-action-based tool. The combination depends on the setup I am looking for.

For a reversal, I might choose MFI and a chart pattern. For a trend pullback, I might choose VWAP and the Stochastic Momentum Index.

The indicators below are my available toolkit. Each has a role, but I do not need all of them on the chart at once.

## The Problem: More Indicators Can Repeat the Same Information

Several indicators agreeing can feel reassuring. However, I need to ask whether they provide different information.

RSI, MACD, and a moving average all use price data. Their calculations differ, but their agreement does not automatically give me three independent reasons to enter.

Another problem is confusing an interesting condition with an entry signal. An overbought reading, divergence, or a touch of support can attract my attention before a trade is ready.

I separate my decision into three stages:

1. **Context:** What market condition am I trading?
2. **Preparation:** Is something developing at a meaningful location?
3. **Confirmation:** Has price behaved in a way that supports the entry?

That distinction helps me use confluence without letting every indicator reading become a trade.

## The Solution: Give Each Tool a Clear Job

### Volume Indicators

#### 1. Volume Profile

Volume profile is one of my preferred tools because it shows how trading activity is distributed across price levels.

I use a fixed profile covering a recent leg, a movement from the start of a session, or a move following high-impact news. The selected range matters: it needs to represent the movement I am analyzing.

My main references are:

- **VAH — Value Area High:** The upper boundary of the selected value area.
- **VAL — Value Area Low:** The lower boundary.
- **POC — Point of Control:** The price level with the most volume within that profile.

I watch VAH and VAL for break-and-retest opportunities. If price breaks above VAH, I wait to see whether it can hold that area on a retest. A breakout alone does not complete the setup.

I also use these levels as support and resistance zones. They show where activity previously concentrated, although they do not guarantee a future buying or selling response.

For take-profit (**TP**) planning, I consider VAH, VAL, and POC according to the trade’s direction and starting location. I work backward from a potential target to assess the acceptable stop-loss (**SL**) distance. However, the stop must also respect where the trade idea becomes invalid. If those requirements do not fit, I skip the setup.

I also watch for weakening activity as price extends. That can prepare me for a possible reversal, but volume profile alone does not provide a time-series divergence signal or count individual participants. Its data may also represent traded volume or tick activity, depending on the instrument and platform. [TradingView explains these volume-profile distinctions](https://www.tradingview.com/support/solutions/43000502040-volume-profile-indicators-basic-concepts/).

#### 2. VWAP

The Volume-Weighted Average Price, or **VWAP**, gives me a volume-weighted price reference. Its role overlaps with volume profile in my setup, although the two measure different things.

I can use a daily VWAP, a weekly VWAP, or an anchored VWAP starting from a meaningful movement. I choose the reference that matches the trade’s context.

The central VWAP and its multiplier bands help me identify potential reaction areas. I need to understand the band settings because different calculations and multipliers produce different levels.

I use these references for break-and-retest setups, targets, and stop planning. During an aggressive trend, I also watch the central VWAP for a possible pullback re-entry.

For example, in an uptrend, price might pull back toward VWAP after a strong advance. I watch whether buyers defend the area and price resumes its upward structure.

When the current session’s VWAP is still developing or offers an unclear reference, I may use the previous day’s VWAP levels for context. They still need to be relevant to current price action.

I avoid forcing a directional setup when price repeatedly crosses VWAP without follow-through. In that environment, a touch or crossing gives me limited information.

#### 3. MFI

The **Money Flow Index**, or MFI, combines price and volume inputs. I use its 20 and 80 levels to identify oversold and overbought conditions.

Those readings begin my observation process. I do not automatically buy below 20 or sell above 80.

I then compare the indicator with price. If price makes a lower low while MFI makes a higher low, that divergence can suggest weakening downside pressure. I still wait for price confirmation before considering a reversal entry.

For example, an oversold reading followed by bullish divergence becomes more relevant if price subsequently breaks a minor swing high or completes a double-bottom structure.

I avoid treating an extreme reading as proof that a trend has finished. Strong trends can maintain extreme conditions, and divergence can appear before price changes direction.

#### 4. CVD

**Cumulative Volume Delta**, or CVD, helps me assess changes in buying and selling pressure and whether those changes support price movement.

I compare its swings with price swings. If price reaches a higher high but CVD fails to confirm, I pay attention to the disagreement. If both advance together, I treat that as supporting evidence.

I also use its color for a quick bias, provided I understand what that color represents in the specific indicator. A color change alone does not confirm a trend shift.

CVD requires particular care with data. Some implementations use trade classifications; others estimate buying and selling pressure from lower-timeframe price and volume. For example, [TradingView’s Volume Delta uses intrabar data to estimate that pressure](https://www.tradingview.com/support/solutions/43000725057-volume-delta/).


I therefore interpret CVD within the limits of its feed, calculation, and reset period. Divergence is a reason to investigate the setup, not proof of who is trading or what price must do next.

### Price Action Indicators and Tools

This category includes chart-reading methods as well as calculated indicators. I group them together because they help me interpret price structure, momentum, or trend.

#### 1. Support and Resistance

Support and resistance involve judgment, so I focus on major areas rather than filling the chart with minor levels. I generally prefer volume-profile references when identifying these zones.

I treat support and resistance as areas where a reaction may occur. Price does not need to stop at an exact number for the zone to remain relevant.

My preferred entry style is a break and retest. For example, after price breaks resistance, I watch whether the retest holds and buyers respond before considering a long.

I also use major higher-timeframe zones when planning TP and SL. A nearby opposing zone can limit the available reward, even if the entry looks attractive.

I avoid forcing a setup when price cuts through a zone without a clear response or when repeated tests make its behavior difficult to interpret.

#### 2. Chart Pattern Analysis

The patterns I usually watch are head and shoulders, double bottoms, and double tops.

The shape attracts my attention, but I also want volume evidence to support the interpretation. I compare price with my selected volume tool for divergence or confirmation.

For example, the second peak of a possible double top may form with weaker volume-based momentum. That prepares a bearish idea, but I still need price to confirm the pattern through a relevant support or neckline break.

I avoid anticipating a completed pattern too early. A possible double top can become a continuation if buyers break above both peaks.

Location matters as well. A pattern near a major zone gives me more context than a similar shape in the middle of an unclear range.

#### 3. Moving Averages

I mainly use moving averages as potential profit-taking references. I also use them for pullback re-entries and to help identify the current trend or a possible trend shift.

Their usefulness depends on where price is relative to the average. If I am trading a move back toward it, the average may be an initial target. If price is already trending away from it, another price level may offer a more relevant target.

For re-entries, I watch whether a pullback toward the average holds within the existing trend.

I consider slope, price behavior around the average, and the surrounding swing structure. I avoid relying on a single crossing to declare a trend change, especially when the average is flat and price repeatedly moves through it.

#### 4. Stochastic Momentum Index

I use the **Stochastic Momentum Index**, or SMI, mainly for re-entry opportunities.

First, I identify the higher-timeframe trend. Then I look at a lower timeframe for a momentum reset that may support joining that trend again.

In an uptrend, I watch an oversold condition during a pullback and look for momentum to turn upward alongside price confirmation. In a downtrend, I apply the opposite logic.

I also watch divergence or confirmation during the pullback, while keeping the higher-timeframe direction in mind.

SMI differs from the standard stochastic oscillator, so I use levels appropriate to my SMI settings rather than automatically transferring another oscillator’s thresholds. [Its calculation measures the close relative to the midpoint of the high-low range](https://www.tradingview.com/support/solutions/43000707882-stochastic-momentum-index-smi/).

For exits, an extreme reading is additional context. Its importance depends on whether I am scalping a short move or holding an intraday trend. I avoid using the oscillator to force repeated entries against the broader structure.

#### 5. Heikin Ashi

I use Heikin Ashi to help identify the higher-timeframe trend and assess possible reversal entries.

Its smoothing can make directional movement easier to read. However, I want a reversal indication to agree with location and actual price structure.

For example, a bullish Heikin Ashi change near support becomes more relevant if actual price also breaks a nearby swing high.

I avoid using it when the market is consolidating or rotating because repeated changes can provide little directional clarity.

Heikin Ashi candles use calculated prices, so I check actual market prices for entries, stops, and targets. The displayed candle values may differ from executable prices. [TradingView explains how Heikin Ashi candles are constructed](https://www.tradingview.com/support/solutions/43000619436-understanding-heikin-ashi-charts/).

#### 6. RSI

I mainly use the **Relative Strength Index**, or RSI, to observe divergence and confirmation between price and momentum.

It helps me notice when price continues extending while its momentum appears to weaken. In my framework, however, RSI does not carry independent entry authority.

If RSI shows bearish divergence while price continues holding its uptrend structure, I remain in observation mode.

Because RSI is derived from price, I also avoid counting its agreement with another price-based indicator as a separate volume confirmation.

#### 7. Divergence and Convergence

Divergence and convergence are comparison concepts that I apply to the tools above.

Here, I use **convergence** to mean confirmation: price and the selected indicator support the same interpretation. **Divergence** means they disagree, such as price making a lower low while a volume-based indicator makes a higher low.

My preferred comparison is:

**Price action versus volume = useful preparation for a setup.**

It still needs an entry trigger.

When I describe price-based combinations such as MACD and RSI as a “wrong setup,” I mean they do not satisfy my chosen volume-plus-price framework. They may provide useful momentum information, but they do not add the separate volume perspective I want.

Even price and volume are not completely independent in every indicator. MFI, for example, includes price in its calculation. My aim is complementary information and a clear role for each tool.

## Putting the Setup Together

The following examples are hypothetical. Each uses one selected volume tool and one price-action method or indicator.

### Example 1: Volume Profile + Break-and-Retest Price Action

I draw a fixed profile over a recent upward leg and mark VAH at 100.

Price breaks above 100, then returns to test the area. I wait for the retest to hold and for a bullish response before considering an entry.

If the entry is 101, structural invalidation is 99, and a relevant overhead level is 105, the setup offers two units of potential reward per unit of risk before costs.

If the next resistance is only 102, the target may be too close. I skip rather than squeeze the stop inside the area that needs room to hold.

If price falls back into value and remains there, the breakout has failed to confirm.

### Example 2: MFI + Double-Bottom Structure

Price forms a low near support while MFI falls below 20. A second test produces a slightly lower price low, but MFI forms a higher low.

That divergence prepares the reversal idea.

I then wait for price to break the intervening swing high, with a retest if that is part of the entry approach. I assess the stop beyond the pattern’s invalidation area and the target near the next resistance.

If price keeps falling or never confirms the pattern, I do not enter simply because MFI diverged.

### Example 3: VWAP + SMI Trend Pullback

The higher-timeframe price structure shows an uptrend. Price pulls back toward the central VWAP while lower-timeframe SMI reaches its oversold area.

I watch for the VWAP area to hold, SMI to turn upward, and price to show a bullish response.

That combination supports a possible re-entry aligned with the broader trend. I assess a prior high or relevant VWAP band as a target, with the stop based on structural invalidation.

If price loses VWAP and breaks the trend’s supporting structure, an SMI upturn alone does not complete the setup.

## Final Conclusion

“Less is more” works for me when every tool has a clear responsibility.

I choose the volume tool that suits the opportunity, then pair it with a price-action tool that helps me interpret or confirm the setup. Understanding when each tool becomes unreliable is part of that choice.

A level gives me a location. Divergence gives me something to investigate. Price confirmation helps me decide whether the opportunity is ready, and the relationship between the target and invalidation determines whether the trade is practical.

My framework remains **volume + price action**. The discipline is choosing the right pair, waiting for the setup to develop, and accepting that sometimes the clearest decision is to stay out.
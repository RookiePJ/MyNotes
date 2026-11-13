# Sequential (TD Sequential)

TD Sequential is a market timing indicator developed by TD, designed to identify when a trend is becoming exhausted and may be approaching a reversal.

Unlike moving averages, MACD, or Ichimoku, TD Sequential is not primarily concerned with trend identification. Its objective is to answer a different question:

> "How far has this move progressed, and is buying or selling pressure becoming exhausted?"

The indicator became widely known after being used by hedge funds, institutional traders, and market commentators to identify potential turning points in equities, bonds, forex, and cryptocurrencies.

## Core Concept

Markets often trend longer than traders expect.

TD Sequential attempts to measure:

- Trend persistence
- Trend exhaustion
- Potential reversal zones

It does this through two phases:

1. **Setup Phase** (1-9)
2. **Countdown Phase** (1-13)

The Setup identifies a potentially exhausted trend.

The Countdown seeks additional confirmation that the trend is overextended.

## TD Setup Phase

The Setup is the most commonly used part of the indicator.

### Buy Setup

A Buy Setup occurs when:

$$
\text{Close}_t < \text{Close}_{t-4}
$$

for nine consecutive bars.

Each qualifying candle receives a count: 1, 2, 3, 4, 5, 6, 7, 8, 9.

The completion of "9" suggests the downtrend may be nearing exhaustion.

**Example**

| Bar | Close |
|-----|-------|
| 1   | 100   |
| 5   | 95    |
| 6   | 92    |
| 7   | 90    |
| 8   | 87    |
| 9   | 85    |

Each close remains below the close four bars earlier.

Eventually a **Buy Setup 9** appears.

This does not guarantee an immediate rally.

It highlights a location where sellers may be exhausted.

### Sell Setup

The opposite condition:

$$
\text{Close}_t > \text{Close}_{t-4}
$$

for nine consecutive bars.

**Example**

| Bar | Close |
|-----|-------|
| 1   | 100   |
| 5   | 105   |
| 6   | 108   |
| 7   | 110   |
| 8   | 113   |
| 9   | 116   |

Produces a **Sell Setup 9**: a warning that buying pressure may be becoming exhausted.

### Why Compare to Four Bars Earlier?

DeMark viewed four bars as sufficient to smooth short-term noise while still capturing trend persistence.

Instead of asking:

> Is today's close higher than yesterday?

it asks:

> Is today's close higher than four bars ago?

This measures sustained trend behaviour.

### Setup Perfection

Not all 9s are equal.

A completed Setup often requires Perfection.

**Buy Setup Perfection**

Typically:

$$
\min(\text{Low}_8, \text{Low}_9) < \min(\text{Low}_6, \text{Low}_7)
$$

This demonstrates a genuine washout.

**Sell Setup Perfection**

Typically:

$$
\max(\text{High}_8, \text{High}_9) > \max(\text{High}_6, \text{High}_7)
$$

This indicates a final buying climax.

Many traders place greater emphasis on perfected setups.

## Countdown Phase

After Setup 9 completes, the Countdown begins.

This is the part many charting packages display as 10, 11, 12, 13, or separately as 1, 2, 3, ..., 13, depending on implementation.

### Buy Countdown

A Buy Countdown occurs when:

$$
\text{Close}_t \le \text{Low}_{t-2}
$$

Thirteen qualifying occurrences must appear.

Importantly:

- They do not need to be consecutive.
- The count can take weeks or months to complete.

When 13 appears (**Buy Countdown 13**), the market is considered significantly oversold.

### Sell Countdown

The opposite:

$$
\text{Close}_t \ge \text{High}_{t-2}
$$

for thirteen qualifying bars.

When Count 13 appears (**Sell Countdown 13**), the market is considered significantly overbought.

## Practical Example: Market Top

Imagine a strong rally.

**Stage 1**

Price rises steadily: 100, 104, 108, 112, 115, 118.

Eventually **Sell Setup 9** appears.

Many traders begin watching closely.

**Stage 2**

The rally continues.

This is important because many 9s fail.

Price: 118, 120, 122, 125, 127.

Countdown progresses: 10, 11, 12, 13.

**Stage 3**

**Sell Countdown 13** appears.

Shortly afterwards: 127, 123, 119, 112.

The market reverses.

The 13 did not predict the exact top but identified an area of exhaustion.

## Practical Example: Market Bottom

Consider a panic selloff: 100, 95, 90, 85, 80, 75, 70.

**Buy Setup 9** appears.

Fear remains high.

The decline continues: 68, 65, 63, 61, 60.

Eventually **Buy Countdown 13** forms.

A rally follows: 60, 65, 72, 80, 90.

The 13 highlights seller exhaustion.

## Interpreting Signals

### Weakest Signal

Setup 9 alone (Sell 9 or Buy 9).

Useful, but often early.

### Stronger Signal

Setup 9 + Perfection.

Example: Sell 9 + Perfected High.

Suggests climax behaviour.

### Strongest Signal

Setup 9 plus Countdown 13.

This combination is generally viewed as the highest-confidence TD signal.

## Relationship to Other Indicators

### Compared with MACD

| TD Sequential                | MACD                         |
|------------------------------|------------------------------|
| Exhaustion tool              | Momentum tool                |
| Finds turning points         | Finds trend acceleration     |
| Can signal against trend     | Usually trend-following      |
| Often early                  | Often late                   |

A Sell 13 may appear while MACD remains strongly bullish.

### Compared with Golden Cross

| TD Sequential                | Golden Cross                 |
|------------------------------|------------------------------|
| Mean reversion               | Trend following              |
| Looks for exhaustion         | Looks for confirmation       |
| Can identify tops            | Usually misses tops          |
| Early                        | Late                         |

Many traders use both.

Example:

- Golden Cross identifies the bull market.
- TD Sequential identifies pullbacks and local peaks within that bull market.

### Compared with Ichimoku

Ichimoku answers:

> What is the trend?

TD Sequential answers:

> How mature is the trend?

They complement one another well.

## Strengths

### 1. Excellent at Finding Exhaustion

This is its greatest strength.

Many indicators become more bullish as a move extends.

TD Sequential becomes more cautious.

Example:

- RSI = 75
- MACD rising
- Price making new highs

While **Sell Countdown 13** warns the move may be nearing completion.

### 2. Works Across Markets

TD Sequential is commonly used on:

- S&P 500
- Nasdaq
- FTSE 100
- Treasury Bonds
- Gold
- Crude Oil
- EUR/USD
- Bitcoin

Because it focuses on market structure rather than fundamentals.

### 3. Useful at Major Turning Points

Some of the most famous applications involve:

- Equity market lows
- Commodity peaks
- Cryptocurrency cycle tops and bottoms

where prolonged trends eventually become exhausted.

### 4. Objective Rules

The counting process is mechanical.

Either a bar qualifies or it doesn't.

This reduces discretionary interpretation.

## Weaknesses

### 1. Can Be Very Early

This is the biggest criticism.

A market can continue trending long after a Setup 9 appears.

Example: after a **Sell Setup 9**, price continues climbing another 15%.

The signal was directionally correct but poorly timed.

### 2. Strong Trends Can Ignore It

During powerful bull markets:

- AI boom stocks
- Commodity supercycles
- Momentum-driven rallies

multiple Sell 9s may occur before the final peak.

This leads traders to short too early.

### 3. Complex Rules

Unlike MACD or moving averages, TD Sequential contains:

- Setup counts
- Countdown counts
- Perfection criteria
- Recycling rules
- Cancellation rules

Many traders only understand part of the methodology.

### 4. Poor as a Standalone System

A Sell 13 does not necessarily mean **SELL NOW**, and a Buy 13 does not necessarily mean **BUY NOW**.

Without trend, volume, support/resistance, or risk management context, false signals occur frequently.

### 5. Different Implementations Exist

Different charting platforms sometimes implement:

- Setup counting
- Countdown counting
- Recycling logic

slightly differently.

This can lead to discrepancies between charts.

## How Many Professional Traders Use It

A common institutional workflow might be:

1. **Trend Filter**: price above 200-day moving average; price above Ichimoku cloud.
2. **Momentum Filter**: MACD positive.
3. **Exhaustion Filter**: TD Sell 9 or TD Sell 13.

Rather than shorting immediately, traders may:

- Tighten stops
- Reduce position size
- Take partial profits

Likewise, during a bear market:

- Price below 200-day average
- MACD negative
- TD Buy 13 appears

A trader may begin looking for a reversal rather than blindly continuing to sell.

## Bottom Line

TD Sequential is best viewed as an exhaustion indicator, not a trend indicator.

If:

- Ichimoku tells you the market structure,
- MACD tells you the momentum,
- 20/200 moving averages tell you the long-term trend,

then TD Sequential tells you how mature that trend has become and whether it may be running out of fuel.

Its biggest strength is spotting potential turning points before traditional indicators react. Its biggest weakness is that markets can remain overbought or oversold for much longer than the countdown suggests, making it most effective when combined with trend and momentum analysis rather than used on its own.

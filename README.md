# Stop Grabber Pattern MT5

**Developer's Site:** [forexroboteasy.com](https://forexroboteasy.com)

**Development by:** Forex Robot Easy Team

---

## Description

Stop Grabber Pattern MT5 is a custom indicator and trading system that identifies buy and sell signals based on the stop grabber pattern. The stop grabber pattern is a technical analysis pattern that indicates potential reversals in the market.

The indicator calculates two Exponential Moving Averages (EMAs) - a fast EMA and a slow EMA. When the fast EMA crosses above the slow EMA and the low of the current bar is lower than the low of the previous bar, a buy signal is generated. Conversely, when the fast EMA crosses below the slow EMA and the high of the current bar is higher than the high of the previous bar, a sell signal is generated.

The trading system places market orders at the close of the signal bar and sets stop loss and take profit levels based on the swing highs and lows.

Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample and may not reflect the exact functionality of the official product. For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/review-stop-grabber-pattern-mt5-a-reliable-forex-software-for-professional-traders/).

---

## External Parameters

- `Fast_EMA`: Fast EMA parameter (default: 9)
- `Slow_EMA`: Slow EMA parameter (default: 21)

---

## Global Variables

- `signalBar`: Signal bar index
- `buySignal`: Buy signal flag
- `sellSignal`: Sell signal flag

---

## Functions

### `OnInit()`

This function is called when the indicator is initialized. It initializes the global variables.

### `CustomIndicator()`

This function calculates the EMA values and checks for buy and sell signals based on the stop grabber pattern. If a buy signal is detected, the `buySignal` flag is set to true and the `sellSignal` flag is set to false. If a sell signal is detected, the `buySignal` flag is set to false and the `sellSignal` flag is set to true.

### `GenerateSignals()`

This function calls the `CustomIndicator()` function to generate signals based on the stop grabber pattern. If a buy signal is generated, a market buy order is placed at the close of the signal bar. The stop loss is set at the low of the signal bar, and the take profit target is set at the first swing high. If a sell signal is generated, a market sell order is placed at the close of the signal bar. The stop loss is set at the high of the signal bar, and the take profit target is set at the first swing low.

### `OnTick()`

This function is called on every tick. It updates the `signalBar` index and generates signals using the `GenerateSignals()` function.

---

For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/review-stop-grabber-pattern-mt5-a-reliable-forex-software-for-professional-traders/). ForexRobotEasy is not the official developer of this product.

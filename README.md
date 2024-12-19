# Martingale Trading Strategy with Random Signals

This project implements a Martingale trading strategy using random signals on the EUR/USD forex pair. The Martingale strategy is a high-risk trading approach that involves doubling the stake after each loss to recover previous losses and make a profit.

## Overview
![bokeh_plot](https://github.com/user-attachments/assets/343e5ba0-d3c4-44af-8f64-87275c9cd45d)

The code:
- Generates random buy/sell signals for EUR/USD.
- Executes trades based on the Martingale strategy.
- Tracks profit/loss after each trade.

**Disclaimer:** This code is for educational purposes only. Trading with real money is risky, and the Martingale strategy carries significant risks. Always trade responsibly.

## What is the Martingale Strategy?

The Martingale strategy is based on the idea of doubling your trade size after each loss. When a winning trade occurs, the profits offset all previous losses and result in a net gain equal to the initial trade size.

### Example of the Martingale Strategy

1. **Initial Trade:** Buy 1 lot of EUR/USD and lose $10.
2. **Second Trade:** Double the position to 2 lots. If you lose again, the total loss is $30 ($10 from the first trade + $20 from the second trade).
3. **Third Trade:** Double the position again to 4 lots. If this trade wins, it covers all losses and adds a profit equal to the initial stake.

#### Calculation:
- Trade 1: -$10
- Trade 2: -$20
- Trade 3: +$40
- **Net Profit:** $10

The key idea is to win enough to recover all losses and gain a profit equal to the initial stake.

## Project Files

- `martingale_trading.ipynb`: The main Jupyter Notebook implementing the Martingale strategy.
- `README.md`: Documentation for the project.

## Prerequisites

- Python 3.7 or higher
- Libraries:
  - `pandas` (for data manipulation)
  - `matplotlib` (optional, for visualization)
  
Install the required libraries using:
```bash
pip install pandas matplotlib
```

## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/martingale-trading.git
   cd martingale-trading
   ```

2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook martingale_trading.ipynb
   ```

3. Modify parameters in the notebook, such as the initial trade size, account balance, and number of iterations.

## Parameters

- **`initial_trade_size`**: The size of the first trade (e.g., 1 lot).
- **`max_iterations`**: The maximum number of trades to execute.
- **`account_balance`**: Starting balance for the trading simulation.
- **`initial_value`**: The starting value for the trading simulation (default set to 1000).
- **`stop_loss`**: Stop-loss level for trades (default set to 300e-4).
- **`take_profit`**: Take-profit level for trades (default set to 300e-4).

## Example Output

```
Trade 1: Signal = Buy, Result = Loss, Balance = $990
Trade 2: Signal = Sell, Result = Loss, Balance = $970
Trade 3: Signal = Buy, Result = Win, Balance = $1010
...
Final Balance: $1020
Return [%]: 0.034184
Buy & Hold Return [%]: -11.93986
```

## Risks of the Martingale Strategy

1. **High Risk:** A series of losses can lead to significant drawdowns.
2. **Account Wipeout:** Doubling trade sizes after losses can quickly deplete account balances.
3. **Market Constraints:** Trading limits and margin requirements can restrict strategy implementation.

## Recommendations

- Use this strategy in simulations only.
- Combine Martingale with robust risk management techniques.
- Avoid using it with real money unless you fully understand the risks.


---

**Note:** For additional help or suggestions, feel free to open an issue in this repository.

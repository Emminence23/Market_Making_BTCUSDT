## Market Making Simulator

This project implements a basic market-making strategy on order book data. It is structured as a Python notebook and designed to simulate quoting, execution, and inventory management in a high-frequency trading environment. The simulator aims to help understand and evaluate simple market-making behaviors under realistic market conditions.

The historical order book data used in this project was downloaded and formatted following the method described in [this article by Lu Battistoni](https://medium.com/@lu.battistoni/how-to-download-and-format-free-historical-order-book-dataset-16b3a84a8e0e).

### Included Notebooks
- **`Market_Making_final.ipynb`**  
  Contains the **base version** of the simulator. Quotes are placed deterministically at spread-adjusted prices, and fills are assumed to happen immediately when a price match occurs. Useful for understanding core logic: quoting, execution, inventory management, and mark-to-market PnL tracking.

- **`Realistic.ipynb`**  
  Extends the base simulator with two realism enhancements:
  - **Execution Probability:** Not all limit orders are assumed to be filled. Each order has a probabilistic chance of execution, simulating queue position and competition.
  - **Gaussian Slippage:** When trades are executed, the price is adjusted with a small random noise to reflect market slippage and non-instant execution.
  
  As expected, this leads to more volatile PnL outcomes, and emphasizes the risk of non-execution and price impact. 

### Credits

:star: [Emminence23](https://github.com/Emminence23)

:star: [khushi-2653](https://github.com/khushi-2653)
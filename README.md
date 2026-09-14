## Cash-to-Futures Basis Convergence with Rolling SOFR Funding

This model revisits the **Cash-to-Futures Treasury Basis Convergence Trade**, with a focus on how the *path of funding rates* affects total return.

Rather than treating financing as a single rate observed at the beginning or end of the trade, the model assumes the trader continuously refinances the cash Treasury position by **rolling 5-day Term SOFR funding across a 90-day investment horizon**.

To isolate the effect of the funding curve, the model holds three major components constant:

* **90-day investment horizon**
* **CTD Treasury yield**
* **ZN futures hedging cost**

The primary variable is therefore the sequence of **5-day SOFR funding rates** encountered as the position is rolled.

Each 5-day period is treated as an individual funding interval. The return generated over each interval is calculated using **Euler's continuous compounding formula**, and the resulting period returns are aggregated to estimate the total return of the basis position across the full 90-day horizon.

The purpose of the model is to demonstrate that a carry trade cannot necessarily be understood from the funding rate at maturity—or even from a single initial funding rate. Two trades with identical CTD yields, futures hedge costs, and terminal 90-day SOFR rates can produce materially different realized returns if the **shape and path of the funding curve** differ during the holding period.

In other words, the profitability of a Treasury cash-to-futures convergence trade depends not only on where funding ultimately settles, but on **how funding evolves while the position is being financed**.

This creates multiple possible paths to profit or loss even when the trade's headline yield, hedge cost, and terminal funding assumptions remain unchanged.

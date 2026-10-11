# Monte Carlo Engine -- Probability & Simulation

## Objective
I used Monte Carlo simulation to answer four probability questions by drawing many random cases and counting the results.

## Methodology
- Set up one seeded NumPy random number generator (seed 42) so every result can be reproduced.
- Simulated 10,000 fair coin flips and plotted the running share of heads on a log scale to watch the Law of Large Numbers at work.
- Simulated 10,000 Monty Hall games under two strategies, always stay and always switch, and compared the win rates with the theoretical 1/3 and 2/3.
- Applied Bayes' Theorem to a disease screening test (prevalence 1%, sensitivity 95%, specificity 90%), then checked the formula by simulating 100,000 people and counting true and false positives.
- Simulated 10,000 daily portfolio returns from a Normal distribution and computed the 95% and 99% Value at Risk and Expected Shortfall for a $1M portfolio.
- Estimated pi by dropping random points in a unit square at several sample sizes, and checked on a log-log plot that the error shrinks like 1/sqrt(n).
- Asked an AI to write a VaR/ES function, revised the prompt to state the method and conventions myself, and checked its output against my own numbers.

## Key Findings
- **Monty Hall:** Switching won 6,694 of 10,000 games, about two in three, so switching doubles the chance of winning.
- **Disease screening:** Only 9.2% of positive tests came from people who were actually sick. Because the disease is rare, false alarms from the healthy majority far outnumber true positives.
- **Value at Risk:** The 95% VaR was $19,494 and the 95% ES was $24,230. On the worst 5% of days, the average loss is larger than the VaR threshold, which is why ES gives a fuller picture of tail risk.
- **Monte Carlo error:** The error in the pi estimate shrank like 1/sqrt(n), so more accuracy costs many more draws.

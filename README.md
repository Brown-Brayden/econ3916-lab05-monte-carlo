# econ3916-lab05-monte-carlo
# Monte Carlo Engine -- Probability & Simulation

## Objective
I used Monte Carlo simulation in NumPy to see how random sampling answers
questions about probability, medical screening, and financial risk.

## Methodology
- Simulated 10,000 fair coin flips and plotted the running share of heads
  to watch the Law of Large Numbers at work.
- Simulated 10,000 Monty Hall games and compared the win rate for always
  staying with the win rate for always switching.
- Worked out the chance that a positive test means disease using Bayes'
  Theorem, then simulated the same screening test on 100,000 people
  (prevalence 1%, sensitivity 95%, specificity 90%) to check it.
- Simulated daily returns for a $1M portfolio and computed the 95% Value
  at Risk and Expected Shortfall from the simulated returns.
- Estimated pi by dropping random points in a unit square, at several
  sample sizes, and checked that the error shrinks like 1/sqrt(n).
- Asked an AI to write a VaR and Expected Shortfall function, revised the
  prompt once, and checked its output against my own numbers.

## Key Findings
- Switching won 6,694 of 10,000 Monty Hall games, about two in three.
  The host's choice of door carries information, so the two closed doors
  are not 50/50.
- Only 9.2% of people who tested positive were actually sick. When a
  disease is rare, false alarms from the large healthy group outnumber
  the true positives, even with a 95% sensitive test.
- On the $1M portfolio, the 95% VaR was $19,494 and the 95% ES was
  $24,230. VaR marks where the worst 5% of days begin; ES is the average
  loss on those days, which is why it is larger.
- The error in my pi estimates fell in line with 1/sqrt(n), so each extra
  digit of accuracy costs far more simulation than the last.

This project implements my solution to the Spring 2025 GRA 65131 Financial Risk Management assignment. 

The brief: 

Model monthly prices/utilization for EU power projects (natural gas, coal, wind) and evaluate five financing mixes for a €200 m, 5-year zero-coupon bond targeting 12%—including cash-flow simulations, default testing, optimal face-value calibration, and the value of a derivative that floors monthly cash flows at zero. 

My approach (code-driven): 

I bootstrap historical monthly returns (2011–2025) and couple series with a t-copula to capture joint tail risk; run 10,000 Monte-Carlo paths over 60 months; apply light winsorization and logical bounds (e.g., utilization in [0, 100]%) ; roll operating cash flows; compound retained cash at 2% risk-free; solve for bond face values via numerical optimization; and price the “no-negative-cash-flow” protection as the expected shortfall of negative months. Results and plots are summarized in the report—see the Recommendation panel on page 1 and the default-probability bar chart on page 7. 

Key results (from the report, reproduced by the code):
Recommended allocation: 65% Wind / 35% Coal (balances low default risk with return; see p. 1). 

Default frequencies (illustrative): Wind lowest (~3.9%); Natural Gas highest (~27%); Equal-weight across all three materially worse than Wind/Coal blends (see p. 7–8). 

Optimized bond face values (targeting 12% expected return): Wind ≈ €353.9m, Coal ≈ €358.4m, Equal-weight ≈ €367.9m, Natural Gas ≈ €432.5m (tables p. 1 & p. 9–10). 

Derivative that floors monthly cash flows: negligible for Wind, ≈€1.5m for Coal, ≈€33.6m for Natural Gas (table p. 10). 

Visuals referenced: forecast fans for prices/utilization (p. 4), projected monthly cash-flow bands (p. 6), retained-cash distributions (p. 7 & p. 11). 

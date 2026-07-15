This repository contains my solution to the Spring 2025 GRA 65131 Financial Risk Management assignment.

The project examines how different European energy investments perform under uncertain prices, production levels and financing conditions. The goal was to compare five investment strategies and determine which offered the strongest balance between return and default risk.

Running the project

Download DataPost.xlsx, update the file path inside FinRisk M1.ipynb, and run the notebook from the beginning.

What I did

I used monthly European energy data from 2011 to 2025 to model how electricity prices, fuel costs, carbon prices and generation levels move together.

The model then:

Simulates 10,000 possible market outcomes over five years.
Converts simulated prices and utilization levels into monthly project cash flows.
Compares five investment strategies across wind, coal and natural gas.
Estimates default probabilities and potential losses.
Calculates the bond face value required to deliver a 12% expected annual return.
Estimates the cost of protection against negative monthly cash flows.

Extreme simulated values are limited where necessary, while utilization rates are kept between 0% and 100%. The complete results and visualizations are presented in the accompanying report.

Main findings
Recommended allocation: 65% wind and 35% coal, offering a stronger balance between expected return and default risk.
Default risk: Wind had the lowest estimated default frequency at approximately 3.9%, while natural gas had the highest at approximately 27%.
Required bond face value: Approximately €353.9 million for wind, €358.4 million for coal, €367.9 million for the equal-weight strategy and €432.5 million for natural gas.
Cost of cash-flow protection: Negligible for wind, approximately €1.5 million for coal and €33.6 million for natural gas.

The report also includes five-year price and utilization forecasts, projected cash-flow ranges, default-risk comparisons and retained-cash distributions.

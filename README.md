# Portfolio-Optimization
Prescriptive Analytic project
Apex Capital Advisors needs a scalable, auditable approach to portfolio construction that serves clients with fundamentally different risk profiles, ethical preferences, and regulatory requirements — without requiring advisors to manually tune each allocation. This report presents a quantitative framework that delivers exactly that: a single pipeline that takes each client's profile as input and produces a fully compliant, individually optimized portfolio as output


# Project Overview 
This project develops a portfolio optimization framework for 15 clients with varying risk tolerances, ESG preferences, and regulatory account types. The framework progresses through four formulations of increasing complexity — LP, QP, Goal Programming, and MIP — fulfilling all 10 deliverable tasks specified in the project guide. Python (cvxpy, scipy, pandas, NumPy) is used throughout; Gurobi is used as the MIP solver.



# My Role 
Built a tool to recommend investment portfolios for 15 clients of a mock wealth management firm. Each client had a different risk tolerance, ESG preference and account type. Every portfolio also had to follow hard rules, like a cap on how much could go into any single investment, so no client could put more than 20% into one stock. I built four optimization models, and the choice of model depended on which rules we had to handle:

•	Started with a simple model that just maximized return. It gave almost everyone the same portfolio, which showed that ignoring risk doesn't work in practice.
•	Adding each client's risk tolerance as a limit required a model that balances return against risk. Now every client got a portfolio that fit them. 
•	When clients had competing targets, like return versus ESG, I used goal programming to show how close we could get to each one. 
•	When rules required whole numbers, like buying bonds in fixed amounts, I used an integer model so the portfolio could be executed.
The most interesting finding was about aggressive clients. We expected risk tolerance to drive the differences between clients, and it did for conservative ones. But past a certain point, giving aggressive clients more risk tolerance didn't raise their returns at all. They'd already hit the cap in every high-return investment. So, the hard rule we started with, not their risk appetite, turned out to be the real bottleneck.
<img width="468" height="336" alt="image" src="https://github.com/user-attachments/assets/a27193e7-b2ec-4822-bf59-2fb1a29bcb1d" />

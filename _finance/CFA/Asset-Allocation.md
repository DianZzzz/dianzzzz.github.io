---
layout: blog
topic: CFA Level III
title: Asset Allocation
tags: cfa finance
comments: true
date: 2022-06-17
---
# Asset Allocation

<!-- MDTOC maxdepth:6 firsth1:0 numbering:0 flatten:0 bullets:1 updateOnSave:1 -->

- [Asset Risks](#asset-risks)
  - [Three Super-Classes of Risks](#three-super-classes-of-risks)
  - [VaR](#var)
    - [Advantages of VaR](#advantages-of-var)
    - [Disadvantages of VaR](#disadvantages-of-var)
  - [Optimal Choice Between One Risky Asset and Risk Free Asset](#optimal-choice-between-one-risky-asset-and-risk-free-asset)
  - [Risk Budgeting](#risk-budgeting)
- [Implementation Choices](#implementation-choices)
- [Approaches to Asset Allocation](#approaches-to-asset-allocation)
  - [Mean Variance Optimization](#mean-variance-optimization)
    - [Utility Function](#utility-function)
    - [Risk of MVO Portfolio Combined with RF Asset](#risk-of-mvo-portfolio-combined-with-rf-asset)
    - [Criticism of MVO](#criticism-of-mvo)
    - [Alternative Models](#alternative-models)
      - [Criticisms of resampling](#criticisms-of-resampling)
  - [Surplus Optimization](#surplus-optimization)
  - [Hedging/Return-Seeking Portfolio Approach](#hedgingreturn-seeking-portfolio-approach)
  - [Integrated Asset-Liability Approach](#integrated-asset-liability-approach)
  - [Risk Parity](#risk-parity)
- [Tax Consideration](#tax-consideration)
- [Strategies to Overcome Behavior Biases in Asset Allocation](#strategies-to-overcome-behavior-biases-in-asset-allocation)
  - [Loss Aversion](#loss-aversion)
  - [Illusion of Control](#illusion-of-control)
  - [Mental Accounting](#mental-accounting)
  - [Representativeness Bias](#representativeness-bias)
  - [Framing Bias](#framing-bias)
  - [Availability Bias](#availability-bias)
- [Optimal Width of Corridor](#optimal-width-of-corridor)
- [Illiquidity Premium](#illiquidity-premium)

<!-- /MDTOC -->
## Asset Risks

### Three Super-Classes of Risks
- Capital Assets
- Consumable/transformable Assets
- Store of Value of Assets

### VaR

A 100 million portfolio has a 1.37% VaR at the 5% probability over one week means that over one week, the portfolio could lose 1.37% of 100 million or 1.37 million. There is a 5% chance that more than this will be lost and a 95% chance that less than this will be lost.

#### Advantages of VaR
- It has become the industry standard for risk measurement and is required by many regulators.
- It aggregates all risk into one single, easy to understand number.
- It can be used in capital allocation.

#### Disadvantages of VaR
- Some of the methods (Monte Carlo) are difficult and expensive.
- The different computation methods can generate different estimates of VaR.
- It can generate a false sense of security. It is only as good as the inputs and estimation process. Even when done correctly it is probabilistic; things can always be worse.
- It is one-sided, focusing on the left tail in the return distribution, and ignores any upside potential.

### Optimal Choice Between One Risky Asset and Risk Free Asset
w* =1/λ * (μ−r_f/σ^2)
λ: investor's risk aversion


### Risk Budgeting
- Objective: specifies the total amount of risk and how much of risk should be budgeted for each asset class
- Marginal Contribution to Total Risk (MCTR) = beta * portfolio volatility
- Absolute Contribution to Total Risk (ACTR) = weight * MCTR
- An optimal asset allocation is when the ratio of excess return to MCTR is the same for all assets and matches the Sharpe ratio of the tangency portfolio


## Implementation Choices
- Whether to allow deviations from the strategic allocation
  - `Tactical asset allocation`: deliberation short term deviation from the strategic asset allocation
  - `Dynamic asset allocation`: deliberation long term deviation from the strategic asset allocation
- Invest along the active/passive spectrum

## Approaches to Asset Allocation

- Asset-only
  - Mean variance optimization
- Liability-relative
  - Surplus optimization
  - Hedging/Return-Seeking Portfolio Approach
- Goals-based

### Mean Variance Optimization

#### Utility Function

U = E(R) - 0.005 * λ * σ^2 where λ = the investor’s risk aversion coefficient

#### Risk of MVO Portfolio Combined with RF Asset

Risk of MVO portfolio combined with rf asset = risky asset standard deviation * (1 - rf asset weight)


#### Criticism of MVO
- Outputs are highly sensitive to small changes in inputs; typically more sensitive to expected return estimates than estimates of volatilities and correlations.
- Investors are concerned more than just mean and variance of return
- Does not take into account of trading costs and taxes
- Efficient portfolios are highly concentrated in a subset of the available asset classes

#### Alternative Models
- Reverse MVO: can be used to estimate expected returns for use in a forward-looking optimization
- Black-Litterman Model: enables investors to combine their unique forecasts of expected returns with reverse-optimized returns in an elegant manner.
- Constrained asset class weights
- Resampled MVO = MVO + Monte Carlo Simulation

##### Criticisms of resampling

- Some frontiers have concave “bumps” where expected return decreases as expected risk increases
- The “riskier” asset allocations are over-diversified
- The asset allocations inherit the estimation errors in the original inputs
- The approach lacks a foundation in theory


### Surplus Optimization

Use MVO to determine an efficient frontier based on the surplus with its volatility as measure of risk

U = E(R) - 0.005 * λ * σ^2
where
E(R) = surplus return = (Δ in asset value - Δ in liability value) / Initial asset value
σ^2 = variance of surplus return


### Hedging/Return-Seeking Portfolio Approach
- Assumes both linear and nonlinear correlation between assets and liabilities
- Requires positive funded ratio
- Single period model

### Integrated Asset-Liability Approach

- Assumes both linear and nonlinear correlation between assets and liabilities
- Can apply to any funded ratio
- Multi period model

### Risk Parity

- Each asset (asset class or risk factor) should contribute equally to the total risk of the portfolio
- weight × Cov(ri,rP) = 1/n * σ^2

## Tax Consideration

- after-tax standard deviation = pre-tax standard deviation * (1-t)
- Tax Advantage Retirement Account = Investment grade bonds, high yield bond, dividend income stock, total return (capital gain) stock

## Strategies to Overcome Behavior Biases in Asset Allocation

### Loss Aversion
- Frame risk in terms of shortfall probability
- Fund high-priority goals with low risk assets

### Illusion of Control
- Use global market portfolio as the starting point in developing asset allocation
- A formal asset allocation process that employs long-term return and risk forecasts, optimization constraints anchored around asset class weights in the global market portfolio, and strict policy ranges

### Mental Accounting
- Goals-based investing by aligning each goal with a discrete sub-portfolio, and the investor can specify the acceptable level of risk for each goal.
- Assign the concentrated stock position to an aspirational goal—one that the client would like to achieve but to which he or she is willing to assign a lower probability of success.

### Representativeness Bias
- A formal asset allocation policy with pre-specified allowable ranges
- A strong governance framework with the appropriate level of expertise and well-documented investment beliefs

### Framing Bias
- Use alternative risk measurement such as VaR and Conditional VaR
  - VaR: the minimum loss that would be expected a certain percentage of the time over a certain period of time given the assumed market conditions.
  - CVaR: the probability-weighted average of losses when the VaR threshold is breached.
  - Shortfall Proability
- Present the possible asset allocation choices with multiple perspectives on the risk/reward trade-off.

### Availability Bias
- A formal asset allocation process using the global market portfolio as the starting point for asset allocation modeling
- A strong governance framework with the appropriate level of expertise and well-documented investment beliefs

## Optimal Width of Corridor

| Factor | Effect on Optimal Width of Corridor |
|:-------------|:------------------|
|Transaction costs | The higher the transaction costs, the wider the optimal corridor.	High transaction costs set a high hurdle for rebalancing benefits to overcome.
|Risk tolerance	| The higher the risk tolerance, the wider the optimal corridor.	Higher risk tolerance means less sensitivity to divergences from the target allocation.
| Correlation with the rest of the portfolio	| The higher the correlation, the wider the optimal corridor.	When asset classes move in sync, further divergence from target weights is less likely.
| Volatility of the asset class	| The higher the volatility, the wider the optimal corridor.
| Volatility of the rest of the portfolio	| The higher the volatility, the narrower the optimal corridor.	Higher volatility makes large divergences from the strategic asset allocation more likely.

## Illiquidity Premium

- Expected compensation for the additional risk of tying up capital for a potentially uncertain time period.
- Illiquidity premium equals the value of a put option with an exercise price equal to the hypothetical “marketable price” of the illiquid asset as estimated at the time of purchase.

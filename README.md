# mindmap

```mermaid

mindmap
  root((Black-Scholes Theorem))
    Core Idea
      "Goal: Price European option with no arbitrage"
      "Formula: C = S*N(d1) - K*exp(-r*(T-t))*N(d2)"
      "Put via Put-Call Parity"
    Foundations
      "Stock follows dS = mu*S*dt + sigma*S*dW"
      "No arbitrage, frictionless market"
      "Constant r, sigma, continuous trading"
      "Instruments: Stock S_t and Bond B_t = exp(r*t)"
    Building Blocks
      "Replicating Portfolio: Option = Delta*S + Bond"
      "Self-Financing: dV = Delta*dS + r*(B - Delta*S)*dt"
      "No-Arbitrage => Black-Scholes PDE"
    PDE Solution
      "Boundary: V(S,T) = max(S-K,0)"
      "d1 = [ln(S0/K)+(r+0.5*sigma^2)*T]/(sigma*sqrt(T))"
      "d2 = d1 - sigma*sqrt(T)"
      "Call = S0*N(d1) - K*exp(-r*T)*N(d2)"
      "Put  = K*exp(-r*T)*N(-d2) - S0*N(-d1)"
    Outputs
      "Option values, Greeks (Delta, Gamma, Theta, Vega, Rho)"
    Interpretations
      "Delta hedging and risk-neutral valuation"
      "Volatility drives time value"
      "Basis of modern derivatives pricing"
    Extensions
      "Dividends: S0*exp(-q*T)"
      "American options: free-boundary models"
      "Stochastic volatility (Heston)"
      "Jump diffusion (Merton)"
      "Binomial model: discrete-time limit"




```

# mindmap

```mermaid

flowchart TD
    %% --- Define All Nodes ---
    A["Black–Scholes Theorem"]

    B1["1️⃣ Core Idea"]
        B1a["Fair price of European option (no arbitrage)"]
        B1b["C = S*N(d₁) − K·e^(−r(T−t))·N(d₂)"]
        B1c["Put via Put–Call Parity"]

    B2["2️⃣ Foundations"]
        B2a["GBM: dS = μSdt + σSdW"]
        B2b["Assumptions: no arbitrage, frictionless, const r, σ"]
        B2c["Instruments: Stock Sₜ, Bond Bₜ = e^(r·t)"]

    B3["3️⃣ Building Blocks"]
        B3a["Replicating Portfolio: Option = ΔS + B"]
        B3b["Self-financing: dV = Δ·dS + r(B − ΔS)dt"]
        B3c["No-Arbitrage ⇒ Black–Scholes PDE"]

    B4["4️⃣ PDE Solution"]
        B4a["Boundary: V(S,T)=max(S−K,0)"]
        B4b["d₁ = [ln(S₀/K)+(r+½σ²)T]/(σ√T)"]
        B4c["d₂ = d₁ − σ√T"]
        B4d["Call = S₀N(d₁) − K·e^(−rT)·N(d₂)"]
        B4e["Put  = K·e^(−rT)·N(−d₂) − S₀N(−d₁)"]

    B5["5️⃣ Outputs"]
        B5a["Option values & Greeks (Δ, Γ, Θ, Vega, ρ)"]

    B6["6️⃣ Interpretations"]
        B6a["Delta hedging = continuous risk elimination"]
        B6b["Risk-neutral valuation replaces μ with r"]
        B6c["Volatility drives time value"]

    B7["7️⃣ Extensions"]
        B7a["Dividends: use S₀·e^(−qT)"]
        B7b["American options: free-boundary"]
        B7c["Stochastic volatility (Heston)"]
        B7d["Jump diffusion (Merton)"]
        B7e["Binomial model: discrete-time limit"]

    %% --- Define Flow Structure ---
    
    %% Main Vertical Spine
    A --> B1 --> B2 --> B3 --> B4 --> B5 --> B6 --> B7

    %% Branches from Spine
    B1 --> B1a
    B1 --> B1b
    B1 --> B1c

    B2 --> B2a
    B2 --> B2b
    B2 --> B2c

    B3 --> B3a
    B3 --> B3b
    B3 --> B3c

    B4 --> B4a
    B4 --> B4b
    B4 --> B4c
    B4 --> B4d
    B4 --> B4e

    B5 --> B5a

    B6 --> B6a
    B6 --> B6b
    B6 --> B6c

    B7 --> B7a
    B7 --> B7b
    B7 --> B7c
    B7 --> B7d
    B7 --> B7e



```

---

```
Black–Scholes Theorem
├── 1️⃣ Core Idea
│   ├── Fair price of European option (no arbitrage)
│   ├── C = S*N(d₁) − K·e^(−r(T−t))·N(d₂)
│   └── Put via Put–Call Parity
├── 2️⃣ Foundations
│   ├── GBM: dS = μSdt + σSdW
│   ├── Assumptions: no arbitrage, frictionless, const r, σ
│   └── Instruments: Stock Sₜ, Bond Bₜ = e^(r·t)
├── 3️⃣ Building Blocks
│   ├── Replicating Portfolio: Option = ΔS + B
│   ├── Self-financing: dV = Δ·dS + r(B − ΔS)dt
│   └── No-Arbitrage ⇒ Black–Scholes PDE
├── 4️⃣ PDE Solution
│   ├── Boundary: V(S,T)=max(S−K,0)
│   ├── d₁ = [ln(S₀/K)+(r+½σ²)T]/(σ√T)
│   ├── d₂ = d₁ − σ√T
│   ├── Call = S₀N(d₁) − K·e^(−rT)·N(d₂)
│   └── Put  = K·e^(−rT)·N(−d₂) − S₀N(−d₁)
├── 5️⃣ Outputs
│   └── Option values & Greeks (Δ, Γ, Θ, Vega, ρ)
├── 6️⃣ Interpretations
│   ├── Delta hedging = continuous risk elimination
│   ├── Risk-neutral valuation replaces μ with r
│   └── Volatility drives time value
└── 7️⃣ Extensions
    ├── Dividends: use S₀·e^(−qT)
    ├── American options: free-boundary
    ├── Stochastic volatility (Heston)
    ├── Jump diffusion (Merton)
    └── Binomial model: discrete-time limit
```

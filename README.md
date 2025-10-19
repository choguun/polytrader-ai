## What it does
A prediction market analyst that deploys domain-expert AI agents (crypto, politics, sports) with Bayesian probability 
  aggregation for systematic alpha. Analyzes Polymarket events, delivering multi-agent consensus and trade recommendations in 
  10-30 min. Quick alpha at $0.01, deep research for trade at $1—built for traders seeking evidence-backed edge, autonomous mode for manage usdc of user autonomously with AI strategy + portfolio optimization.

## The problem it solves
Prediction Markets Are Broken

Traders face information overload with thousands of data sources and no systematic analysis framework. Deep market research takes 5-12 hours and costs $100-500 per report. Most predictions rely on gut feelings rather than evidence-based analysis.

Meanwhile, AI agents possess predictive intelligence but have zero monetization pathways. There's no marketplace for AI-generated insights, no trust mechanisms, and manual payment processes block autonomous commerce

## Challenges I ran into
N/A

## Technologies I used
1. Solidity
2. TypeScript
3. LLM
4. Next.js

## How we built it
Our Solution: Systematic Intelligence Meets Autonomous Commerce

9-Agent Intelligence Pipeline

Planner, Researcher, Critic, Analyst, and Reporter agents work together using Bayesian probability aggregation with evidence quality scoring from A to D based on verifiability.

Truly Autonomous

analyzes markets using multi-source search, delivers structured JSON predictions, and receives USDC payment—all without human intervention.

Self-Improving System

Tracks every prediction against actual outcomes, calculates Brier score accuracy automatically, and improves over time while showing transparent historical performance to buyers.

## What's next for
### Wave 2
- Design smart contract and agent architecture
### Wave 3
- Actual implementation of smart contract and agent architecture


### Key Features

- **9-Agent AI System** - Domain-aware orchestration with expert agents: Domain Detection → Domain Experts → Planner → Researcher → Critic → Analyst → Reporter
- **Domain-Specific Expertise** - Specialized analysis for crypto, politic, and sport markets with dedicated expert agents
- **Intelligent Pipeline Routing** - Automatically detects domain and routes to appropriate expert agents while maintaining backward compatibility
- **Bayesian Probability Aggregation** - Mathematical rigor, not just LLM opinions
- **Smart Search Routing** - 90% free APIs (Brave/Tavily), 10% Valyu (academic) - **93% cost savings**
- **Agent-to-Agent Commerce** - Monetized via ACP smart contracts on Base L2
- **Self-Learning System** - Tracks predictions vs outcomes, improves over time
- **Real-Time Data** - Multi-source search (Brave, Tavily, Valyu)
- **Platform Support** - Polymarket & Kalshi markets

## Architecture

### System Overview

```
┌─────────────────────────────────────────────────────┐
│                    AI System                        │
└─────────────────────────────────────────────────────┘
                          │
                          │
            ┌─────────────▼──────────────┐
            │     YieldBet Agent         │
            │    (Prediction AI)         │
            └─────────────┬──────────────┘
                          │
                          │
            ┌─────────────▼──────────────┐
            │   Domain-Aware Orchestrator│
            │                            │
            │   • Domain Detection       │
            │   • Domain Experts         │
            │   • Planner                │
            │   • Researcher             │
            │   • Critic                 │
            │   • Analyst                │
            │   • Reporter               │
            └─────────────┬──────────────┘
                          │
          ┌───────────────┼───────────────┐
          │               │               │
    ┌─────▼─────┐   ┌─────▼─────┐   ┌────▼────┐
    │   Crypto  │   │  Politics  │   │  Sports │
    │   Expert  │   │   Expert   │   │  Expert │
    └───────────┘   └────────────┘   └─────────┘
```

### Vault Architecture & Smart Contract System

The vault architecture enables fully autonomous portfolio management where users deposit USDC and AI agents dynamically allocate capital across prediction market strategies.

```
┌──────────────────────────────────────────────────────────────┐
│                     Vault Smart Contract                     │
│                         (Base L2)                            │
└──────────────────────────────────────────────────────────────┘
                              │
                              │ User Deposits USDC
                              ▼
                    ┌─────────────────┐
                    │  Vault Treasury  │
                    │   (USDC Pool)    │
                    └─────────────────┘
                              │
                              │ AI Agent Allocation
                              ▼
        ┌─────────────────────┴─────────────────────┐
        │                                           │
        │         Portfolio Optimizer AI            │
        │                                           │
        │  • Risk Assessment                        │
        │  • Kelly Criterion Sizing                 │
        │  • Correlation Analysis                   │
        │  • Dynamic Rebalancing                    │
        │  • Historical Performance Weighting       │
        │                                           │
        └─────────────────────┬─────────────────────┘
                              │
                              │ Strategy Allocation
                              ▼
        ┌─────────────────────────────────────────────┐
        │              Category Strategies            │
        └─────────────────────────────────────────────┘
                              │
                ┌─────────────┼─────────────┐
                │             │             │
                ▼             ▼             ▼
        ┌──────────────┐ ┌──────────┐ ┌──────────┐
        │    Crypto    │ │ Politics │ │  Sports  │
        │   Strategy   │ │ Strategy │ │ Strategy │
        │              │ │          │ │          │
        │ • 30-40%     │ │ • 30-40% │ │ • 20-30% │
        │ • BTC/ETH    │ │ • Elections│ │ • Outcomes│
        │ • DeFi       │ │ • Policy  │ │ • Player  │
        │ • Regulatory │ │ • Geopolitics│ • Stats  │
        └──────────────┘ └──────────┘ └──────────┘
                │             │             │
                └─────────────┼─────────────┘
                              ▼
                    ┌─────────────────┐
                    │  Trade Executor  │
                    │                 │
                    │ • Polymarket    │
                    │ • Kalshi        │
                    └─────────────────┘
```

### Vault Smart Contract Features

**Core Functions:**
- `deposit(uint256 amount)` - Users deposit USDC into vault
- `withdraw(uint256 shares)` - Users redeem shares for USDC + profits
- `allocate(Strategy[] strategies)` - AI agent allocates funds across categories
- `rebalance()` - AI agent rebalances portfolio based on performance
- `executeTradeOrder(bytes order)` - Executes trades on prediction markets

**Strategy Allocation Mechanism:**

1. **Portfolio Optimizer AI** analyzes:
   - Historical performance of each category expert
   - Current market opportunities across domains
   - Risk-adjusted returns (Sharpe ratio per category)
   - Correlation between crypto/politics/sports markets
   - Market volatility and liquidity

2. **Dynamic Allocation** based on:
   - **Crypto Strategy (30-40%):** BTC price predictions, ETH moves, DeFi protocol events, regulatory decisions
   - **Politics Strategy (30-40%):** Elections, policy outcomes, geopolitical events, legislative votes
   - **Sports Strategy (20-30%):** Game outcomes, player performance, tournament winners, season records

3. **Risk Management:**
   - Maximum 10% position size per individual market
   - Kelly Criterion for position sizing
   - Diversification across 15-25 concurrent positions
   - Stop-loss at 20% per position
   - Portfolio volatility target: <15% monthly

4. **Performance Tracking:**
   - Each category tracks Brier scores independently
   - Allocation weights adjust based on 30-day rolling performance
   - Underperforming categories get reduced allocation
   - Top performer gets increased allocation (up to max limit)

5. **Autonomous Execution:**
   - AI agent receives analysis from domain experts
   - Aggregates probabilities using Bayesian methods
   - Executes trades when edge > 5% vs market price
   - Automatically claims winnings and compounds into vault

**Vault Economics:**
- **Management Fee:** 2% annual (0.5% quarterly)
- **Performance Fee:** 20% of profits above 10% APY
- **AI Agent Fee:** $0.01-$1 per analysis (paid from vault)
- **Minimum Deposit:** 100 USDC
- **Lock Period:** None (withdraw anytime, subject to liquidity)

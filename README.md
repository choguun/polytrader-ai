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

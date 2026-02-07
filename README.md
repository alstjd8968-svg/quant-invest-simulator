# Strategy-based Investment Simulation System

## 1. Introduction
This project is a strategy-based investment simulation system designed to
compare and analyze different trading strategies under identical market conditions.

Instead of focusing on real-time trading or profit maximization,
the system emphasizes architectural design, strategy abstraction,
and explainable decision-making with AI assistance.

## 2. Problem Statement
Most individual automated trading programs focus on executing a single strategy
and provide limited insight into why a strategy succeeds or fails.

Additionally, AI-driven trading systems often operate as black boxes,
making their decisions difficult to analyze or explain.

## 3. System Overview
The system is composed of four main layers:

- Data Layer: Market prices, financial indicators, and news data
- Strategy Layer: Multiple interchangeable trading strategies
- Execution Layer: Simulation-based order execution
- Analysis Layer: Performance reporting and strategy comparison

## 4. Strategy Design
All trading strategies implement a common interface,
allowing them to be executed and evaluated under the same conditions.

Current strategy types include:
- Quantitative rule-based strategies
- AI-assisted recommendation strategies
- User-defined strategies
  
## 5. AI-assisted Recommendation
AI is used as a decision-support tool rather than an autonomous trader.

The AI module analyzes financial indicators and related news,
providing recommendation scores and textual explanations.
Final trading decisions are made by explicit strategy rules.

## 6. User-defined Strategy
The system allows users to define their own trading strategies
by composing predefined conditions and parameters
without modifying the core trading engine.

## 7. Simulation Flow
1. Load historical market data for a specific date
2. Generate account snapshot
3. Execute strategies for each symbol
4. Apply simulated order execution
5. Evaluate daily assets
6. Generate performance reports
   
## 8. Results & Evaluation
Strategies are evaluated based on:
- Total return
- Drawdown
- Trade frequency
- Consistency across simulation runs

## 9. Future Work
- Web-based visualization dashboard
- Mobile monitoring application
- Integration with broker APIs using an execution abstraction layer

## 10. Tech Stack
- Java (Core simulation engine)
- Python (AI analysis and data processing)
- GitHub Issues (project management)
- Cursor / AI-assisted development



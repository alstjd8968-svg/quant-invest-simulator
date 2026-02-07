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

## 11. Architecture overview
This project is designed to simulate and extend toward real-world automated trading systems.

The core architectural principle is a strict separation between decision-making and execution.

Core Architecture

Domain: Account, Order, Market, Strategy
Service: TradingService, MarketService
Execution Loop: DailySimulation / AutomatedTradingLoop

Strategy는 시장과 계좌의 스냅샷을 읽어 의사결정(Intent) 만을 반환하며, 실제 주문 생성과 체결 관리는 Service 계층에서 수행된다.

Strategies decide what to do.
The execution engine decides how and when it is done.

This separation allows the system to:

Support partial buy/sell and partial fills

Handle unfilled or delayed orders

Reuse the same strategies across simulation, automated trading, and real brokerage APIs

High-level Flow
Market Data
    ↓
Strategy (User / Quant / AI)
    ↓
StrategyDecision (Intent)
    ↓
Execution Engine
    ↓
Orders & Fills
    ↓
Account & Positions

Strategy Layer

The strategy layer is responsible only for decision-making.

Each strategy analyzes the current market context and portfolio state, then outputs a StrategyDecision, which represents trading intent rather than direct orders.

Three strategy types are supported:

User-defined Strategy
Rule-based logic explicitly defined by the user.

Quantitative Strategy
Data-driven strategies based on numerical indicators and statistical factors.

AI-assisted Strategy
Strategies that incorporate AI-generated signals such as sentiment analysis, financial metrics, or confidence scores.

All strategies share a common interface and are interchangeable.

Execution Layer

The execution layer simulates the role of a brokerage system.
It translates strategy decisions into actual orders, manages:

- Order splitting
- Partial fills
- Unfilled or canceled orders
- Position and cash updates

By isolating execution logic, the system can evolve from:

- Daily simulation
- Event-driven automated trading
- Real brokerage API integration

without modifying strategy implementations.

Extensibility

This architecture enables:

- Web and mobile interfaces
- Real-time market data
- Live trading through brokerage APIs
- Advanced AI-driven recommendation systems
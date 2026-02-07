# StrategyDecision

## Purpose
StrategyDecision represents the intent of a trading strategy without directly creating orders.

## Responsibilities
- Express target position intent
- Define entry and exit plans
- Provide confidence or reasoning for execution decisions

## Fields (Conceptual)
- targetPositionSize
- entryPlan
- exitPlan
- confidenceScore
- reasoning

## Design Principles
- StrategyDecision does not create orders
- StrategyDecision does not know about execution details
- Execution layer interprets StrategyDecision

## Strategy Types

### User-Defined Strategy

Explicitly encodes user-specified rules and conditions.
Decisions are made based on predefined, rule-based logic tailored by the user.

### Quantitative Strategy

Leverages numerical indicators such as moving averages, volatility, and trading volumes.
Decisions are derived from quantitative models and statistical factors.

### AI-Assisted Strategy

Incorporates financial data, market news, and external signals as inputs.
Outputs are typically recommendation scores or probabilities, providing additional context or guidance for strategic decisions.
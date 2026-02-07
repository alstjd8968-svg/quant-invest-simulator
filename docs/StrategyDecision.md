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

Domain Responsibilities

Account

- Holds the state of assets and positions.
- Is passively updated based on order execution results.
- Does not directly perform trading actions.

Order

- Core domain object representing trading intent.
- Has state and goes through lifecycle changes after creation.

Market

- Represents external market data and conditions.
- Provides information such as price, volume, and liquidity.
- Not modifiable by the internal system.
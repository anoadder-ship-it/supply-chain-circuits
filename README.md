# Supply Chain Darkpool

Encrypted matching of surplus industrial inventory and carbon credits between competitors.

**Program:** 3HQHpSBSgYkx81E25bSJZVz4mGoW6nQFJWDtZL9fmMR4
**Explorer:** https://explorer.solana.com/address/3HQHpSBSgYkx81E25bSJZVz4mGoW6nQFJWDtZL9fmMR4?cluster=devnet

## The problem

Companies with surplus inventory cannot sell it without revealing excess stock to competitors. Carbon credit trading exposes emission levels publicly. Traditional brokers require disclosing prices upfront.

## The solution

Offers and requests are encrypted. Arcium MPC nodes compare them without seeing the values. Match returned only when all criteria align.

## Circuits

### match_supply - 6 criteria, 16 points each (max 96)

| Field | Offer | Demand |
|---|---|---|
| Material code | What you have (1001=steel) | What you need |
| Quantity | Amount available | Minimum required |
| Quality (1-100) | Your grade | Minimum acceptable |
| Price (cents/unit) | Asking price | Maximum budget |
| Delivery (days) | Your lead time | Maximum acceptable |
| Region | EU=1 Asia=2 US=3 | Required region |

### match_carbon - 4 criteria

| Field | Offer | Demand |
|---|---|---|
| Credits | Amount for sale | Minimum needed |
| Price (cents/credit) | Asking price | Maximum budget |
| Vintage (year) | Year of issuance | Minimum year |
| Certificate | VCS=1 Gold=2 CDM=3 | Required type |

Circuit binaries: https://github.com/anoadder-ship-it/supply-chain-circuits/releases/tag/v0.1.0

## Test results



## Use cases

- Surplus inventory: find buyers among competitors anonymously
- Carbon credits: trade without revealing emission levels
- Circular economy: waste from A becomes feedstock for B
- Capacity exchange: spare factory capacity matched to overflow demand
- Joint procurement: aggregated buying power, volumes stay private

## License

MIT

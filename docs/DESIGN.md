# Kettle design

Implement against this file, not folklore.

## Identity

- Product: **Kettle**
- Repo: `computerpets-kettle`
- Idea: Pet Cooking Dash
- Genre: Arcade kitchen
- Engine: Unity
- Surface: `Unity editor`

## Loop

Feed is currently a click. Kettle makes the meal: recipes keyed to species (bamboo steam for Rui, brine for Paint). Buffs expire. Burned food still feeds, no buff.

## Play beats

- Ticket queue of hungry pets (yours + visitors).
- Cook within patience timer.
- Plate = care event with buff JSON.
- Visiting pets cannot be poisoned — canon gate.

## Neighbors

- computerpets (feed + buffs)
- computerpets-lure (ingredients)
- computerpets-acre (crops)
- computerpets-ledger

## Failure doctrine

Timer to zero → dish dumped, pet stays hungry, overlay does not crash. Recipe missing species → generic chow.

## Hard rules

1. Minigames cannot mint or burn NFTs by themselves (Minter is the write path).
2. Stats come from lived overlay care + Dojo caps, not cash shop.
3. Species kits stay inside Lore. Illegal hybrids never spawn.
4. Fail soft: the desktop overlay process is not this process.

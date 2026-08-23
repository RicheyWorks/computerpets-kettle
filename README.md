# Kettle

**Pet Cooking Dash** — Time-management cooking game that prepares stat-boosting meals for overlay care.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) universe. Map: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. Gameplay contract is frozen. Engine choice is the one in the brief. Implementation comes next.

## Loop

Feed is currently a click. Kettle makes the meal: recipes keyed to species (bamboo steam for Rui, brine for Paint). Buffs expire. Burned food still feeds, no buff.

## Genre & engine

- Genre: **Arcade kitchen**
- Engine: **Unity**
- Stack: Unity 6 · C# · time-management stations · meals apply overlay buffs
- Default surface: `Unity editor`

## How you play

1. Ticket queue of hungry pets (yours + visitors).
2. Cook within patience timer.
3. Plate = care event with buff JSON.
4. Visiting pets cannot be poisoned — canon gate.

## Talks to

- computerpets (feed + buffs)
- computerpets-lure (ingredients)
- computerpets-acre (crops)
- computerpets-ledger

## Failure doctrine

Timer to zero → dish dumped, pet stays hungry, overlay does not crash. Recipe missing species → generic chow.

Canon rules that never yield:

- 210 living kinds. No illegal hybrids.
- Overlay pets can get tired, sick, or hide. Tokens are not burned by a minigame.
- Desktop walk stays the main quest. Closing Kettle must leave Rui walking.

## Layout

```
computerpets-kettle/
  README.md
  LICENSE
  docs/DESIGN.md
  src/                implementation lands here
```

## Run (Windows)

```powershell
Unity Hub > open Kettle/; play mode. Meals POST to flagship care API.
```

Meet Rui first via the [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md). This game is optional.

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*

# To-do (future wishlist)

## Ore processing chain
- [x] Foundry for liquid metal (steam-powered; ore or bar -> 100 units molten copper, zinc or iron in its tank; built from 20 stone blocks + 12 iron plates at the Crafting Table; numbers are guesses)
- [ ] Fireproof bricks: a heat-resistant brick (made from clay or similar), to replace the stone blocks in the Foundry's recipe
- [x] Bar Caster: casts molten metal into bars (100 units per bar; fluid pipes in, one output slot; built from 10 stone blocks + 6 iron plates at the Crafting Table; numbers are guesses)
- [x] Liquid alloyer (mix liquid metals into alloys)
- [x] Steel creation (steel is the material for the Industrial tier): coal or wood -> coke in the Steam Furnace, coke -> molten carbon in the Foundry, molten iron + carbon -> molten steel in the Liquid Alloyer, cast into Steel Bars (numbers are guesses)
- [ ] Coke Oven: a machine with the same two coke recipes (coal and wood) at half the materials per coke

## Biomes
- [x] Desert biom
- [ ] Snow biome
- [ ] Volcano biome
- [ ] Underground biomes (idea, not decided): biomes below the surface, e.g. caves with their own look/resources, rather than only surface ones
- [ ] Desert-only resources/content
- [ ] Geothermal vents: a cave feature (and later part of the volcano biome) that gives free heat or steam when you build a boiler over it.
- [ ] Save biome locations: a saved world doesn't remember where its desert is (`World.desert_span` is only filled in on the run that generated it), so any new biome needs its location saved too

## Mechanics workbench
A workbench built with brass, used to make components and advanced automation machines.

- [x] The workbench itself (item, object, art; built at the Crafting Table from 6 brass plates, 2 brass bars, 8 wood; manual)
- [x] Basic Drill recipe (3 brass cogs, 6 iron plates, 4 copper plates, 2 steam pipes; amounts are guesses)
- [x] Brass cog (2 brass plates)

## Industrial tier
The third tier of machines, made of steel. Uses the existing unused steel machine sprites (the steel press and steel sheet bender art has no object, item or recipe yet); the crafting table has none.

- [ ] Industrial Press
- [ ] Industrial Sheet Bender
- [ ] Advanced Crafting Table
  - Needs new art: there is no steel crafting table sprite yet.
  - [ ] Advanced filter pipe: a multi-item filter (several item slots), to go with the single-item Basic Filter Tube
  - [ ] Advanced limiter pipe: to go with the Input Limiter

## Fixes
- [ ] Thin water doesn't reach distant holes: in a headless test, a thin film (e.g. 200 units over ~16 cells) spreads into a gentle slope and stalls ~2 cells short of a hole, because water only flows between cells differing by `MIN_FLOW_DIFF` (2) or more. It then evaporates (sub-16 cells idle 45 ticks) without ever draining. Idea: let the sub-visible front keep flowing toward a lower cell. Stranded smears and pooled spills already behave correctly.

## Low Priority
- [ ] Research bench: recipes unlock by feeding a research bench items, so progression comes from the player's own automation instead of a fixed tech tree.

## Logistics and storage
- [ ] Overflow valve: a pipe piece that only passes fluid above a set level, so tanks can chain without flooding (a fluid-side partner to the Input Limiter).
- [ ] Item vault / large storage: a bigger, upgradable crate that tubes can insert into and pull from.

## Farming and automation
- [ ] Greenhouse / crop farming: planted crops grow with water and light, and feed automation (seeds in, produce out).
- [ ] Tree farm automation: a machine that plants saplings and harvests grown trees (uses the existing sapling and tree systems), so wood can be automated like the drill's output.

## UI and quality of life
- [ ] Better fluid picker: the "select fluid" menu (the Infinite Tank's and the Filter Valve's) is a plain text dropdown made for debugging; replace it with something end-user friendly (e.g. a grid of fluid swatches/icons).
- [ ] Waypoints / map markers: place a marker in the world and see markers on a simple map overlay.

## World visuals
- [ ] Parallax background: a distant-hills texture behind the world that scrolls slower than the terrain
- [x] Steam pipe art (round pipes with slim collars, redrawn so they differ from the fluid pipes and item tubes)

# To-do (future wishlist)

## Ore processing chain
- [ ] Coke Oven: a machine with the same two coke recipes (coal and wood) at half the materials per coke
- [ ] More clay uses: more Mixing Vat recipes (e.g. cement/concrete from sand, stone dust or similar). (Fireproof bricks and the Brick Block are done.)

## Biomes
- [ ] Snow biome
- [ ] Volcano biome
- [ ] Underground biomes (idea, not decided): biomes below the surface, e.g. caves with their own look/resources, rather than only surface ones
- [ ] Desert-only resources/content
- [ ] Geothermal vents: a cave feature (and later part of the volcano biome) that gives free heat or steam when you build a boiler over it.
- [ ] Save biome locations: a saved world doesn't remember where its desert is (`World.desert_span` is only filled in on the run that generated it), so any new biome needs its location saved too

## Industrial tier
The third tier of machines, made of steel. Uses the existing unused steel machine sprites (the steel press and steel sheet bender art has no object, item or recipe yet); the crafting table has none.

- [ ] Industrial Press
- [ ] Industrial Sheet Bender
- [ ] Industrial Mixing Vat: a steel upgrade of the Mixing Vat (faster, bigger tank, more recipes)
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
- [ ] Partial fluid fill in pipes (visual only): instead of fading the fluid's opacity, show each pipe piece partly filled. Spread a network's fluid over its pipes by gravity (lowest pieces first; a horizontal run fills along its bottom), give each piece its own 0-100% level, and have the fill shader clip to that height (a surface line in horizontal pieces, filling from the bottom in vertical ones). Also needs the machine stub pieces handled and some smoothing so the fill doesn't jitter. Behaviour stays the same (real height-based flow would be a much bigger fluid rewrite, not planned).

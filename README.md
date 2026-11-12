# base-unit-trait-ignores-zone-of-control

The `IgnoresZoneOfControl` unit trait: a unit type with it moves as if there were no zones of control.

A unit type with this trait may move from one tile next to an enemy unit to another, which zones of control otherwise forbid.

For example: Civ1: Diplomat and Caravan. Civ2: flag 1 (Diplomat, Spy, Caravan, Freight, Explorer, Partisans).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(IgnoresZoneOfControl)`:

```ts
import IgnoresZoneOfControl from '@civ-clone/base-unit-trait-ignores-zone-of-control/IgnoresZoneOfControl';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, IgnoresZoneOfControl));
```

Part of the unit traits design (civ-clone/web-renderer#1008).

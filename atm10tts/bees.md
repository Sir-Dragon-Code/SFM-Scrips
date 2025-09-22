# BEES
Simple bee script

This is a setup for using advanced beehives + expansion boxes.
Personally, I use full omega upgrades in the hives, and 2 omega + 2 speedier upgrades in the heated centrifuges.

``` Haskell
EVERY 20 TICKS DO
  INPUT FROM hive
  OUTPUT TO comb_store
FORGET
  INPUT configurable_comb FROM comb_store
  OUTPUT TO centri
FORGET
  INPUT FROM centri
  OUTPUT TO storage
FORGET
  INPUT fluid:: FROM centri
  OUTPUT fluid:: TO fluid_store
END

EVERY TICK DO
  INPUT fe:: FROM fe_source
  OUTPUT fe:: TO centri
END
```

| Block | Tag  |
|-|-|
| Advanced Hive | hive |
| Power Source  | fe_source |
| Comb Storage | comb_store |
| Heated Centrifuge | centri |
| End Products | storage |
| Fluid storage | fluid_store |


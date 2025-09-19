# AE 2 Circuit automation using Slicers and Assemblers
## NOTE THIS IS NOT DONE
Most of the material names are incorrect, this is just the base while I don't have access to MC

### Due to a quirk in how these machines work, you make need to do the power using JDT wireless, more testing needed here

``` Haskell
EVERY 20 TICKS DO
  INPUT FROM materials
  OUTPUT certus_block TO slicer_certus
  OUTPUT gold_block TO slicer_gold
  OUTPUT diamond_block TO slicer_diamond
  OUTPUT silicon_block TO slicer_silicon
  OUTPUT redstone_dust TO assembler_all SLOTS 2
FORGET
  INPUT FROM slicer_all
  OUTPUT sliced_silicon TO assembler_all SLOTS 1
  OUTPUT sliced_certus TO assembler_certus SLOTS 0
  OUTPUT sliced_gold TO assembler_gold SLOTS 0
  OUTPUT sliced_diamond TO assembler_diamond SLOTS 0
FORGET
  INPUT FROM assembler_all
  OUTPUT TO circuit_storage
END
```

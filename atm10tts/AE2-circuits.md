# AE 2 Circuit automation using Slicers and Assemblers

### Due to a quirk in how these machines work, you make need to do the power using JDT wireless, more testing needed here

``` Haskell
EVERY 20 TICKS DO
  INPUT FROM materials
  OUTPUT ae2:quartz_block TO slicer_certus
  OUTPUT gold_block TO slicer_gold
  OUTPUT diamond_block TO slicer_diamond
  OUTPUT silicon_block TO slicer_silicon
  OUTPUT redstone TO assembler_all SLOTS 2
FORGET
  INPUT FROM slicer_all
  OUTPUT printed_silicon TO assembler_all SLOTS 1
  OUTPUT printed_calculation_processor TO assembler_certus SLOTS 0
  OUTPUT printed_logic_processor TO assembler_gold SLOTS 0
  OUTPUT printed_engineering_processor TO assembler_diamond SLOTS 0
FORGET
  INPUT FROM assembler_all
  OUTPUT TO circuit_storage
END
```

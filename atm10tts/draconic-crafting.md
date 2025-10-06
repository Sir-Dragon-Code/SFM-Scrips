# Draconic Crafting

``` Haskell
-- Draconic Crafting
-- This script is setup with AE2 blocking mode in mind, in which the AE2 pattern provider is set to a barrel/chest on block until primary crafting result is obtained
-- This does require you to set the crafting recipe in such a way that the item that needs to be first is in slot 0 of the crafting recipe, since AE2 is smart with how it places items

EVERY 20 TICKS DO
  INPUT FROM materials
  OUTPUT RETAIN 1 TO core
  OUTPUT RETAIN 1 TO EACH injector
FORGET
  INPUT FROM core
  OUTPUT TO provider
END

-- If the source is an energy cube, sides are needed (ex. TOP SIDE after FeSource, and set energy cube to output to top)
EVERY TICK DO
  INPUT fe:: FROM feSource
  OUTPUT fe:: TO injector
END
```

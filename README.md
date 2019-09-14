# Stardew Schedule Fixes

This ContentPatcher mod fixes schedule bugs present in Stardew Valley v1.3.36

## Installation

1. Install
   [ContentPatcher](https://github.com/Pathoschild/StardewMods/tree/develop/ContentPatcher)
2. Copy the `[CP] ScheduleFixes` directory into your Stardew Valley `Mods`
   directory

## Changes

### Alex

#### Wednesdays if 6 or more hearts with Alex
* **Before**: Go to HaleyHouse at 1200 if less than 6 hearts with Haley.
  Otherwise, fall back to spring schedule.
* **After**: Follow current season schedule.
* **Root cause**: `Wed_6` requires a season prefix, e.g. `spring_Wed_6`,
  `summer_Wed_6`.

### Demetrius

No observable changes, but location strings of `ScienceHouse 19 4 11` were
changed to `ScienceHouse 19 4 1` to provide a valid face direction.

### Elliott

#### Fridays if 6 or more hearts with Elliott
* **Before**: Go to Beach wharf at 1100 and then Saloon at 1700 if less than 6
  hearts with Leah. Otherwise, fall back to spring schedule.
* **After**: Follow Thursday schedule (SeedShop at 1130).
* **Root cause**: `Fri6` requires a season prefix and an underscore between the
  day and heart value, e.g. `spring_Fri_6`, `summer_Fri_6`.

### Harvey

#### Saturdays
* **Before**: Stay in HarveyRoom all day.
* **After**: Go to ArchaeologyHouse at 830, and return to HarveyRoom at 1500.
* **Root cause**: `ArchaeologyHouse` had a typo: `ArhcaeologyHouse`.

### Leah

#### Summer
* **Before**: Stand in the water on the Beach shore at 1200.
* **After**: Stand a bit further back and draw.
* **Root cause**: `Beach 72 18` is on the right side of the beach, and NPCs
  don't seem to path there correctly, even if the wooden bridge has been
  repaired.

### Lewis

#### Fall 9
* **Before**: Follow Marnie's hospital schedule.
* **After**: Follow Lewis's default schedule except for the hospital visit.
* **Root cause**: It seems like Marnie's schedule was accidentally pasted here.
  Perhaps it was intentional that Lewis goes to AnimalShop, but it doesn't seem
  right for him to overlap on Marnie's tiles.

#### Winter sundays
* **Before**: Stay in ManorHouse all day.
* **After**: Go to ArchaeologyHouse at 1100, and return to ManorHouse at 1600.
* **Root cause**: `ArchaeologyHouse` was typed as `Library`.

### Maru

#### Summer mondays
* **Before**: Fall back to summer schedule.
* **After**: Stand beside Penny in Town on rock bench at 1310, then return to
  ScienceHouse at 1830.
* **Root cause**: The season in `Summer_Mon` needs to have a lowercase letter.

#### Summer sundays
* **Before**: Fall back to summer schedule.
* **After**: Stand beside Penny in Maru's room in ScienceHouse at 1230 (after
  a similar fix to Penny's schedule).
* **Root cause**: The season in `Summer_Sun` needs to have a lowercase letter.

### Penny

#### Winter 4
* **Before**: Fail to sit down on Town bridge to JojaMart at 1600.
* **After**: Stand on bridge near original location.
* **Root cause**: The bridge railing doesn't appear to be a valid location.

#### 9th and 23th of each season if hearts with Sam and Penny are both below 6
* **Before**: Fail to sit down on Town bridge to ArchaeologyHouse at 1100.
* **After**: Stand on bridge beside Sam.
* **Root cause**: The bridge railing doesn't appear to be a valid location.

#### Summer sundays
* **Before**: Fall back to summer schedule.
* **After**: Go to Maru's room in ScienceHouse at 1200, then return to Trailer
  at 1800.
* **Root cause**: The season in `Summer_Sun` needs to have a lowercase letter.

### Sebastian

#### 15th of each month
* **Before**: Stand near couch in SebastianRoom expecting Abigail at 1200.
* **After**: Follow current season schedule.
* **Root cause**: It appears that `15` was a typo for `25`.

#### 25th of each month
* **Before**: Fall back to current season schedule.
* **After**: Stand near couch in SebastianRoom expecting Abigail at 1200.
* **Root cause**: It appears that `15` was a typo for `25`.

#### Fall
* **Before**: Fail to walk to `Mountain 64 14`.
* **After**: Walk directly from `Mountain 57 33` to `Mountain 42 13` at 1430.
* **Root cause**: The Mountain areas around the cave entrance don't appear to be
  pathable.

### Shane

#### Winter 15
* **Before**: Stand in AnimalShop kitchen all day and don't go to Night Market.
* **After**: Go to the big tree in Forest at 1100, then go to Night Market at
  1500.
* **Root cause**: `AnimalShop 37 10` is invalid and should be `Forest 37 10`.

#### Summer sundays
* **Before**: Stand in AnimalShop kitchen all day and don't go to Saloon.
* **After**: Go to the big tree in Forest at 1100, then go to Saloon at 1600.
* **Root cause**: `AnimalShop 37 10` is invalid and should be `Forest 37 10`.

#### Sundays
* **Before**: Stand in AnimalShop kitchen all day and don't go to Saloon.
* **After**: Go to the big tree in Forest at 1100, then go to Saloon at 1600.
* **Root cause**: `AnimalShop 37 10` is invalid and should be `Forest 37 10`.

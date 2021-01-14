# Monster Sanctuary Exported Data
Dump of monster, item and skills data ripped from Monster Sanctuary for usage in tools, mods and apps.

# Contents
Folders contain game files converted from unity prefab yaml to json. Most data related to animation, sprites and unity were removed.

## db_raw
This file has all contents from the folder in a single file

## db_parsed
File sticks to the following format:
```js
{
    skills: [],
    passives: [],
    explore: [],
    items: [],
    equips: [],
    monsters: [],
    champions: [],
    misc: [],
    enums: {
        monsterTypes: {},
        elements: {},
        damageTypes: {},
        damageNumberTypes: {}
    }
}
```
Fields reference other objects by their `guid`.  
This file adds some fields like "HitCount" for skills and decodes "MonsterTypes".

## db_parsed_expanded
Same as above but all referenced objects are expanded. (For instance, monsters already come with all skill data embedded)

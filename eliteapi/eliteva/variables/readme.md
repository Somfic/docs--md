# Variables

Variables in EliteVA are split into two types; *Status* and *Event* variables. Status variables are variables that are
constantly updated, while Event variables are only updated when a new event is triggered.

## Status variables

Status variables are constantly updated as you play the game. The default syntax for these variables is:

```
{<TYPE>:EliteAPI.Status.<Name>}
```

|Type|Name|Description|
|---|---|---|
|`boolean`|Available|Set to `false` when the Commander in the main menu or not in-game|
|`boolean`|Docked|Set to `true` when the ship is docked|
|`boolean`|Landed|Set to `true` when the ship is landed|
|`boolean`|Gear|Set to `true` when the ship's gear is extended|
|`boolean`|Shields|Set to `true` when the ship's shields are online|
|`boolean`|Supercruise|Set to `true` when the ship is in supercruise|
|`boolean`|FlightAssist|Set to `true` when the ship's flight assist mode is on|
|`boolean`|Hardpoints|Set to `true` when the ship's weapons are deployed|
|`boolean`|Winging|Set to `true` when the Commander is in a wing|
|`boolean`|Light|Set to `true` when the ship's lights are on|

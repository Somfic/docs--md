Status variables are constantly updated as you play the game. The default syntax for these variables in VoiceAttack is as follows:

```
{<TYPE>:EliteAPI.Status.<Name>}
```

For more information on VoiceAttack variables see [the VoiceAttack help guide](https://voiceattack.com/VoiceAttackHelp.pdf).

## Available variables
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
|`boolean`|CargoScoop|Set to `true` when the ship's cargo scoop is extended|
|`boolean`|SilentRunning|Set to `true` when the ship is in silent running mode|
|`boolean`|Scooping|Set to `true` when the ship is scooping fuel from a star|
|`boolean`|SrvHandbreak|Set to `true` when the SRV's handbreak is enabled|
|`boolean`|MassLocked|Set to `true` when the ship is mass-locked and cannot jump|
|`boolean`|FsdCharging|Set to `true` when the frame shift drive is charging|
|`boolean`|FsdCooldown|Set to `true` when the frame shift drive is in cooldown|
|`boolean`|LowFuel|Set to `true` when the ship is low on fuel|
|`boolean`|Overheating|Set to `true` when the ship is overheating|
|`boolean`|HasLatLong|Set to `true` when the ship's latitude and longitude on the body are known|
|`boolean`|InDanger|Set to `true` when the ship is in danger|
|`boolean`|InInterdiction|Set to `true` when the ship is being interdicted|
|`boolean`|InMothership|Set to `true` when the commander is in the mothership|
|`boolean`|InFighter|Set to `true` when the commander is in a figher|
|`boolean`|InSrv|Set to `true` when the commander is in a SRV|
|`boolean`|AnalysisMode|Set to `true` when the ship's cockpit mode is in analysis mode|
|`boolean`|NightVision|Set to `true` when the ship's night vision is enabled|
|`boolean`|AltitudeFromAverageRadius|Set to `true` when the ship's altitude is calculated from the body's average radius, rather than from the surface|
|`boolean`|FsdJump|Set to `true` when the ship is jumping between star systems|
|`boolean`|SrvHighBeam|Set to `true` when the SRV's high beam is enabled|
|`integer`|Pips.System|Them amount of half-pips set to the ship's systems|
|`integer`|Pips.Engines|The amount of half-pips set to the ship's engines|
|`integer`|Pips.Weapons|The amount of half-pips set to the ship's weapons|
|`integer`|Pips.Weapons|The amount of half-pips set to the ship's weapons|
|`integer`|FireGroup|The ship's active fire-group|
|`integer`|GuiFocus|The currently focussed GUI, see [Gui modes](gui-modes.md)|
|`decimal`|Fuel.Main|The amount of fuel left in the main tank|
|`decimal`|Fuel.Reservoir|The amount of fuel left in the reservoir tank|
|`integer`|Cargo|The amount of cargo on the ship|
|`text`|LegalState|The commander's legal state in this system|
|`decimal`|Latitude|The ship's latitude on this body|
|`decimal`|Longitude|The ship's longitude on this body|
|`decimal`|Altitude|The ship's altitude on this body|
|`decimal`|Heading|The ship's heading on this body|
|`text`|Body|The name of the active body|
|`integer`|BodyRadius|The radius of the active body|
|`boolean`|OnFoot|Whether the commander is on foot|
|`boolean`|InTaxi|Whether the commander is in a taxi|
|`boolean`|InMultiCrew|Whether the commander is in multi-crew|
|`boolean`|OnFootInStation|Whether the commander is on foot in a station|
|`boolean`|OnFootOnPlanet|Whether the commander is on foot on a planet|
|`boolean`|AimDownSight|Whether the commander is aiming down the sight of their weapon|
|`boolean`|LowOxygen|Set to `true` if the commander is low on oxygen|
|`boolean`|LowHealth|Set to `true` if the commander's health is low|
|`boolean`|Cold|Set to `true` if the commander is cold|
|`boolean`|VeryCold|Set to `true` if the commander is very cold|
|`boolean`|Hot|Set to `true` if the commander is hot|
|`boolean`|VeryHot|Set to `true` if the commander is very hot|

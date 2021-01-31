A VoiceAttack plugin for Elite: Dangerous, powered by [EliteAPI](https://www.github.com/EliteAPI/EliteAPI).

EliteVA is a plugin for VoiceAttack that can full connect your macros to your Elite: Dangerous game. With events, variables and keybindings support. With EliteVA it is now possible to make a truly intelligent voice assistant.

[[guides]]

## Why EliteVA?
Let's consider the scenario of wanting to retracting our landing gear through a VoiceAttack macro.

### Without EliteVA
Tradionally, the macro would be quite simple:

```
Press the `G` key
```

However, this isn't a very smart way to go about it. 
What if the landing gear is already retracted, what if the commander is currently in supercruise? 
Or what if the landing gear key is not actually the `G` key?

There are a lot of scenarios where this macro would fail. EliteVA can help you turn your profiles into intelligent voice assistantances that actually know what is going on in-game.

### With EliteVA
When using EliteVA we can make the macro smarter in a lot of ways.

We can first check if the landing gear is not already retracted:

``` 
Boolean compare: EliteAPI.Gear equals True 
```

Then we can check if the commander is in normal non-supercruise space

```
Boolean compare: EliteAPI.Supercruise equals False
``` 

Finally, we can have our macro press the corresponding landing gear key

```
Press variable key: [EliteAPI.LandingGearToggle]
```

Implementing all these checks into your profile will certainly boost your profile's intelligence significantly.

## Getting started
Let's get you up and running, commander.

### Installation
EliteVA is distributed through GitHub; the recommended way to install this plugin. Alternatively, the plugin could also be compiled to retrieve the plugin file.

Download the [EliteVA zip](https://github.com/EliteAPI/EliteVA/releases) and extract it in a new folder called `EliteVA` in your `VoiceAttack\Apps` directory. 
Make sure **Plugin Support** is enabled in VoiceAttack. After restarting VoiceAttack the EliteVA plugin will be ready to go.

### Events
```
((EliteAPI.Ship.Gear))
```

EliteVA converts a ton of in-game events to macro commands. For example, retracting your gear will trigger the `((EliteAPI.Ship.Gear))` command, while cracking an ateriod will trigger the `((EliteAPI.AsteroidCracked))` event.

A list of all supported in-game events can be found [on the documentation website](https://docs.somfic.com/project/eliteapi/eliteva).

### Variables
```
{BOOl:EliteAPI.Gear}
```
A number of variables are made available through EliteVA, these variables are synced with the game. For example, `{BOOl:EliteAPI.Gear}` holds the the value of the ship's landing gear, and `{BOOL:MassLocked}` contains information on whether or not you're currently mass-locked.

A list of all supported variables can be found [on the documentation website](https://docs.somfic.com/project/eliteapi/eliteva).

### Bindings

```
Variable keypress: [EliteAPI.LandingGearToggle]
```

All in-game keybindings are made available through EliteVA and are updated whenever a change is made to the keybindings preset in-game. 
Instead of traditionally having VoiceAttack press `G` when you want to retract the landing gear, your macro can press the actual key assigned to the gear using the `{TXT:EliteAPI.LandingGearToggle}` variable.

A list of all supported keybindings can be found [on the documentation website](https://docs.somfic.com/project/eliteapi/eliteva).

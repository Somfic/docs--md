EliteVA is a VoiceAttack plugin for Elite: Dangerous, powered by [EliteAPI](https://www.github.com/EliteAPI/EliteAPI).

EliteVA is a plugin for VoiceAttack that can fully connect your macros to the Elite: Dangerous game. With events, variables and keybindings support. With EliteVA it is now possible to make a truly intelligent voice assistant.

[[guides]]

## Why EliteVA?
Let's consider the scenario of wanting to retract our landing gear through a VoiceAttack macro.

### Without EliteVA
Traditionally, the macro would be quite simple:

```
Press the `G` key
```

However, there are a lot of points at which this macro could fail. 
What if the landing gear is already retracted or what if the commander is currently in supercruise? 
What if the landing gear key is not actually the `G` key?

There are a lot of scenarios where this macro would fail. EliteVA can help you turn your profiles into intelligent voice assistants that actually know what is going on in-game.

### With EliteVA
First, we can first check if the landing gear is not already retracted:

``` 
Boolean compare: EliteAPI.Gear equals True 
```

Then we can check if the commander is in normal (non-supercruise) space

```
Boolean compare: EliteAPI.Supercruise equals False
``` 

Finally, we can have our macro press the corresponding landing gear key

```
Press variable key: [EliteAPI.LandingGearToggle]
```

Implementing all these checks into your profile will boost your profile's intelligence significantly.

## Getting started
Let's get you up and running, commander.

### Installation
EliteVA is distributed through GitHub; the recommended way to install this plugin. Alternatively, the plugin could also be compiled to retrieve the plugin files.

Download the latest [EliteVA zip](https://github.com/EliteAPI/EliteVA/releases) and extract it in a new folder called `EliteVA` in your `VoiceAttack\Apps` directory. 
Make sure **Plugin Support** is enabled in VoiceAttack. After restarting VoiceAttack, the EliteVA plugin will be ready to go.

### Events
```
((EliteAPI.Ship.Gear))
```

EliteVA aims to convert all in-game events to macro commands. For example, retracting our gear will trigger the `((EliteAPI.Status.Gear))` command, while cracking an asteroid will trigger the `((EliteAPI.AsteroidCracked))` event.

A list of all supported in-game events can be found [in the events guide](./events).

### Variables
```
{BOOl:EliteAPI.Gear}
```

A number of variables are made available through EliteVA, these variables are alwaus synced with the game. For example, `{BOOl:EliteAPI.Gear}` holds the value of the ship's landing gear, while `{BOOL:MassLocked}` contains information on whether you're currently mass-locked.

A list of all supported variables can be found [in the variables guide](./variables).

### Bindings

```
Variable keypress: [EliteAPI.LandingGearToggle]
```

All in-game keybindings are made available through EliteVA and are updated whenever a change is made to the keybindings preset in-game. 
Instead of traditionally having VoiceAttack press `G` when you need to retract your landing gear, your macro can now press the actual key assigned to the gear using the `{TXT:EliteAPI.LandingGearToggle}` variable.

A list of all supported keybindings can be found [in the keybindings guide](./bindings).

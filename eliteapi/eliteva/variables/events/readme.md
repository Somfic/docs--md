EliteVA aims to redirect all Journal event variables to VoiceAttack variables.
The default syntax for event variables in VoiceAttack is as follows:

```
{<Type>:EliteAPI.<EventName>.<PropretyName>}
```

Elite: Dangerous outputs hundreds events with thousands of parameters in total. 
For a full list of all available events and variables see the [official Journal manual](https://hosting.zaonce.net/community/journal/v30/Journal_Manual_v30.pdf).
Every event mentioned in this manual is made available in EliteVA.

For more information on VoiceAttack variable usage see [the VoiceAttack help guide](https://voiceattack.com/VoiceAttackHelp.pdf).

## ActiveVariables.txt
During runtime, EliteVA will generate a file named `ActiveVariables.txt` in the same folder as the `EliteVA.dll` file.
This file is constantly updated to reflect which variables are set by EliteVA. 
If you're ever unsure about which specific variables the plugin has set, the `ActiveVariables.txt` file will be your best bet to find out.

## Complex variables
Some events contain complexer variables; **objects** and **arrays**. EliteVA is able to handle these complex variables too.

### Objects
Variables within objects are prefixed with the name of the object.

For example, let's take part of the `Statistics` event that's triggered during startup. 
The event's (simplified) JSON:
```
{
    Timestamp:         2021-05-20T13:46:29Z,
    BankAccount: {
        CurrentWealth:            974830088,
        SpentOnShips:             153304805,
        SpentOnOutfitting:        439958912,
    }
}
```
Would result in:

|Type|Name|Value|
|---|---|---|
|`date`|Timestamp|2021-05-20 13:46:29|
|`integer`|BankAccount.CurrentWealth|974830088|
|`integer`|BankAccount.SpentOnShips|153304805|
|`integer`|BankAccount.SpentOnOutfitting|439958912|

Objects within objects work the same way.

### Arrays
All array values are prefixed with the name of the array and their index within the array.

For example, let's take the `Scan` event that occurs whenever we scan a system.
The event's (simplified) JSON:
```
{
   Timestamp:                 2021-05-20T13:57:17Z,
   ScanType:                              AutoScan,
   Rings: [
      {
         Name:        Bleia Byoe QM-W c4-21 A Belt,
         RingClass:               eRingClass_Rocky,
      },
      {
         Name:        Bleia Byoe QM-W c4-21 B Belt,
         RingClass:              "eRingClass_Rocky,
      }
   ]
}
```
Would result in:

|Type|Name|Value|
|---|---|---|
|`date`|Timestamp|2021-05-20 13:57:17|
|`text`|ScanType|AutoScan|
|`text`|Rings[0].Name|Bleia Byoe QM-W c4-21 A Belt|
|`text`|Rings[0].RingClass|eRingClass_Rocky|
|`text`|Rings[1].Name|Bleia Byoe QM-W c4-21 B Belt|
|`text`|Rings[1].RingClass|eRingClass_Rocky|

Please notice: arrays start with an index of 0. An array with a total of 12 items would have indexes 0 - 11.

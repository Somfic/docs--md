Variables in EliteVA are split into two types; *Status* and *Event* variables. Status variables are variables that are
constantly updated, while Event variables are only updated when a new event is triggered.

[[guides]]

## ActiveVariables.txt
During runtime, EliteVA will generate a file named `ActiveVariables.txt` in the same folder as the `EliteVA.dll` file.
This file is constantly updated to reflect which variables are set by EliteVA.
If you're ever unsure about which specific variables the plugin has set, the `ActiveVariables.txt` file will be your best bet to find out.

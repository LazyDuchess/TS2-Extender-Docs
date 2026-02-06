# Globals

These are the new globals that are introduced with TS2 Extender.

## Fields

---

### `TS2Extender`
(boolean) Set to True. This is simply to allow you to check if Extender is installed.

#### Usage:
```lua
if TS2Extender ~= nil then
	-- Extender is installed. Do stuff!
end
```

## Methods

---

### `GetExecutableDirectory()`
Returns the directory path that the game executable is located in.

#### Returns

`path`
: (string) Path to directory.

---

### `GetUserDirectory()`
Returns the directory path that the user data is located in. e.g. `"Documents/EA Games/The Sims 2 Legacy"`.

#### Returns

`path`
: (string) Path to directory.

---

### `RegisterCheat(name, description, callback)`
Registers a new cheat for the in-game Ctrl+Shift+C console.

#### Parameters

`name`
: (string) The name of the cheat.

`description`
: (string) Cheat description as shown by the `help` cheat.

`callback`
: (function) The Lua function that will run when the cheat is called. Arguments are automatically passed from player input.

#### Usage:
```lua
RegisterCheat("Test", "Test cheat! Writes a custom string into a TNS. Usage: Test (string)", function(str)
	nUI.ShowTextNotification(1,str)
end)
```

---

### `GetTS2ExtenderVersion()`
Simply returns the current version of TS2 Extender, as a string.

#### Returns

`version`
: (string) Version string.

---

### `GetUserInput()`
Returns what the player typed into the last `text entry` dialog (called via BHAV Dialog prim), which on an unmodded game goes unused.

#### Returns

`input`
: (string) Player text input.

---

### `OverrideString(originalIndex, originalId, originalGroup, newIndex, newId, newGroup)`
Overrides a string with another.

#### Parameters

`originalIndex`
: (number) Index of the string in the STR#. Beginning from 1.

`originalId`
: (number) Instance ID of the STR# to override.

`originalGroup`
: (number) Group ID of the STR# to override.

`newIndex`
: (number) Index of the new string in the STR#. Beginning from 1.

`newId`
: (number) Instance ID of the new STR#.

`newGroup`
: (number) Group ID of the new STR#.

---

### `ClearStringOverride(originalIndex, originalId, originalGroup)`
Clears a previously overriden string.

#### Parameters

`originalIndex`
: (number) Index of the replaced string in the STR#. Beginning from 1.

`originalId`
: (number) Instance ID of the replaced STR#.

`originalGroup`
: (number) Group ID of the replaced STR#.

---

### `OverrideUI(originalId, newId)`
Overrides a UIScript resource with another.

#### Parameters

`originalId`
: (number) Instance ID of the UIScript to replace.

`newId`
: (number) Instance ID of the new UIScript to use.

---

### `ClearUIOverride(originalId)`
Restores a previously replaced UIScript.

#### Parameters

`originalId`
: (number) Instance ID of the UIScript to restore.

---

### `OverrideMakeMoneyString(callback)`
Replaces the function the game uses to generate money strings (e.g. 900000 -> $900,000)

#### Parameters

`callback`
: (function) Lua function to use to generate money strings.

#### Usage:
```lua
OverrideMakeMoneyString(function(money)
	return money .. " pennies"
end)
```

---

### `ClearMakeMoneyStringOverride()`
Reverses the `OverrideMakeMoneyString` function, making the game generate money strings as normal.

---

### `AddGameCallback(delegate, callback, priority)`
Adds a callback that will run a custom Lua function when an event fires.

#### Parameters

`delegate`
: (number) Delegate or event to listen to.

`callback`
: (function) Lua function to run when the delegate is fired.

`priority`
: (number) Number specifying the order the callback should run at. Higher values mean the callback will run after lower priority ones.

#### Returns

`id`
: (string) Unique ID of the callback, for future removal.

#### Usage:
```lua

-- create a callback that will disable all interactions.

local clearInteractionsCallback = AddGameCallback(Delegates.OnBuildPieMenu, function(interactions, sim, object, clicked, debug)
	interactions:Clear()
end)

-- ..later remove it.

RemoveGameCallback(Delegates.OnBuildPieMenu, clearInteractionsCallback)
```

---

### `RemoveGameCallback(delegate, callbackId)`
Removes a callback previously added with `AddGameCallback`

#### Parameters

`delegate`
: (number) Delegate or event to listen to.

`callbackId`
: (string) Unique ID of the callback to remove.

---

### `EnsureDirectory(path)`
Creates all directories in a path if they don't exist.

#### Parameters

`path`
: (string)

---

### `GetFilesInDirectory(path, extension)`
Recursively returns all files in a path.

#### Parameters

`path`
: (string) Path to the directory.

`extension`
: (string) Extension filter (e.g. ".lua"). Pass "" to allow any extension.

#### Returns

`files`
: (table) Table array with paths to all found files.

---

### `ReadFile(path)`
Reads a file

#### Parameters

`path`
: (string) Path to the file to read.

#### Returns

`fileContents`
: (string) The contents of the file in a string.

---

### `WriteFile(path, contents)`
Writes contents into a file.

#### Parameters

`path`
: (string) Path to the file to write.

`contents`
: (string) Contents to write into the file.
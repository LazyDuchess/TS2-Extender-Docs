# InteractionList

The `InteractionList` class represents the interactions available in a Sim's pie menu. They can be retrieved via the `OnBuildPieMenu` delegate.

## Methods

---

### `InteractionList:Clear()`
Removes all interactions from the pie menu.

---

### `InteractionList:AddInteraction(id, objectId, blocking, name, param0, param1, param2, param3)`
Adds a new interaction to the current pie menu being built.

#### Parameters
`id`
: (number) Instance ID of the interaction BHAV. e.g. 0x0000 and above for global scope, 0x1000 and above for private scope, 0x2000 and above for semi-global scope.

`objectId`
: (number) Object ID of the object to pull the interaction from. When running an interaction from a different object, that object will be used as the Stack Object, so if you're trying to inject an interaction it's recommended you pass the ID of the object you want to perform the interaction on as a param.

`blocking`
: (boolean) Can be true or false. If false, the interaction runs immediately.

`name`
: (string) Display name of the interaction.

`param0`
: (number) Param to pass to the interaction BHAV.

`param1`
: (number) Param to pass to the interaction BHAV.

`param2`
: (number) Param to pass to the interaction BHAV.

`param3`
: (number) Param to pass to the interaction BHAV.
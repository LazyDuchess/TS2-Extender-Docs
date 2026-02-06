# Delegates

Delegates are basically game events you can listen to to run your own custom code. For example, you can listen for the game building the pie menu to inject custom interactions.

You can use delegates via the [AddGameCallback](Globals.md#addgamecallbackdelegate-callback-priority) method.

---

### `Delegates.OnBuildPieMenu(interactions, sim, object, clicked, debug)`
Fired when the game builds a user-directed interaction menu. Happens when hovering and clicking over objects.

#### Parameters

`interactions`
: ([InteractionList](Classes/InteractionList.md)) List of interactions.

`sim`
: (number) Object ID of the sim building the pie menu.

`object`
: (number) Object ID of the target object.

`clicked`
: (boolean) Whether the pie menu is being built because the player has clicked on the object. If False, then we're just hovering the mouse on it.

`debug`
: (boolean) Whether the player is shift clicking with testingcheatsenabled.
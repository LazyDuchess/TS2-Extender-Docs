# Globals

Global utilities that don't fit into a specific category.

## Methods

---

### `RunTree(treeName, objectId, param0, param1, param2)`
Runs a BHAV tree by name, on the provided Object ID and with the provided parameters.

#### Parameters

`treeName`
: (string) Name of the BHAV tree to run.

`objectId`
: (number) ID of the object to run the tree on. "My -> object id" in the BHAV.

`param0`
: (number) (optional) Param0 to be passed to the BHAV.

`param1`
: (number) (optional) Param0 to be passed to the BHAV.

`param2`
: (number) (optional) Param0 to be passed to the BHAV.

#### Returns

`result`
: (boolean) The return value of the tree.

#### Remarks

On top of the obvious benefits of running SimAntics inside the Lua context, this can be used to implement "Check Trees" when performing interaction injection with Extender.
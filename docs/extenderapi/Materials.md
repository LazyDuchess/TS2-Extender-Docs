# Materials

Functions having to do with materials.

---

### `MAT_SetVariable(name, value)`
Sets a global variable for shaders (MATSHAD files) to access.

#### Parameters

`name`
: (string) Name of the variable.

`value`
: (string) Value assigned to the variable. Can be a number, string, or a boolean like `true` or `false`, anything really.

---

### `MAT_RemoveVariable(name)`
Removes a previously set shader global variable.

#### Parameters

`name`
: (string) Name of the variable.
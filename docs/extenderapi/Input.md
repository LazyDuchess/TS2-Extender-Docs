# Input

These are global functions used to poll keyboard and mouse input.

Inputs are currently polled per frame, so you should call these inside of a [Delegates.OnFrameUpdate](Delegates.md) callback.

You can find the Windows key codes at [Microsoft Learn](https://learn.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes). You will have to type them in decimal however, as the version of Lua TS2 uses doesn't support hex codes.

## Methods

---

### `KBM_GetKeyDown(keyCode)`
Returns whether a key was just pressed this frame.

#### Parameters

`keyCode`
: (number) Windows virtual key code for the key to check.

#### Returns

`result`
: (boolean) Whether the key was just pressed this frame.

---

### `KBM_GetKey(keyCode)`
Returns whether a key is being held this frame.

#### Parameters

`keyCode`
: (number) Windows virtual key code for the key to check.

#### Returns

`result`
: (boolean) Whether the key is being held this frame.

---

### `KBM_GetKeyUp(keyCode)`
Returns whether a key was just released this frame.

#### Parameters

`keyCode`
: (number) Windows virtual key code for the key to check.

#### Returns

`result`
: (boolean) Whether the key was just released this frame.
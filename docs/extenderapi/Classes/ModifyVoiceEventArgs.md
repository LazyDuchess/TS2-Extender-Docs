# ModifyVoiceEventArgs

The `ModifyVoiceEventArgs` class represents the arguments for the `OnModifyVoiceEvent` Delegate.

## Fields

---

### `ModifyVoiceEventArgs.Vox`
(string) Voice sample name. Can be modified to alter which voice sample is played.

---

### `ModifyVoiceEventArgs.Suffix`
(string) Suffix for the voice sample, derived from the Sim. Can be modified. If not empty, gets appended to `Vox` with a connecting underscore to form the final sample name.

Examples:

`ama`: (a)dult (m)ale voice (a)

`tfa`: (t)een (f)emale voice (a)

`ca`: (c)hild voice (a)

---

### `ModifyVoiceEventArgs.PersonId`
(number) Object ID of the Sim playing the voice event.
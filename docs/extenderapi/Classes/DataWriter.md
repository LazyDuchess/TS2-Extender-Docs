# DataWriter

The `DataWriter` class allows you to write a sequence of shorts. Similar to something like BinaryWriter in C#.

## Methods

---

### `DataWriter.new()`
Constructs a `DataWriter` instance.

#### Returns

`datawriter`
: (DataWriter)

---

### `DataWriter:Write(value)`
Writes a number into the stream.

#### Parameters

`value`
: (number) Number to write.

---

### `DataWriter:WriteString(str)`
Packs and writes a string into the stream, as shorts.

#### Parameters

`str`
: (string) String to write.

---

### `DataWriter:ApplyToToken(token)`
Copies the contents of the stream into a Sims 2 token, replacing the original properties in the token.

#### Parameters

`token`
: (token) Token to write into.

## Fields

---

### `DataWriter.index`
(number) Current location in the stream.

---

### `DataWriter.data`
(table) Array with all data written so far.
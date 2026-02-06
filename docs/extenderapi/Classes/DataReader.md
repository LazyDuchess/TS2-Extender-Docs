# DataReader

The `DataReader` class allows you to read a sequence of shorts. Similar to something like BinaryReader in C#.

## Methods

---

### `DataReader.new()`
Constructs a `DataReader` instance.

#### Returns

`datareader`
: (DataReader)

---

### `DataReader.FromToken(token)`
Constructs a `DataReader` instance, with the contents from a Sims 2 token.

#### Parameters

`token`
: (token) Token to pull data from.

#### Returns

`datareader`
: (DataReader)

---

### `DataReader:Read()`
Reads a number from the current position in the stream, and advances the position.

#### Returns

`value`
: (number) Number that was read.

---

### `DataReader:ReadString()`
Reads and unpacks a packed string from the stream.

#### Returns

`value`
: (string) String that was read.

## Fields

---

### `DataReader.index`
(number) Current location in the stream.

---

### `DataReader.data`
(table) Array with the data in the stream.
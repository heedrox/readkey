# readkey

A simple node key listener to read keys pressed on keyboard.

# Usage

Create a config object with:
- fn: the function that evaluates if the key has been pressed.
- command: the command executed if fn() returns true

Send it to readkey();

```
const readkey = require('readkey');
const keyCommands = [
  { fn: (str, key) => str === 'p', command: () => push(options) },
  { fn: (str, key) => key.ctrl && key.name === 'c', command: () => process.exit() },
  { fn: (str, key) => key.name === 'q', command: () => process.exit() },
];
readkey(keyCommands);
```



# configurable

  Configuration mixin.

## API

 Make something configurable:

```js
var Configurable = require('configurable');

// plain obj
var obj = {};
Configurable(obj);

// returns the obj itself
var obj = Configurable({});

// make a prototype configurable
Configurable(MyThing.prototype);
```

The object will then have the following methods available:

```js
.get(name)
.set(name, val)
.set(obj)
.enable(name)
.disable(name)
.enabled(name)
.disabled(name)
```

__NOTE__: when assigning to a `.prototype` make sure to re-define `.settings = {}`
in the constructor so objects do not share these values.








# Use arrow functions

Arrow functions are nice.

Instead of:

```javascript
import React from 'react';

const Widget = function(props) {
  return (
    <div>
      I am a widget. My name is {props.name}.
    </div>
  );
}

export default Widget;
```

Try:

```javascript
import React from 'react';

const Widget = props => (
  <div>
    I am a widget. My name is {props.name}.
  </div>
);

export default Widget;
```

[More info on arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

[Next: Destructure your props](destructure-your-props.md)

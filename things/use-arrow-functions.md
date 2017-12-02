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

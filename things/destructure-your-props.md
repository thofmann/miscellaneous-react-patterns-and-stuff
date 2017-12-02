# Destructure your props

It's tedious to always use `props.myProp`.

Instead of:

```javascript
import React from 'react';

const Widget = function(props) {
  return (
    <div>
      I am a widget. My name is {props.firstName} {props.lastName}.
    </div>
  );
}

export default Widget;
```

Try:

```javascript
import React from 'react';

const Widget = ({ firstName, lastName }) => (
  <div>
    I am a widget. My name is {firstName} {lastName}.
  </div>
);

export default Widget;
```

[Next: Spread your props](spread-your-props.md)

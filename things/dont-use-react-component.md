# Don't use `React.Component`

When possible, use pure stateless functions instead!

Instead of:

```javascript
import React, { Component } from 'react';

class Widget extends Component {

  render() {
    return (
      <div>
        I am a widget. My name is {this.props.name}.
      </div>
    );
  }

}

export default Widget;
```

Try:

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

[More info on stateless components](https://hackernoon.com/react-stateless-functional-components-nine-wins-you-might-have-overlooked-997b0d933dbc)

[Next: Use arrow functions](use-arrow-functions.md)

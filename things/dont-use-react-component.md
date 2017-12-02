# Don't Use `React.Component`

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

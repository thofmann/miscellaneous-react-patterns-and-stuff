# You probably shouldn't use context

But if you want to, here's how:

```javascript
import React, { Component } from 'react';
import PropTypes from 'prop-types';

const Title = (props, context) => (
  <h2>
    Language: {context.language}
  </h2>
);

Title.contextTypes = {
  language: PropTypes.string
};

const SmallContainer = () => <div><Title /></div>
const MediumContainer = () => <div><SmallContainer /></div>;
const BigContainer = () => <div><MediumContainer /></div>;

class HugeContainer extends Component {

  getChildContext() {
    return {
      language: 'en'
    };
  }

  render() {
    return <div><BigContainer /></div>;
  }
}

HugeContainer.childContextTypes = {
  language: PropTypes.string
};
```

[Next: Destructure your context, too](destructure-your-context-too.md)

# Use `prop-types`, maybe

This is a nice way to document your components and detect some programming errors during development.

But it's also extra code.

```javascript
import React from 'react';
import PropTypes from 'prop-types';

const TradeLabel = ({currency, price, quantity}) => (
  <p>{quantity} units of {currency} were traded at a price of {price}.</p>
);

TradeLabel.propTypes = {
  currency: PropTypes.string,
  price: PropTypes.number,
  quantity: PropTypes.number
};

export default TradeLabel;
```

[Next: Require props](require-props.md)

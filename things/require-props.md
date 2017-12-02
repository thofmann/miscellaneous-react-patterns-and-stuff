# Require props

If you are going to define the prop types, you might as well specify when they are required.

```javascript
import React from 'react';
import PropTypes from 'prop-types';

const TradeLabel = ({currency, price, quantity}) => (
  <p>{quantity} units of {currency} were traded at a price of {price}.</p>
);

TradeLabel.propTypes = {
  currency: PropTypes.string.isRequired,
  price: PropTypes.number.isRequired,
  quantity: PropTypes.number.isRequired
};

export default TradeLabel;
```

[Next: Specify default props](specify-default-props.md)

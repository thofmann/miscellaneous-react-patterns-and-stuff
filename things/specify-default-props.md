# Specify default props

If a prop is not required, define a default value for it.

```javascript
import React from 'react';
import PropTypes from 'prop-types';

const Avatar = ({ url }) => <img src={url} />;

Avatar.propTypes = {
  url: PropTypes.string
};

Avatar.defaultProps = {
  url: '/img/default-avatar.png'
};

export default Avatar;
```

[Next: Props as props](props-as-props.md)

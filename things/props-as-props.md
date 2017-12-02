# Props as props

Defining entire "props" objects as props can help to organize data, and it works well with spreading props.

It's hard to explain, but here is an example:

```javascript
const Avatar = ({ url }) => (
  <img src={url} />
);

const Name = ({ firstName, lastName }) => (
  <p>Name: {firstName} {lastName}</p>
);

const Info = ({ nameProps, age }) => (
  <div>
    <Name {...nameProps} />
    <p>Age: {age}</p>
  </div>
);

const Profile = ({ avatarProps, infoProps }) => (
  <div>
    <Avatar {...avatarProps} />
    <Info {...infoProps} />
  </div>
);
```

# Props as props

Defining entire "props" objects as props can help to organize data, and it works well with spreading props.

It's hard to explain, but here is an example:

```javascript
const Avatar = ({ url }) => (
  <img src={url} />
);

const Info = ({ firstName, lastName, age }) => (
  <div>
    <p>{firstName} {lastName}</p>

  </div>
);

const Profile = ({ avatarProps, infoProps }) => (
  <div>
    <Avatar {...avatarProps} />
    <Info {...infoProps} />
  </div>
);
```

[Next: Your probably shouldn't use context](you-probably-shouldnt-use-context.md)

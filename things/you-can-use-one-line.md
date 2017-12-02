# You can use one line

If your component is small enough, you might want to fit it on one line.

Instead of:

```javascript
const Title = ({ text }) => (
  <h2>{text}</h2>
);
```

Try:

```javascript
const Title = ({ text }) => <h2>{text}</h2>;
```

[Next: Don't use the index as a key](dont-use-the-index-as-a-key.md)

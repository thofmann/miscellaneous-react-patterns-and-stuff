# Destructure your context, too

Instead of:

```javascript
const greetings = {
  en: 'Hello',
  es: 'Hola',
  jp: 'こんにちは',
  ru: 'Здравствуйте'
};

const Hello = (props, context) => (
  <p>
    {greetings[context.language]} {props.name}
  </p>
);

Hello.propTypes = {
  name: PropTypes.string.isRequired
};

Hello.contextTypes = {
  language: PropTypes.string.isRequired
};
```

Try:

```javascript
const greetings = {
  en: 'Hello',
  es: 'Hola',
  jp: 'こんにちは',
  ru: 'Здравствуйте'
};

const Hello = ({ name }, { language }) => (
  <p>
    {greetings[language]} {name}
  </p>
);

Hello.propTypes = {
  name: PropTypes.string.isRequired
};

Hello.contextTypes = {
  language: PropTypes.string.isRequired
};
```

[More info on destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)

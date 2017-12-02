# Have children

The `children` prop is super useful, especially for making very flexible and reusable components.

Instead of:

```javascript
const Title = ({ text }) => <div className='title'>{text}</div>;

const Subtitle = ({ text }) => <div className='subtitle'>{text}</div>;

const BlueTitle = ({ text }) => (
  <div className='blue-section'>
    <Title text={text} />
  </div>
);

const BlueSubtitle = ({ text }) => (
  <div className='blue-section'>
    <Subtitle text={text} />
  </div>
);

const Titles = ({ title, subtitle }) => (
  <div>
    <BlueTitle text={title} />
    <BlueSubtitle text={subtitle} />
  </div>
);
```

Try:

```javascript
const Title = ({ text }) => <div className='title'>{text}</div>;

const Subtitle = ({ text }) => <div className='subtitle'>{text}</div>;

const Blue = ({ children }) => (
  <div className='blue-section'>
    {children}}
  </div>
);

const Titles = ({ titleText, subtitleText }) => (
  <div>
    <Blue>
      <Title text={titleText} />    
    </Blue>
    <Blue>
      <Subtitle text={subtitleText} />    
    </Blue>
  </div>
);
```

Let's use more children:

```javascript
const Title = ({ children }) => <div className='title'>{children}</div>;

const Subtitle = ({ children }) => <div className='subtitle'>{children}</div>;

const Blue = ({ children }) => (
  <div className='blue-section'>
    {children}}
  </div>
);

const Titles = ({ titleText, subtitleText }) => (
  <div>
    <Blue>
      <Title>{titleText}</Title>
    </Blue>
    <Blue>
      <Subtitle>{subtitleText}</Subtitle>    
    </Blue>
  </div>
);
```

* [Next: Use `prop-types`, maybe](use-prop-types-maybe.md)

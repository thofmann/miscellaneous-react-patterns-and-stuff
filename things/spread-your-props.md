# Spread your props

This can save you from long lists of props.

Instead of:

```javascript
const Todo = ({id, text}) => (
  <div>{id}: {text}</div>
);

const TodoList = ({todos}) => (
  <div>
    {todos.map(todo => (
      <Todo key={todo.id} id={todo.id} text={todo.text} />
    ))}
  </div>
);
```

Try:

```javascript
const Todo = ({id, text}) => (
  <div>{id}: {text}</div>
);

const TodoList = ({todos}) => (
  <div>
    {todos.map(todo => (
      <Todo key={todo.id} {...todo} />
    ))}
  </div>
);
```

[Next: You can use one line](you-can-use-one-line.md)

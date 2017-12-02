# Don't use the index as a key

Try to find/make a better identifier when rendering a list.

Instead of:

```javascript
const TodoList = ({todos}) => (
  <div>
    {todos.map((todo, i) => (
      <div key={i}>{todo.id}: {todo.text}</div>
    ))}
  </div>
);
```

Try:

```javascript
const TodoList = ({todos}) => (
  <div>
    {todos.map(todo => (
      <div key={todo.id}>{todo.id}: {todo.text}</div>
    ))}
  </div>
);
```

[Next: Use lots of small components](use-lots-of-small-components.md)

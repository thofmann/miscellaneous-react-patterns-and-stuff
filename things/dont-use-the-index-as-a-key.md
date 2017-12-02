# Don't use the index as a key

Try to find/make a better identifier when rendering a list.

Instead of:

```javascript
const TodoList = ({ todos }) => (
  <div>
    {todos.map((todo, i) => (
      <div key={i}>{todo.id}: {todo.text}</div>
    ))}
  </div>
);
```

Try:

```javascript
const TodoList = ({ todos }) => (
  <div>
    {todos.map(todo => (
      <div key={todo.id}>{todo.id}: {todo.text}</div>
    ))}
  </div>
);
```

[More info on using an index as a key](https://medium.com/@robinpokorny/index-as-a-key-is-an-anti-pattern-e0349aece318)

[Next: Use lots of small components](use-lots-of-small-components.md)

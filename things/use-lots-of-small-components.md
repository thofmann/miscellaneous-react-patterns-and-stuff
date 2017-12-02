# Use lots of small components

It's way better to use tiny components than complex ones.

Instead of:

```javascript
const TodoList = ({todos}) => (
  <div>
    {todos.map(todo => (
      <div key={todo.id}>{todo.id}: {todo.text}</div>
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
      <Todo key={todo.id} id={todo.id} text={todo.text} />
    ))}
  </div>
);
```

* [Next: Have children](have-children.md)

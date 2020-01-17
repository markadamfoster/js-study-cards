Implement the `updateTodo` and `deleteTodo` methods in this React component:

```js
function TodoList() {
  const [todos, setTodos] = useState([
    {
      id: 1,
      item: "Eat breakfast"
    },
    {
      id: 2,
      item: "Study JavaScript"
    }
  ]);

  const deleteTodo = id => {};

  const updateTodo = todo => {};

  return <div>{/* Todos stuff */}</div>;
}
```

---

```js
const deleteTodo = id => {
  const updatedTodos = todos.filter(todo => todo.id !== id);
  setTodos(updatedTodos);
};

const updateTodo = todo => {
  const updatedTodos = [...todos];
  updatedTodos[todos.findIndex(el => el.id === todo.id)] = todo;
  setTodos(updatedTodos);
};
```

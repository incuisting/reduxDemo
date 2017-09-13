- connect 是做什么用的?
- Provider 的作用是什么？

- react 的ref有什么作用,下面这段代码是什么作用  
答：ref可以通过回调获取dom对象，所以下面node就是input，然后被赋值给了外部变量input input可以调用原生domAPI来获取dom的属性
```jsx
<input
    ref={node => {
        input = node
    }}
/>
```

- mapStateToProps 做什么用的？

- mapDispatchToProps 做什么用的？

- react 纯组件 传参数 下面的{...todo} 怎么可以这样操作

答：拓展运算符。可以把todo里面的内容弄出来，所以最后可以在Todo组件里得到text
```jsx
const TodoList = ({ todos, onTodoClick }) => (
    <ul>
        {todos.map(todo => (
            <Todo key={todo.id} {...todo} onClick={() => onTodoClick(todo.id)} />
        ))}
    </ul>
)
```
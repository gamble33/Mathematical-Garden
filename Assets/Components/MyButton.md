---
defines-react-components: true
react-components-namespace: projects.graphics
---

```jsx:component:MyButton
const [counter, setCounter] = useState(0);
return <button onClick={() => setCounter(old => old + 1)}>Hello {props.name} {counter}</button>
```
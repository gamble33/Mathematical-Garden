---
defines-react-components: true
react-components-namespace: projects.graphics
---

```jsx:component:QuizQuestion
return (
<div>
	<div>{props.question}</div>
	{props.responses.map((response) => <button>{response}</button>)}
</div>
)
```
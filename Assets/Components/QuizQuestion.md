---
defines-react-components: true
react-components-namespace: projects.graphics
---

```jsx:component:QuizQuestion

import confetti from 'https://cdn.skypack.dev/canvas-confetti';

const [answered, setAnswered] = useState(false);

const onCorrectAnswer = () => {
	confetti();
	setAnswered(true);
}

const onWrongAnswer = () => {
	setAnswered(true);
}

return (
<>
	<div>
		<h2>{props.question}</h2>
	</div>
	{props.responses.map((response) => 
	<label><input
		type="radio"
		value={response.text}
		name="response"
	 />{response.text}</label>
	 )}
	 <button type="submit">Submit</button>
</>
)
```
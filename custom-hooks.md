# Custom Hooks
### Questions
  - What does a component’s lifecycle refer to?
    - Each component in React has a lifecycle which you can monitor and manipulate during its three main phases. The three phases are:      
      > Mounting 
      > Updating  
      > Unmounting.
  - Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect
    - We do this because sometimes we need to use callback functions when a state is being changed or updating, depending on where else the function is being used in the app. 
  - Why are functional components preferred over class components?
    > Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks. You end up with less code. They help you to use best practices.
  - What is wrong with the following code?
  
```JavaScript
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

- the useEffect hook doesn't need to be inside the for loop, because there will never be more than one count item because it's getting clobbered each time it changes, in the changeCount function
- instead, use the spread operator to add to it

***

### Terms

|    **Term**    | **Definition**  |
| -------------- | ----------- |
| state hook | the way to affect state without using a class and setState. returns a pair which is the current state value and the function to update it |
| effect hook | allows you to handle side side effects in the functional components |
| reducer hook | accepts a reducer function with the app initial state, returns the current app state and then dispatches a function|

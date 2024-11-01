```js
import React, { useState, useCallback } from 'react';
import Button from './Button'; // Adjust the path as necessary

const App = () => {
  const [count, setCount] = useState(0);
  const [inputValue, setInputValue] = useState('');

  const increment = useCallback(() => {
    setCount(count + 1);
  }, [count]);

  return (
    <div>
      <h1>Count: {count}</h1>
      <Button handleClick={increment} />
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
    </div>
  );
};

export default App;

```
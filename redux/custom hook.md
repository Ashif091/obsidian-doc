You can create your own custom Hooks to reuse stateful logic across multiple components. A custom Hook is a JavaScript function whose name starts with "use" and that may call other Hooks.

```jsx
import { useState, useEffect } from 'react';

function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch(url)
      .then((response) => response.json())
      .then((data) => {
        setData(data);
        setLoading(false);
      });
  }, [url]);

  return { data, loading };
}

```

```jsx
import React from 'react';
import useFetch from './useFetch';

function App() {
  const { data, loading } = useFetch('https://api.example.com/data');

  if (loading) {
    return <div>Loading...</div>;
  }

  return (
    <div>
      <pre>{JSON.stringify(data, null, 2)}</pre>
    </div>
  );
}

export default App;

```


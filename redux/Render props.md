>[!note]
>Render props is a pattern in React for sharing code between components using a prop whose value is a function. This function is called a "render prop" because its purpose is to return a React element that will be rendered by the component.

```jsx 
//DataFetcher
import React, { useState, useEffect } from 'react';

function DataFetcher({ url, children }) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    fetch(url)
      .then(response => response.json())
      .then(data => {
        setData(data);
        setLoading(false);
      })
      .catch(error => {
        setError(error);
        setLoading(false);
      });
  }, [url]);

  return children({ data, loading, error });
}

export default DataFetcher;

```

```jsx
//App.jsx
import React from 'react';
import DataFetcher from './DataFetcher';

function App() {
  return (
    <DataFetcher url="https://api.example.com/data">
      {({ data, loading, error }) => {
        if (loading) {
          return <div>Loading...</div>;
        }

        if (error) {
          return <div>Error: {error.message}</div>;
        }

        return (
          <div>
            <h1>Data:</h1>
            <pre>{JSON.stringify(data, null, 2)}</pre>
          </div>
        );
      }}
    </DataFetcher>
  );
}

export default App;

```
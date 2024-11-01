>[!note]
>Navigating programmatically in Next.js can be achieved using the `useRouter` hook or the `Router` object provided by `next/router`

```jsx

import { useRouter } from 'next/router';
function MyComponent() {
  const router = useRouter();
  const handleClick = () => {
    // Navigate to a different route
    router.push('/about');
  };
  return (
    <button onClick={handleClick}>
      Go to About
    </button>
  );
}

export default MyComponent;

```


>[!Route groups in Next.js are a way to organize your routes into logical sections without affecting the URL structure.]
> This is particularly useful for structuring large applications with complex routing requirements, such as grouping related pages or creating nested routes.

```js
pages/
├── page.jsx          // Home page
├── 📁(auth)/
│   ├──📁login // localhost:3000/login
│       ├──page.jsx
│   ├── 📁singup       // localhost:3000/singup
```

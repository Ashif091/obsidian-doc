>[!Setting up a custom 404 Not Found page in Next.js is straightforward. By default, Next.js provides a built-in 404 page, but you can customize it by creating a `404.jsx` or not-found.jsx ]
>```js
>scr/
├── not-found.jsx
│   
>```


```jsx
export default function NotFound(){
    return <h1> not found 404 </h1>
}
```

## > [[notfound()]] 

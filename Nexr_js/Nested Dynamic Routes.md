>[!note]
>Nested dynamic routes in Next.js combine the concepts of nested routes and dynamic routes, allowing you to create more complex URL patterns that include variable segments at multiple levels of the directory structure

```js
📁pages/app/
├── page.tsx
├── 📁product
│	├── 📁[productid]
│	│    ├── page.tsx // show all products 
│        └── 📁review
│	          ├── 📁[reviewid]
│	              └── page.tsx  // n th review of n th product 
└── 
```
*****
### 📁[review]/pge.tsx

```jsx
export default function ({
  params,
}: {
  params: {productid: String; reviewid: String}
}) {
  return <h1>{params.reviewid} th review of {params.productid} th product </h1>
}
```
*****

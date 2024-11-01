>[!note]
>Dynamic routes allow you to create flexible URL patterns that match a range of paths based on variable data. This is ideal for cases like product pages with unique IDs or blog posts with custom slugs.

```js
pages/
└── app/
    ├── page.tsx
    └── 📁products/
        └── [id].tsx
```

### How to use the id ?
```tsx
export default function Product({params}: {params: {productid: String}}) {
  return (
    <h1 className="text-4xl">this is the {params.productid} th product </h1>
  )
}
```

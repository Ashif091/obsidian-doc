>[!tip]
>you can use the `notFound` option within `getStaticProps` or `getServerSideProps` to programmatically return a 404 page. This is useful when you want to show a 404 page based on certain conditions,

```jsx
import { notFound } from "next/navigation"

export default function Doc ({params}:{params:{products:String[]}}){
    if(parseInt(params.products[0])){
        notFound()
    }
    return <h1>this the page created with catch all segments  {params.products[1]}</h1>
}
```

>[!warning]
>Ensure you have a custom 404 page set up to provide a user-friendly message when the page is not found. Create a `404.js` or `not-found.jsx` file in the `pages` directory:

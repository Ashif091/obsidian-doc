![[Pasted image 20240719101655.png]]

```tsx
export default function RootLayout({
    children,
  }: {
    children: React.ReactNode
  }) {
    return (
        <>
        {children}
        <h1 className="text-sm text-red-700"> new layout for products </h1>
        </>
    )
  }
```

### useMemo ⤵️
```tsx
const data = useMemo(()=>{
return [data]
},[dependencies])

_________Output__________

data = [data] //get only the value

```
### useCallback ⤵️

```tsx
const data = useCallback(()=>{
return [data]
},[dependencies])

_________Output__________

data = ()=>{
return [data]
} //get only the function

```


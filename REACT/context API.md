## ~ normal example ⤵️
### app.tsx
```tsx (app.tsx)
import React, {useState} from "react"

import Navbar from "./components/Navbar"

export const ThemeContext = React.createContext<{theme: boolean; changeTheme: () => void} | undefined>(undefined)
function App() {
  const [theme, setTheme] = useState(false)
  const changeTheme = () => {
    setTheme((pevTheme) => !pevTheme)
  }
  
  return (
    <>
      <ThemeContext.Provider value={{theme, changeTheme}}>
        <Navbar />
      </ThemeContext.Provider>
    </>
  )
} 
export default App
```
### Navbar.tsx
```tsx
import {useContext} from "react"

import {ThemeContext} from "../App"

  

function Navbar() {

  const selectedTheme = useContext(ThemeContext)

  const darkTheme = "bg-gray-800 text-white"

  const style = selectedTheme?.theme ? darkTheme : ""

  return( <div className={`w-full h-[50rem] ${style}`}>

  <button onClick={selectedTheme?.changeTheme} className="bg-orange-500 broder border-orange-50 rounded-sm ">Theme</button>

  </div> )

}

  

export default Navbar
```
## ~ ADVANCED way ⤵️
by setting a provider like
```tsx
interface Props {
  children: ReactNode
}
export const ThemeContext = createContext<{theme: boolean;chagerFun:()=>void} | undefined>(undefined)
export function useTheme(){
    return useContext(ThemeContext)
}
function ThemeProvider({children}: Props) {
    const [theme,setTheme]= useState(false)
    const chagerFun = ()=>{
        setTheme(prevTheme => !prevTheme)
    }
  return (
    <>
      <ThemeContext.Provider value={{theme,chagerFun}}>
        {children}
      </ThemeContext.Provider>
    </>
  )
}
export default ThemeProvider
```
‼️ important 
```
u can only use context by exporting it (export function useTheme(){
    return useContext(ThemeContext)
})
```
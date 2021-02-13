## useContext
離れたコンポーネントでもpropsを経由せずに、ステートを渡すことができる

* import
```
import {createContext} from 'react'
```

* 使い方
App.jsのdivタグを以下のようにする
```
 <AppContext.Provider value={'value from App.js'}>
     <div className="App">
     ・・・
     </div>
 </AppContext.Provider>
```
valueはuseContextとして渡す値
以下のようにAppContext.jsを作成し
```
import {createContext} from 'react'

const AppContext = createContext()

export default AppContext
```
渡したいコンポーネントファイルで
```
const value = useContext(AppContext)
```
のようにすると```value={'value from App.js'}```の値が親コンポーネントから渡され、使うことができる

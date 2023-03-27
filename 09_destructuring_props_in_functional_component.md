# Destructuring Props In Functional Component

### App.js
```
import './App.css';
import Hello from './component/Hello';

function App() {
  return (
    <div className="App">
      <Hello name="lubna" role="developer" />
    </div>
  );
}

export default App;
```

### Hello.js
method 1:
```
import React from 'react'

const Hello = ({name, role}) => {
    return (
      <div>
        <h1>Hello, {name} - {role}</h1>
      </div>
    )
}

export default Hello
```
method 2:
```
import React from 'react'

const Hello = (props) => {
   const {name, role} = props
    return (
      <div>
        <h1>Hello, {name} - {role}</h1>
      </div>
    )
}

export default Hello
```

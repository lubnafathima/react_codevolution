# onClick in Class Component

### App.js
```
import './App.css';
import ClassClick from './component/ClassClick';

function App() {
  return (
    <div className="App">
      <ClassClick />
    </div>
  );
}

export default App;

```

### ClassCompo.js
```
import React, { Component } from 'react'

class ClassClick extends Component {
  render() {
    const clickHandler = () => {
      console.log("clicked")
    }
    return (
      <div>
        <button onClick={clickHandler}>Click Here</button>
      </div>
    )
  }
}

export default ClassClick
```

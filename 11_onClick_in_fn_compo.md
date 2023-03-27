# onClick In functional Component

### App.js
```
import './App.css';
import FnClick from './component/FnClick';

function App() {
  return (
    <div className="App">
      <FnClick />
    </div>
  );
}

export default App;
```

### FnClick.js
```
import React from 'react'

function FnClick() {
    function clicked() {
        console.log("Clicked")
    }
  return (
    <button onClick={clicked}>Click Me</button>
  )
}

export default FnClick
```

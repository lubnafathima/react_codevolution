# Functional Component
## Display a Hello message in Functional Component

### component/Hello.js
```
import React from 'react'

function Hello() {
  return (
    <div>Hello from Functional Component</div>
  )
}

export default Hello
```

### App.js
```
import './App.css';
import Hello from './component/Hello';

function App() {
  return (
    <div className="App">
      <Hello />
    </div>
  );
}

export default App;
```

# Class Component
Displaying a message from class component

### component/Welcome.js
```
import React, { Component } from 'react'

class Welcome extends Component {
    render() { 
        return (
            <div>Hello from Class Component</div>
        );
    }
}
 
export default Welcome;
```

### App.js
```
import './App.css';
import Welcome from './component/Welcome';

function App() {
  return (
    <div className="App">
      <Welcome />
    </div>
  );
}

export default App;
```

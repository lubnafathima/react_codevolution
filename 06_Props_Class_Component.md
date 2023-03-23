# Props in Class Component
### Welcome.js
```
import React, { Component } from 'react'

class Welcome extends Component {
    render() { 
        return (
            <div>Hello, {this.props.name}</div>
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
      <Welcome name="Lubna" />
    </div>
  );
}

export default App;

```

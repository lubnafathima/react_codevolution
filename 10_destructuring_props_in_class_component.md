# 10 Destructuring Props In Class Component

### App.js
```
import './App.css';
import Welcome from './component/Welcome';

function App() {
  return (
    <div className="App">
      <Welcome name="lubna" role="developer" />
    </div>
  );
}

export default App;

```
### Welcome.js
```
import React, { Component } from 'react'

class Welcome extends Component {
    render() { 
        const {name, role} = this.props
        return (
            <React.Fragment>
                <h1>Hello, {name} - {role}</h1>
            </React.Fragment>
        );
    }
}
 
export default Welcome;
```

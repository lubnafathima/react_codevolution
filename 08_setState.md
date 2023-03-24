# setState

### App.js
```
import './App.css';
import Counter from './component/Counter';

function App() {
  return (
    <div className="App">
      <Counter />
    </div>
  );
}

export default App;

```

### Counter.js
```
import React, { Component } from 'react'

class Counter extends Component {
    constructor(props) {
        super(props);
        this.state = {
            count: 0
        }
    }

    increment() {
        this.setState({
            count: this.state.count + 1
        })
    }

    render() { 
        return (
            <React.Fragment>
                <p>Count: {this.state.count}</p>
                <button onClick={() => this.increment()}>Increment</button>
            </React.Fragment>
        );
    }
}

export default Counter;
```

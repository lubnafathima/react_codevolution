# Parameter As Props
# App.js
```
import './App.css';
import ParentCompo from './component/ParentCompo';

function App() {
  return (
    <div className="App">
      <ParentCompo />
    </div>
  );
}

export default App;
```
# ParentCompo.js
```
import React, { Component } from 'react'
import ChildCompo from './ChildCompo'

export class ParentCompo extends Component {
    constructor() {
        super()
        this.state = {
            parentName: 'Parent'
        }
        this.greetParent = this.greetParent.bind(this)
    }

    greetParent(childName) {
        alert(`Hello ${this.state.parentName} from ${childName}`)
    }
  render() {
    return (
      <div>
        <ChildCompo greetHandler={this.greetParent} />
      </div>
    )
  }
}

export default ParentCompo

```
# ChildCompo.js
```
import React from 'react'

function ChildCompo(props) {
  return (
    <button onClick={() => props.greetHandler('child')}>Call Parent</button>
  )
}

export default ChildCompo
```

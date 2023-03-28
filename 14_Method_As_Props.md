# Method As Props
If Child Component wants to communicate with Parent Component we pass method as props to Child Component
#### App.js
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
### ParentCompo.js
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

    greetParent() {
        alert(`Hello ${this.state.parentName}`)
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
### ChildCompo.js
```
import React from 'react'

function ChildCompo(props) {
  return (
    <button onClick={props.greetHandler}>Call Parent</button>
  )
}

export default ChildCompo
```

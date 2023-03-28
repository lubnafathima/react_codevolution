# Binding Event Handler

### App.js 
```
import './App.css';
import EventBind from './component/EventBind';

function App() {
  return (
    <div className="App">
      <EventBind />
    </div>
  );
}

export default App;
```

There are different approaches to bind Event Handler
#### (1) Binding In Rendering

### EventBind.js
```
import React, { Component } from 'react'

class EventBind extends Component {
    constructor() {
        super()
        this.state = {
            msg: "Hello"
        }
    }

    clickHandler() {
        this.setState({
            msg: "Bye"
        })
    }

    render() { 
        return (
            <React.Fragment>
                <p>{this.state.msg}</p>
                <button onClick={this.clickHandler.bind(this)}>Click</button>
            </React.Fragment>
        );
    }
}
 
export default EventBind;
```

#### (2) Binding Arrow In Rendering

### EventBind.js
```
import React, { Component } from 'react'

class EventBind extends Component {
    constructor() {
        super()
        this.state = {
            msg: "Hello"
        }
    }

    clickHandler() {
        this.setState({
            msg: "Bye"
        })
    }

    render() { 
        return (
            <React.Fragment>
                <p>{this.state.msg}</p>
                <button onClick={() => this.clickHandler()}>Click</button>
            </React.Fragment>
        );
    }
}
 
export default EventBind;
```

#### (3) Binding In Class Constructor

### EventBind.js
```
import React, { Component } from 'react'

class EventBind extends Component {
    constructor() {
        super()
        this.state = {
            msg: "Hello"
        }
        this.clickHandler = this.clickHandler.bind(this)
    }

    clickHandler() {
        this.setState({
            msg: "Bye"
        })
    }

    render() { 
        return (
            <React.Fragment>
                <p>{this.state.msg}</p>
                <button onClick={this.clickHandler}>Click</button>
            </React.Fragment>
        );
    }
}
 
export default EventBind;
```

#### (4) Class Property as Arrow Function

### EventBind.js
```
import React, { Component } from 'react'

class EventBind extends Component {
    constructor() {
        super()
        this.state = {
            msg: "Hello"
        }
    }

    clickHandler = () => {
        this.setState({
            msg: "Bye"
        })
    }

    render() { 
        return (
            <React.Fragment>
                <p>{this.state.msg}</p>
                <button onClick={this.clickHandler}>Click</button>
            </React.Fragment>
        );
    }
}
 
export default EventBind;
```

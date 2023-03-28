# Conditional Rendering
### App.js
```
import './App.css';
import UserGreet from './component/UserGreet';

function App() {
  return (
    <div className="App">
      <UserGreet />
    </div>
  );
}

export default App;
```

#### Approach 1: Using If/Else
### UserGreet.js
```
import React, { Component } from 'react'

export class UserGreet extends Component {
    constructor() {
        super()
        this.state = {
            isLogged: true
        }
    }
  render() {
    if(this.state.isLogged) {
        return <div>Welcome user</div>
    } else {
        return <div>Welcome Guest</div>
    }
  }
}

export default UserGreet

```

#### Approach 2: Using Element Variable
### UserGreet.js
```
import React, { Component } from 'react'

export class UserGreet extends Component {
    constructor() {
        super()
        this.state = {
            isLogged: true
        }
    }
  render() {
    let msg
    if(this.state.isLogged) {
        msg = <div>Welcome user</div>
    } else {
        msg = <div>Welcome Guest</div>
    }
    return (
        <div>{msg}</div>
    )
  }
}

export default UserGreet

```

#### Approach 3: Using Itenary Conditional Operator
### UserGreet.js
```
import React, { Component } from 'react'

export class UserGreet extends Component {
    constructor() {
        super()
        this.state = {
            isLogged: true
        }
    }
  render() {
    return (
        this.state.isLogged ? <div>Welcome User</div> : <div>Welcome Guest</div>
    )
  }
}

export default UserGreet

```

#### Approach 4: Using Short Circuit Operator
### UserGreet.js
```
import React, { Component } from 'react'

export class UserGreet extends Component {
    constructor() {
        super()
        this.state = {
            isLogged: true
        }
    }
  render() {
    return (
        this.state.isLogged && <div>Welcome User</div>
    )
  }
}

export default UserGreet

```

# Props in Functional Component
## 1. Method 1:

### Hello.js
```
import React from 'react'

const Hello = (props) => {
    return (
      <div>Hello, {props.name}</div>
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
      <Hello name="Lubna Fathima" />
    </div>
  );
}

export default App;
```

## Method 2:

### Hello.js
```
import React from 'react'

const Hello = (props) => {
    const name = props.name;
    return (
      <div>Hello, {name}</div>
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
      <Hello name="Lubna Fathima" />
    </div>
  );
}

export default App;
```

## 2. Passing Multiple Props
### Hello.js
```
import React from 'react'

const Hello = (props) => {
    const name = props.name;
    const role = props.role;
    return (
      <div>Hello, {name} - {role}</div>
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
      <Hello name="Lubna Fathima" role="Developer" />
    </div>
  );
}

export default App;
```

## 3. Passing Children Props
### Hello.js
```
import React from 'react'

const Hello = (props) => {
    const name = props.name;
    const role = props.role;
    return (
    <div className="App">
      <Hello name="Lubna Fathima" role="Developer">
        <p>This is a Children prop</p>
      </Hello>
    </div>
  );
}

export default Hello
```

### App.js
```
import './App.css';
import Hello from './component/Hello';

function App() {
  return (
    <div>
        <h1>Hello, {props.name} - {props.role}</h1>
        <p>{props.children}</p>
      </div>
  );
}

export default App;
```

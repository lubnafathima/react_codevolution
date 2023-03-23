# IMPORT AND EXPORT

### Hello.js

```
import React from 'react'

export const NamedExport = () => {
  return (
    <div>Hello from Named Export</div>
  )
}

const DefaultExport = () => {
    return (
      <div>Hello from DefaultExport</div>
    )
}

export default DefaultExport
```

### App.js
```
import './App.css';
import Hello, {NamedExport} from './component/Hello';

function App() {
  return (
    <div className="App">
      <Hello />
      <NamedExport />
    </div>
  );
}

export default App;
```

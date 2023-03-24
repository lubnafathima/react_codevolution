# STATE
Create a button that says "Subscribe", When user clicks it, the welcome message should change into Thanks.
### Welcome.js
```
import React, { Component } from 'react'

class Welcome extends Component {
    constructor() {
        super()
        this.state = {
            message: "Welcome"
        }
    }
    
    clickHandler() {
        this.setState({
            message: "Thanks for Subscribing"
        })
    }

    render() { 
        return (
            <div style={{textAlign: 'center'}}>
                <h3>{this.state.message}</h3>
                <button onClick={() => this.clickHandler()}>Subscibe</button>
            </div>
        );
    }
}
 
export default Welcome;
```

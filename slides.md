# Team Gibraltar
#### Presents
<div>
<span>
<img src='images/react-logo.png' width='20%' class='spin image'/>
<img src='images/redux-logo.png' width='20%' class='counter-spin image'/>
</span>
</div>
#### Created By:
Randy && Haiden

---

# What is React?
* React is component based JavaScript UI Framework.
* React takes a composition approach to create reusable UI components.
* A component has an idea of a state or prop. A state represents a components data, primitive values, and react elements/functions.

---

### What about Inheritance?
>At Facebook, we use React in thousands of components, and we haven’t found any use cases where we would recommend creating component inheritance hierarchies.

---

#### What do we love about it?

<!--v-->

 ## ES6 SYNTAX

* Template Strings
```
 `Hello ${user.name}`
```
* Fat Arrow Functions
```
  => () {return true}
``` 
* Destructuring Assignment
```
 {name, role} = this.props.user;
```

<!--v-->

# JSX
* HTML Literals

---

# What is Redux?

#### Redux is a predictable state container for JavaScript apps.

- Why would we use redux?
    * It is tiny (2kB, including dependencies).
    * The state of your app is stored in an object tree inside a single store.

---

#### Redux and it's opinions

* Redux provides the idea of:
    * Global Store, Actions and a Reducer
* The Global Store is a immutable object of the entire application.
* Actions specify the mutations that need to occur to the Store.
* Reducers decides what and how a specific Action transforms the entire applications state.

---
### React-Redux Cycle

<div>
    <img src='images/react-redux-cycle.png' width='70%'/>
</div>

---

#### Why do we think its cool?

* Powerful Developer Tools
    * The state of you application is now held accountable by Actions.
    * You can trace or debug by replicating those actions.
    * We can now make better and more complex choices in our application.

---
## File Structures

* Focus on two basic file structures
    * Modular Components
    * Redux Organization

---

## File Structure - Base
<pre class='no-borders tree'>
React-Redux Project
│   package.json    | Records project info + project dependencies
│   README.md       | Documentation
│                   |
├───node_modules    | Stores all dependency folders
│
├───src
│   │   index.html
│   │   index.js
│   │   store.js
.
.
.
</pre>

<!--v-->

### File Structure - Redux
<pre class='no-borders'>
.  src
.   │
.   ├───styles
│   │
│   ├───actions
│   │       actions
│   │
│   ├───Reducers
│   │       reducers
│   │
│   └───components
│       ├───app
│       │
│       └───componentA
│       .           _componentA
│       .           componentA
│       .
│
├───static
│   └───images
│
└───webpack
</pre>

<!--v-->

### File Structure - Modular
<pre class='no-borders tree'>
.  src
.   │
.   │
│   ├───styles 
│   │
│   └───Components
│       ├───app
│       │     app_reducer
│       │
│       ├───componentA
│       .           _componentA 
│       .           componentA-actions
│       .           componentA-reducer
│                   componentA
├───static
│   └───images
│
└───webpack
</pre>

---

## Component Example
```javascript
import React, { Component } from 'react'

export default class Component extends Component {

  constructor(props, context) {
    super(props);

    this.state = { };
  }
  render() {
    return (
        <div>Hello World</div>
    )
  }

}

```

<!--v-->

## Actions

```javascript
export const GET_COMPONENT_DATA = 'GET_COMPONENT_DATA';

export function getComponentData(data) {
  return {
    type: GET_COMPONENT_DATA,
    payload: data
  }
}

```
<!--v-->

## Reducer 
```javascript
export default function (state={}, action) {
  let stateCopy = {...state};
  switch (action.type) {
    case 'GET_COMPONENT_DATA':
       /*Do your mutex here!*/
       return {...state, your_mutex};
    default:
      return {...stateCopy};
  }
}

```
<!--v-->

## Container 
```javascript
import Component from './component';
import * as ComponentActions from './component-actions.js';
import {bindActionCreators} from 'redux';
import {connect} from 'react-redux';

function mapStateToProps(state) {
  return {
      data: state.your_mutex
  }
}

function mapDispatchToProps(dispatch) {
  return bindActionCreators({
    
  }, dispatch);
}

export default connect(mapStateToProps, mapDispatchToProps)(Component);

```
---

<!-- Was thinking it would be cool to show how many React projects we have -->
## Projects that use React + Redux

* Portal
* DIET
* Tank Vapors
* GroudWater
* Socrates
* 318
* Grow

---

## Resources
* [npmjs](www.npmjs.com)
* [React](github.com/facebook/react)
* [Redux](github.com/buckyroberts/React-Redux-Boilerplate)

---

# Questions?
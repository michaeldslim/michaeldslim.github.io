---
title: "React.js - Props and State"

categories:
  - Blog
tags:
  - react
  - props
  - state
last_modified_at: 2020-08-25T14:06:00-0700
---

### What are props?

Props is for properties and they are used to pass data between React components. React's data flow between components is unidirectional (from parent to child only).

```
class Parent extends Component {
    render() {
        return (
            <Child name="John Doe" />
        );
    }
}

const Child = (props) => {
    return <p>{props.name}</p>;
};
```

### What is state?

It allows components to create and manage their own data. So unlike props, components cannot pass data with state, but they can create and manage it internally.

```
class Person extends React.Component {
    constructor() {
        this.state = {
            id: 1,
            name: "John Doe"
        };
    }

    render() {
        return (
            <div>
              <p>{this.state.id}</p>
              <p>{this.state.name}</p>
            </div>
        );
    }
}
```

#### How do you update a component's state?

State should not be modified directly, but it can be modified with a method called setState().

```
// wrong
this.state.id = "10";

// correct
this.setState({
    id: "10"
});
```

Basically, a functional component can't have a state since there is no "this" keyword but can use useState instead.

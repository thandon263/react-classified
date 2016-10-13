# Why React

* Facebook
* Airbnb
* Dropbox
* Instagram

1. Fast & Responsive
2. Composable components
3. Pluggable
4. Simple to learn
5. Facebook's brain

## JSX

* Live syntax also similar to HTML
* Compiled down to HTML but sits in Javascript - We will use JSX to build and create components.

## What do you need

```HTML
<script src="https://fb.me/react-0.14.7.js"></script>
<script src="https://fb.me/react-dom-0.14.7.js"></script>
```
* You build your components inside the script file or tag.
* Render react components in the DOM

----------------------------------------------------------------------------------

# How to handle events in react

* figure 1.2

```Javascript
var Product = React.createClass({
  getInitialState: function() {
    return {quantity: 0};
  },

  buy: function () {
    this.setState({quantity: this.state.quantity + 1});
    alert("You just Bought an Android!");
  },

  render: function () {
    return (
      <div>
        <p>Android - $199 </p>
        <h3>Quantity: {this.state.quantity} item(s)</h3>
        <button>Buy</button>
        <hr />
      </div>
    )
  }
});

var Total = React.createClass({
  render: function() {
    return (
      <div>
        <h3>Total Cash: </h3>
      </div>
    );
  }

});

var ProductList = React.createClass({
  render: function () {
    return (
      <div>
        <Product/>
        <Product/>
        <Product/>
        <Total/>
      </div>
    )
  }
});

React.render(<Product/>, document.getElementById('root'));

```

# Working with State

- Place where the data comes from.
- Reduce number of stateful components
- Make state as simple as possible
- Only seen on the inside of component definitions
- This is the internal dataset which affects the rendering of components.

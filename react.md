# React

### Creating an app
create-react-app directory-name
npm start

### Declaring Functions
* can be bound to certain 
* Stateless function 
```
const App = () => <h1>Hello stateless</h1>
```
* Other Way 
```
class App extends React.Component(){
	render(){

	}
}
```

### Render 
* returns DOM representation of component
* can only return a single node (because it's similar to a function)

### Props
* static values passed to components
* can get items through: this.props.name
* `App.propsTypes{name: React.PropTypes.String}`: 
* `App.defaultProps{name: "default value"}`: specify default props values specify types, add .isRequired if a props is required 
* custom validation (can change to check length etc): 
```javascript
  Title.propTypes = {
    text(props, propName, component){
      if(!(propName in props)){
        return new 
       ('missing')
      }
    }
  }
```

### State 
* managed and updated by components
* create a constructor, `super()` - gives keyword this the context within component as opposed to parent class, and `this.state= {value: "state text"}`
* to have things change on type create and update function: 
```
 update(e){
    this.setState({txt: e.target.value})
  }
```
* in render, update method bound to 'this': `<input type="text" onChange={this.update.bind(this)}/> 

### Components Rendering Other Components

### props.children
* content between opening and closing tag
* can pass children by: 
	* string: put between opening and closing tags 
	* JavaScript expression: explore within `{}`

### Events
* onKeyPress, onCopy, onCut, onPaste, onFocus, onBlur, onDoubleClick, onTouchStart, onTouchMove, onTouchEnd

### ref
* returns node that is being referenced, can also return callback
* used to differentiate between two similar inputs 
* in an html element (node) add ref = "name"
* to reference: `this.refs.name.value`
* https://egghead.io/lessons/react-using-refs-to-access-components

### Component Lifecycle 
* `componentWillMount()`: right before component mounted into DOM
* `componentDidMount()`: once component is mounted into DOM
* `componentDidUnmount()`: before component leaves the DOM
* Rendering elements: `ReactDOM.render(<App />, document.getElementById('a'))`
* Unmounting elements: `ReactDOM.unmountComponentAtNode(document.getElementById('a'))
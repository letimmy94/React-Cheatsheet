# Component Lifecycle

## There are two types of component lifecycle methods:

### Mounting lifecycle methods.

e.g. What happens when the component is created? Was an initial state set?
Methods:

* constructor()
* componentWillMount()
* render()
* componentDidMount()
* componentWillUnmount()

### Updating lifecycle methods.

e.g. Has state changed?
Methods:

* componentWillReceiveProps()
* shouldComponentUpdate()
* componentWillUpdate()
* render()
* componentDidUpdate()

Axios is a node module commonly used with React to send HTTP requests to an API. It functions much like jQuery's Ajax method, or window.Fetch(). Some benefits to using Axios:

* It is a promise-based library with an interface for simpler and cleaner syntax (compared to native XHR especially).
* It is lightweight and focused solely on handling HTTP requests (as opposed to jQuery which brings in an extensive set of new functions and methods)
* It is very configurable and has a number of useful methods for doing more complex requests from one or multiple API endpoints
* It handles a lot of the http header manual work for you (e.g. send a json file, it sets Content-Type: application/json)

To load in the Axios module:

If you are using Babel to compile your code

```
import axios from 'axios'
```

// In standard vanilla Javascript

```
let axios = require('axios')
```

To use Axios to query an API at a given url endpoint:

```
axios.get('url')
  .then((response) => {
    console.log(response)
  })
  .catch((error) => {
    console.log(error)
  })
```

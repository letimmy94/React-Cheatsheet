# React Router

Allows for a more robust way to render components

## Setup

```
npm install -S react-router-dom
```

Within Index.js

```
import { BrowserRouter as Router } from "react-router-dom";

ReactDOM.render(
  <Router>
    <App />
  </Router>,
  document.getElementById("root")
);

import { Route, Link } from "react-router-dom";
```

Within the navbar create links and in a seperate tage create a route

```
<Link to="">A Link</Link>
<main>
<Route path="" render= {} />
</main>
```

Redirect: is used to redirect the user back to a specific page if it does not exist or manually entered to the wrong page. Needs to be imported with Link, Route

Switch: its key purpose is to have React Router go to and render the first matching result instead of checking all possible matching results.

Sub Routes: are auxiliary views on the page, such as if we wanted to add a share component, without taking us or rendering a new page.

Using Links/Routes/Switches/Redirects allows us to create quick links and pass information to our components.
Allow us to ensure that users can't access incorrect web pages
Allows us to redirect users if there are errors

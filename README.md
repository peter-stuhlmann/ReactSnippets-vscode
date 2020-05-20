# Useful React Snippets (Visual Studio Code Extension)

![Release](https://img.shields.io/github/v/release/peter-stuhlmann/ReactSnippets-vscode)
[![MIT License](https://img.shields.io/github/license/peter-stuhlmann/ReactSnippets-vscode.svg)](https://github.com/peter-stuhlmann/ReactSnippets-vscode/blob/master/LICENSE)
![Code size](https://img.shields.io/github/languages/code-size/peter-stuhlmann/ReactSnippets-vscode.svg)
![open issues](https://img.shields.io/github/issues/peter-stuhlmann/ReactSnippets-vscode.svg)
![closed issues](https://img.shields.io/github/issues-closed/peter-stuhlmann/ReactSnippets-vscode.svg)

---

## Download

You can [download the extension](https://marketplace.visualstudio.com/items?itemName=peter-stuhlmann.react-snippets) from the Visual Studio Marketplace.

## Snippets

Below is a list of all available snippets and the Shortcodes of each one.

### Brief overview

|   Shortcodes | Description                                                  |
| -----------: | ------------------------------------------------------------ |
|      `class` | class component                                              |
|     `iclass` | class component with import of React, Component and Fragment |
|   `function` | functional component                                         |
|  `ifunction` | functional component with import of React and Fragment       |
|      `const` | const (arrow function)                                       |
|     `iconst` | const (arrow function) with import of React and Fragment     |
|    `context` | context provider                                             |
|     `router` | router                                                       |
| `lazyrouter` | router with lazy loaded components                           |

### Generated code snipptes

#### `class` - class component

```javascript
| class | extends Component {
  render() {
    return (
      <Fragment>Lorem ipsum</Fragment>
    );
  }
}
```

#### `iclass` - class component with import of React, Component and Fragment

```javascript
import React, { Component, Fragment } from 'react';

| class | extends Component {
  render() {
    return (
      <Fragment>Lorem ipsum</Fragment>
    );
  }
}
```

#### `function` - functional component

```javascript
| function |() {
  return (
    <Fragment>Lorem ipsum</Fragment>
  )
}
```

#### `ifunction` - functional component with import of React and Fragment

```javascript
import React, { Fragment } from 'react';

| function |() {
  return (
    <Fragment>Lorem ipsum</Fragment>
  )
}
```

#### `const` - const (arrow function)

```javascript
| const | = (props) => {
  return (
    <Fragment>Lorem ipsum</Fragment>
  );
};
```

#### `iconst` - const (arrow function) with import of React and Fragment

```javascript
import React, { Fragment } from 'react';

| const | = (props) => {
  return (
    <Fragment>Lorem ipsum</Fragment>
  );
};
```

#### `context` - context provider

```javascript
import React, { createContext, useState } from 'react';

const Context| = createContext(null);

export default function ContextProvider|({ children }) {
  const [count, setCount] = useState(0);

  return (
    <Context|.Provider
      value={{
        count,
        setCount,
      }}
    >
      {children}
    </Context|.Provider>
  );
}

// Don't forget this: Wrap your app in the context provider, like in the example:
//   <ContextProvider|>
//     <App />
//   </ContextProvider|>
```

#### `router` - router

```javascript
import React from 'react';
import { Switch, Route, Redirect } from 'react-router-dom';

import | from './|';

export default function Router() {
  return (
    <Switch>
      <Route exact path="|" component={|} />
      <Route exact path="/redirect" render={() => <Redirect to="|" />} />
    </Switch>
  );
}
```

#### `lazyrouter` - router with lazy loaded components

```javascript
import React, { Suspense, lazy } from 'react';
import { Switch, Route, Redirect } from 'react-router-dom';

const | = lazy(() => import('./|'));

export default function Router() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <Switch>
        <Route exact path="|" component={|} />
        <Route exact path="/redirect" render={() => <Redirect to="|" />} />
      </Switch>
    </Suspense>
  );
}
```

## License

Licensed under the [MIT License](https://github.com/peter-stuhlmann/ReactSnippets-vscode/blob/master/LICENSE) by [Peter R. Stuhlmann](https://peter-stuhlmann-webentwicklung.de).

# use-guarded-context

> useContext with fail-fast assertion. Tests if provider is mounted and throws an error if not

[![NPM](https://img.shields.io/npm/v/use-guarded-context.svg)](https://www.npmjs.com/package/use-guarded-context) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save use-guarded-context
```

## Usage

```tsx
import React, { Component } from 'react'

import MyComponent from 'use-guarded-context'
import 'use-guarded-context/dist/index.css'

class Example extends Component {
  render() {
    return <MyComponent />
  }
}
```

## License

MIT © [kardysm](https://github.com/kardysm)

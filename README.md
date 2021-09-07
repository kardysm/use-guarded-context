# use-guarded-context
useContext with fail-fast assertion. Tests if provider is mounted and throws an error if not

## How it works?

Hook uses `useContext` under the hood. It enhances original one with assertion - checks if value is other than `undefined` .

What for?

See example:

## Example
```typescript jsx
interface ProviderValue{
  someValue: unknown
}
// default value is undefined to fail fast 
// rather than spend hours on debugging
const ExampleContext = React.createContext<ProviderValue | undefined>(undefined)

//...

const Component = () => {
  // regularValue: ProviderValue | undefined 
  // you have to guard it by yourself
  const regularValue = useContext(ExampleContext)
 
  // safeValue: ProviderValue, 
  // safe to use
  const safeValue = useGuardedContext(ExampleContext)
  
  //...
}

```

## Installation
``` bash
npm install use-guarded-context
//or
yarn add use-guarded-context
```

## Usage

``` typescript
    import {useGuardedContext} from 'use-guarded-context'
    
    //in component
    const yourContextValue = useGuardedContext(YourContext) 
```

If provider is not mounted anywhere above, error is thrown:
```
`Provider for context ${context.displayName} is not mounted`
```

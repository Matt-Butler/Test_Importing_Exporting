# Test_Importing_Exporting

Demonstration on when exporting multiple objects from a module that you still import all of the code.

# Install
```
npm install
```

# Build
```
npm run compile
```

# Example 1
```
npm run example_1
```

Example of importing using this syntax:
```
import { print_a } from './print';
```
Notice how it imports **print_a**, **print_b**, and **print_c**

# Example 2
```
npm run example_2
```

Example of importing using this syntax:
```
import print_a from './print_a';
```
Notice how it only imports **print_a**

# **Takeaway**

**Don't do this:**
Import from a file that exports several files:
```js
export { default as print_a } from './print_a';
export { default as print_b } from './print_b';
export { default as print_c } from './print_c';
```

```js
import print_a from './print';
```

**Do this:**
Import directly from the file:
```js
const print_a = console.log('print_a');
export default print_a;
```

```
import print_a from './print_a';
```

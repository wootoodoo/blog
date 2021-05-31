# blog
## How to add a new action

In order to extend a new action to the code, simply place the new code within the /src/actions folder, and add these additional lines of code to the switch statement in **index.js**.

```
case 'NEW_ACTION':
  res = require('./actions/NEW_ACTION')(args);
  break;
```

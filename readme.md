```
cd fastboot-test
yarn
ember b
node server.js
```

Navigates to http://0.0.0.0:4000/google

This works because we are require'ing from a level up 
https://github.com/ember-fastboot/fastboot/blob/v1.2.0/src/ember-app.js#L130

```
cd server
yarn
node server.js
```
You will see something like
> Error: Cannot find module 'abortcontroller-polyfill/dist/cjs-ponyfill'

If you put a `console.log` at `fbtest/server/node_modules/fastboot/src/ember-app.js`

The path is `... fbtest/fastboot-test/dist/node_modules/abortcontroller-polyfill/dist/cjs-ponyfill`

# package.json

We could spend hours on tools that are centered around `package.json`.  It's just a tiny little file, but there are many useful utilties built around it.

Let's talk about some of the most common you're bound to see in the wild.

## devDependencies
Remember how we installed packages to our `package.json` using `--save`?  Consider when your pacakge may require tooling to support development or quality?  For example, a _testing utility_ would be useful.  Let's install `tape`, a popular "Test Anything Protocol" utility.

- run `npm i --save-dev tape`

`tape` is now installed into your `node_modules/`, just like normal.  However, there is a key difference.  Inspect your `package.json` for `devDependencies`.  Here, `tape` is listed.  **The significance** is that when your package is used as a dependent package of another package, the `devDependencies` will _not_ be installed.  This shrinks the size of your package, sometimes significantly, for consumers of it.  This results in faster download times, faster install times, and a clear list of dependencies that your program _really_ needs in order to run.

## scripts
`npm` has many handy built in scripts.  Let's generate some.

Edit your pacakge.json to include a `"start"` entry and a "demo" entry:
```json
...
  "scripts": {
    "start": "node index.js just-demoing",
    "test": "echo \"Error: no test specified\" && exit 1",
    "demo": "npm start"
  },
...
```

Great.  Run `npm start`.  Check it out!  It ran your script. [npm scripts](https://docs.npmjs.com/misc/scripts) provide a task-runner like interface.  You can get really wild with some of these, and even add configuration variables, which is super handy and fun.

What about the "test" script?

Run `npm test`.  No surprises here.  What if we added a real test though?

```js
// test.js
var test = require('tape');
var mypackage = require('./index.js'); // or just require('./')
test('test rainbow-ness', function (t) {
    t.ok(true, 'insert real test, will ya?');
    t.end();
});
```

Then updated `"test"` from `"echo \"Error: no test specified\" && exit 1"` to "node test.js".

Run `npm test` again!  This is a real process that exits when things fail with bad exit codes, so if you wanted to build a big program with a build step, yet cancel the build if the tests failed, this becomes very easy to do!

Finally, let's look at the "demo" script.  What happens if you run `npm demo`?  Uh oh, it errors out!  Some scripts, like `start` and `test` are reserved.  No worries.  For most custom scripts you make, simply add a `run` in the middle.

Run `npm run demo`.  Well look at that!  Demo _ran_ your _start_ script!  Pretty fancy stuff!

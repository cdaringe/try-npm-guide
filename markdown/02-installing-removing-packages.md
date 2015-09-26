# installing packages

npm hosts _drillions_, even _ba-gillions_, of useful packages.  Let's jump on [npmjs.com](http://www.npmjs.com) and search for a package called "colors.""

When I searched for colors, I immediately found the [colors](https://www.npmjs.com/package/colors) package.  By peering over the documentation, it seems like this package can help us a great deal as we write our program.

To install it, run the command `npm install --save colors`.  This installs the colors package _to the current project_.  More accurately, it installs `colors` to the current project if it has a package.json, or, npm will traverse up your folder tree to the nearest folder that contains a package.json and install it there.

Two things to notice:

1. Run a `ls` to see the current directory.  Do you see the `node_modules` folder?  This is where project packages are installed.
1. Open up your package.json file.  Do you see `dependencies` section?  Here, you will see `colors@some-version`.  npm supports [semver versioning](https://docs.npmjs.com/files/package.json#version).  Don't worry if you're not familiar with it now.  It will be easy to pick up with practice.

<br>
There are _more_ ways to install packages.  Let's learn one more.  Shall we add `lodash.map` to our package?  I think we shall!  Go ahead and add it to your `package.json` as shown below:

```json
"dependencies": {
  "colors": "^1.1.2",
  "lodash.map": "latest"
}
```

<br>
Now, run `npm i` (shorthand for `npm install`).  Look at that!  You've now installed two packages in two different ways!

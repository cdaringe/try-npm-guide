# installing packages

npm hosts _drillions_, even _ba-gillions_, of useful packages.  Let's jump on [npmjs.com](http://www.npmjs.com) and search for _colors_.

When I searched for _colors_, I immediately found the [colors](https://www.npmjs.com/package/colors) package.  It looks like this will help us a great deal.

To install it, run the command `npm install --save colors`.  This installs your package _to the current project_.  More accurately, it install `colors` to the current folder if it has a package.json, or up your folder tree to the nearest folder that contains a package.json.

Two things to notice:

1. Run a `ls` to see the current directory.  Do you see the `node_modules` folder?  This is where project packages are installed.
1. Open up your package.json file.  Do you see `dependencies` section?  Here, you will see `colors@some-version`.  npm supports [semver versioning](https://docs.npmjs.com/files/package.json#version).  Don't worry if you're not familiar with it now.  It will be easy to pick up with practice.

There are _more_ ways to install packages, such as simply editing your package.json with package names and versions, then running `npm install`, or `npm i` for short.  We won't touch all of those now.  Let's keep moving.

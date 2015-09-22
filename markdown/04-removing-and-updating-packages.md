## removing and updating packages
What if you want to uninstall the colors package?

1. run `npm remove colors`.  you should see a confirmation that the package was remove or unbuilt.
1. check your package.json.  colors is still listed in the dependencies section.  didn't we just remove it?  sure did, but to persist changes to our package.json, remember that we need to couple install/remove commands with a `--save` option.
1. run `npm remove colors --save` and the entry will be removed.

Running our app will now break.  When node tries to find `colors`, nothing will be present.  So, let's reinstall our package.  However, let's pretend that the latest version of `colors` doesn't work with your application.  In many cases, you may want an _older_ version of the package.  By looking at the colors [github releases](https://github.com/Marak/colors.js/releases), we can see that there is a version 1.1.1, and we know that it will work with our app.

1. run `npm i --save colors@1.1.1`

Boom!  Done!  We can `require('colors')` and rest assured that version 1.1.1 will be used in our program.

Note: not all packages use github, nor do packages that do use github necessarily use the releases feature.  many large, popular projects do however, which makes it a handy tool to inspect package history or versions.

Before we move on, let's talk about updating `colors` when we think the module has stablized.  To see if we are outdated, run `npm outdated`.  It shows that we are at `1.1.1`.  The "wanted" field indicated the latest version permitted to install as defined by our package.json's versioning rules.  Looks like we are OK to install the "latest".  If the "latest" begins with a "1.", then we are good to update!

`npm update` will update `colors` to the most-up-to-date version we can.  Try it!

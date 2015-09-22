# global packages
npm let's you install packages globally on your system.  Let's check one out.

Run `sudo npm install -g shrugy`.

Note, your system _may_ not require sudo. [it depends](https://docs.npmjs.com/getting-started/fixing-npm-permissions) on your own preference, or company's preference.

Ok, now that `shrugy` is installed, let's start shrugging.

```bash
$ shrugy     //=> ¯\_(ツ)_/¯
$ shrugy npm //=> ¯\_(npm)_/¯
$ node index.js $(shrugy npm) //=> ¯\_(npm)_/¯ ... but more colorful :)
```

So, using `npm`, we were able to install a program that gets added to our system PATH that we can call from the CLI!  How cool!

Suppose hypothetically that you wanted to _unistall_ `shrugy`.  That would be crazy, because it's clearly amazing, but, you'd simply run:

`npm uninstall -g shrugy`

Ba-da-bing.  You're a global package guru.

# use packages

Let's create a file to use our package, `index.js`.  Paste or type the following code into the file:

```js
var colors = require('colors');
console.log('npm is GREAT'.rainbow);
```

Now, run `node index.js`.  Whoa! You saw <span style='font-weight:bold;'><span style='color:#FF0000;'>n</span><span style='color:#FF7F00;'>p</span><span style='color:#FFFF00;'>m</span> <span style='color:#00FF00;'>i</span><span style='color:#00FF7F;'>s</span> <span style='color:#007FFF;'>G</span><span style='color:#0000FF;'>R</span><span style='color:#7F00FF;'>E</span><span style='color:#FF00FE;'>A</span><span style='color:#FF007F;'>T</span></span>, right? Beautiful!  But you know what we really want?  Let's allow our user to add arguments to the program and make those inputs colorful too.  That is, let's call `node index.js i love rainbows` and get the text <span style='font-weight:bold;'><span style='color:#FF0000;'>i</span> <span style='color:#FFCC00;'>l</span><span style='color:#CBFF00;'>o</span><span style='color:#65FF00;'>v</span><span style='color:#00FF00;'>e</span> <span style='color:#00FFCC;'>r</span><span style='color:#00CBFF;'>a</span><span style='color:#0065FF;'>i</span><span style='color:#0000FF;'>n</span><span style='color:#6500FF;'>b</span><span style='color:#CC00FF;'>o</span><span style='color:#FF00CB;'>w</span><span style='color:#FF0065;'>s</span></span> back.  Try the following code then run `node index.js i love rainbows`.  Don't worry if you don't understand the code.

```js
var colors = require('colors');
var args = process.argv.slice(2);
var colorArgs = args.map(function(arg) {
    return arg.rainbow;
});
console.log(colorArgs.join(' '));
```

Cool.  Now you can clearly see how npm and node work together.

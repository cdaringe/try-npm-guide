# npm init

`npm` comes pre-installed with [nodejs](nodejs.org).  It is, after all, the node-package-manager.

To start a project using npm, you will run `npm init` in your project folder.  This generates a `package.json` file which is your package's definition file.  You will reference `package.json` often!

npm is best learned with an example.  Let's pretend that it's 1990 and you have just bought your very first <span style='font-weight:bold;'><span style='color:#FF0000;'>C</span><span style='color:#CBFF00;'>O</span><span style='color:#00FF66;'>L</span><span style='color:#0065FF;'>O</span><span style='color:#CC00FF;'>R</span></span> monitor  &#128187;.  You never want to look at <span style='font-weight:bold;'><span style='color:#000000;'>BLACK</span></span> or <span style='font-weight:bold;'><span style='color:#00A100;'>GREEN</span></span> text again!  Let's make an app that will take normal text, and output <span style='font-weight:bold;'><span style='color:#FF0000;'>c</span><span style='color:#FFBF00;'>o</span><span style='color:#7FFF00;'>l</span><span style='color:#00FF3F;'>o</span><span style='color:#00FEFF;'>r</span><span style='color:#003FFF;'>f</span><span style='color:#7F00FF;'>u</span><span style='color:#FF00BF;'>l</span></span> text.

1. create a project directory: `mkdir color-time`
1. enter the directory: `cd color-time`
1. run: `npm init`

<br>
This will guide you through an interactive tutorial to auto-generate your `package.json file`.  You can press `enter` through each field for now.  Now that your package is npm ready, let's install some packages!

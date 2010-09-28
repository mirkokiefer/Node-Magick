Node-Magickal - GraphicsMagick wrapper for Node.js
=====

This is a very simple library for async calls to the [GraphicsMagick](http://http://www.graphicsmagick.org/) command line tools.
Its basically a rewrite of [magickal-node](http://github.com/quiiver/magickal-node) to fix a bug and usage of deprecated Node.js functions.

An example:

    var magick = require('./libs/node-magick');
    
    magick
      .createCommand("large_image.JPG")
      .resize(150, 150)
      .write("$HOME/Development/node/examples/output.PNG", function() {
          sys.puts("Done");
      });
Node-Magickal - GraphicsMagick wrapper for Node.js
=====

This is a very simple library for async calls to the [GraphicsMagick](http://http://www.graphicsmagick.org/) command line tools.

An example:

    var magick = require('./libs/node-magick');
    
    magick
      .createCommand("$HOME/Development/node/examples/large_image.JPG")
      .resize(150, 150)
      .write("$HOME/Development/node/examples/output.PNG", function() {
          sys.puts("Done");
      });
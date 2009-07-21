# Recursive Creative Website

This project generates the HTML source for [Recursive Creative's Website](http://recursivecreative.com).

This website is can be built with the [Henrik's version of Jekyll](http://github.com/henrik/jekyll/tree/master)
that adds support for HAML and SASS.

We had to make a small change to the HAML gem in order to get the SASS to compile. In:

  lib/sass/tree/import_node.rb

Change the line:

  paths = (@options[:load_paths] || []).dup

To this:

  paths = (@options[:load_paths] || []).dup.to_a

Hopefully this change won't be necessary in future versions of HAML, but as of 2.2.2 it seems to be.

To generate the website in the output directory, type:

  rake generate

To generate and deploy, type:

  rake deploy


## License

Feel free to reuse any of the scripts and code found on this web site, but note that all content and
images are copyright © 2009, Recursive Creative, LLC. and are not licensed for distribution. If you
have questions about any of this, please get in touch.
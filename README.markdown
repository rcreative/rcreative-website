Recursive Creative Website
--------------------------

This website is can be built with the Henrik's version of Jekyll that adds
support for HAML and SASS:

  http://github.com/henrik/jekyll/tree/master

I had to make a small change to the HAML gem in order to get the SASS to
compile. In:

  lib/sass/tree/import_node.rb

Change the line:

  paths = (@options[:load_paths] || []).dup

To this:

  paths = (@options[:load_paths] || []).dup.to_a

Hopefully this change won't be necessary in future versions of HAML, but as of
2.2.2 it seems to be.

To generate the website in the output directory, type:

  rake generate

To generate and deploy, type:

  rake deploy
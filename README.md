#Hack! Toru Interactive, May 2017

We inherited a site that was remarkably tidy and well written in all ways except for one apparent hack. When we build the site using the existing Gulp build scripts the title on the chart on chapter 2 is displaying on one line and at a too big font size.

Turned out this package had been manually modified to display multiline titles. As Bower components aren't commited to the Git repo this will be a recurring problem for us and anyone else who tries to build the site.

So we made this copy of the nv.d3 repo, reverse engineered the change and applied it here. This package is pulled into the app rather than the actual nv.d3 library. This is not an ideal solution but it's the best that could be done within the scope of the current work. 

##The change

Search `// START CUSTOM TORU INTERACTIVE REWRITE //` and `// END CUSTOM TORU INTERACTIVE REWRITE //` on build/nv.d3.js
This is going to be the web page that'll come up when I log into my BeagleBone Black locally on port 8080.  It's main purpose will be to house BoneScript (js) apps for experimentation with interactive BeagleBone projects.  This will be my first experience with Web Servers (LightTPD), BeagleBone Black, Web Design (Aptana Studio), HTML5, CSS3, JavaScript (BoneScript), or node.js, so it's likely to be fairly clumsy in design and operation as I learn about each of the components.  

UPDATE - I've found that running server-side scripts (which is what the JS/BoneScript apps seem to have to be) requires a server-side JS interpreter.  For this purpose I've created a node.js server to listen in on port 8081, establish WebSocket connections using the ws library, and execute the scripts that the HTML pages on port 8080 ask for.  It also serves as a middle man between the script and the calling web page (which now serves as the user interface for the application being called), passing data from the script to the web page, and vice versa.  

![alt tag](/img/Interoperations_Layout.bmp)


The scripts that this repository calls to are kept in another repo (/BeagleBoneScripts).  I'll be keeping the node server in my autorun directory under /var/lib/cloud9, but will also be adding it to both these repos just for cohesion in tracking.


Any comments or suggestions are, of course, always welcome.



I'm leaving the HTML5 Boilerplate part of the README that Aptana has added as it's free software and seems appropriate to do so.  I don't however claim to have read or understand it   :)


# [HTML5 Boilerplate](http://html5boilerplate.com)

HTML5 Boilerplate is a professional front-end template for building fast,
robust, and adaptable web apps or sites.

This project is the product of many years of iterative development and combined
community knowledge. It does not impose a specific development philosophy or
framework, so you're free to architect your code in the way that you want.

* Source: [https://github.com/h5bp/html5-boilerplate](https://github.com/h5bp/html5-boilerplate)
* Homepage: [http://html5boilerplate.com](http://html5boilerplate.com)
* Twitter: [@h5bp](http://twitter.com/h5bp)


## Quick start

Choose one of the following options:

1. Download the latest stable release from
   [html5boilerplate.com](http://html5boilerplate.com/) or a custom build from
   [Initializr](http://www.initializr.com).
2. Clone the git repo — `git clone
   https://github.com/h5bp/html5-boilerplate.git` - and checkout the tagged
   release you'd like to use.


## Features

* HTML5 ready. Use the new elements with confidence.
* Cross-browser compatible (Chrome, Firefox, IE8+, Opera, Safari).
* Designed with progressive enhancement in mind.
* Includes [Normalize.css](http://necolas.github.com/normalize.css/) for CSS
  normalizations and common bug fixes.
* The latest [jQuery](http://jquery.com/) via CDN, with a local fallback.
* The latest [Modernizr](http://modernizr.com/) build for feature detection.
* Placeholder CSS Media Queries.
* Useful CSS helpers.
* Default print CSS, performance optimized.
* Protection against any stray `console.log` causing JavaScript errors in
  older browsers.
* An optimized Google Analytics snippet.
* Apache server caching, compression, and other configuration defaults for
  Grade-A performance.
* Cross-domain Ajax and Flash.
* "Delete-key friendly." Easy to strip out parts you don't need.
* Extensive inline and accompanying documentation.

[HTML5 Boilerplate v4 provides legacy browser
support](https://github.com/h5bp/html5-boilerplate/tree/v4) (IE 6+, Firefox
3.6+, Safari 4+), but is no longer actively developed.

## Documentation

Take a look at the [documentation table of contents](doc/TOC.md). This
documentation is bundled with the project, which makes it readily available for
offline reading and provides a useful starting point for any documentation you
want to write about your project.


## Contributing

Anyone and everyone is welcome to [contribute](CONTRIBUTING.md). Hundreds of
developers have helped make the HTML5 Boilerplate what it is today.

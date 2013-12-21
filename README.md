This is going to be the web page that'll come up when I log into my BeagleBone Black locally on port 8080.  It's main purpose will be to house BoneScript (js) apps for experimentation with interactive BeagleBone projects.  This will be my first experience with Web Servers (LightTPD), BeagleBone Black, Web Design (Aptana Studio), HTML5, CSS3, JavaScript (BoneScript), or node.js, so it's likely to be fairly clumsy in design and operation as I learn about each of the components.  

UPDATE - I've found that running server-side scripts (which is what the JS/BoneScript apps seem to have to be) requires a server-side JS interpreter.  For this purpose I've created a node.js server to listen in on port 8081, establish WebSocket connections using the ws library, and execute the scripts that the HTML pages on port 8080 ask for.  It also serves as a middle man between the script and the calling web page (which now serves as the user interface for the application being called), passing data from the script to the web page, and vice versa.  

![alt tag](/img/Interoperations_Layout.bmp)


The scripts that this repository calls to are kept in another repo (/b--dub/BeagleBoneScripts).  I'll be keeping the node server in my autorun directory under /var/lib/cloud9 so that it will launch when I boot the Beagle, but will be storing it in the /BeagleBoneScripts repo as I'm writing/updating it in Cloud 9 with the other scripts and this makes it easier to keep everything updated cohesively.




Any comments or suggestions are, of course, always welcome.




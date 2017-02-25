# frontend-nanodegree-mobile-portfolio-master
Cloned from Udacity's [repo](https://github.com/udacity/frontend-nanodegree-mobile-portfolio).

This website was created by Cameron Pittman as a final project for Udacity's course [*__Website Performance Optimization__*](https://www.udacity.com/course/website-performance-optimization--ud884).  It was my task to optimize this site to meet the requirements explained in the [project outline](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Project%20outline.md).

I modified the following files, follow the links to view changes.
* **HTML**
    * [docs/index.html](#docs/index.html)
    * [docs/views/pizza.html]()
    * [docs/project-2048.html]()
    * [docs/project-mobile.html]()
    * [docs/project-webperf.html]()
* **CSS**
    * [docs/css/print.css]()
    * [docs/css/style.css]()
    * [docs/views/css/bootstrap-grid.css]()
    * [docs/views/css/style.css]()
* **JS**
    * [docs/js/perfmatters.js]()
    * [docs/views/js/main.js]()
* **IMAGES**
    * [docs/views/images/pizzeria.jpg]()
    * [docs/views/images/pizza.png]()
    * [docs/img/2048.png]()
    * [docs/img/cam_be_like.jpg]()
    * [docs/img/mobilewebdev.jpg]()
    * [docs/img/profilepic.jpg]()

<br></br>
The next section briefly describes the changes I made to each file and the reasoning behind each change.
<br></br>

<a id="docs/index.html"></a>

## Changes to **docs/index.html**
* [inlined style.css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b162585ce944eee45d1ccf2c05645263939443c) to head section of index.html file to prevent render blocking.
* [added class attributes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/ac71d65e25e245c2ee2474656749f7589668fde0) to html elements and [modified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/559d16d0fd21539e21087b8f92dc5c2c570c7bc8) to reference classes instead of tags to improve render time.
* [minified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/60b3f8b28c99db25f823cca20793b0a4ee905877) to reduce file size.
* [removed and refactored css styles](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/689c0c6a536943536f09fb785fef12b3fa61fd5d) from inlined style.css not pertinate to index.html to reduce file size.
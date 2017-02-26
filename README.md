# frontend-nanodegree-mobile-portfolio-master
Cloned from Udacity's [repo](https://github.com/udacity/frontend-nanodegree-mobile-portfolio).

This website was created by Cameron Pittman as a final project for Udacity's course [*__Website Performance Optimization__*](https://www.udacity.com/course/website-performance-optimization--ud884).&nbsp; It was my task to optimize this site to meet the requirements explained in the [project outline](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Project%20outline.md).

As per the project outline I only needed to improve pagespeed score for `index.html` and achieve 60fps with `pizza.html` but thought, for practice I would improve page speed scores for all the pages in this site.  

I modified the following files, follow the links to view changes.  
* [**HTML**](#html-files)
    * [`docs/index.html`](#docs/index.html)
    * [`docs/views/pizza.html`](#docs/views/pizza.html)
    * [`docs/project-2048.html`](#docs/project-2048.html)
    * [`docs/project-mobile.html`](#docs/project-mobile.html)
    * [`docs/project-webperf.html`](#docs/project-webperf.html)
* [**CSS**](#css-files)
    * [`docs/css/print.css`](#docs/css/print.css)
    * [`docs/css/style.css`](#docs/css/style.css)
    * [`docs/views/css/bootstrap-grid.css`](#docs/views/css/bootstrap-grid.css)
    * [`docs/views/css/style.css`](#docs/views/css/style.css)
* [**JS**](#js-files)
    * [`docs/js/perfmatters.js`](#docs/js/perfmatters.js)
    * [`docs/views/js/main.js`](#docs/views/js/main.js)
* [**IMAGES**](#image-files)
    * [`docs/views/images/pizzeria.jpg`](#docs/views/images/pizzeria.jpg)
    * [`docs/views/images/pizza.png`](#docs/views/images/pizza.png)
    * [`docs/img/2048.png`](#docs/img/2048.png)
    * [`docs/img/cam_be_like.jpg`](#docs/img/cam_be_like.jpg)
    * [`docs/img/mobilewebdev.jpg`](#docs/img/mobilewebdev.jpg)
    * [`docs/img/profilepic.jpg`](#docs/img/profilepic.jpg)
* [**FINAL RESULTS**](#final-results)
    * [pagespeed scores](#final-pagespeed-scores)

<br></br>
The next section briefly describes the changes I made to each file, the reasoning behind each change and has links to the corresponding commits.
<br></br>
<a id="html-files"></a>
# Changes made to the HTML files

<a id="docs/index.html"></a>

## [`docs/index.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/index.html)
* [removed link to google fonts](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/4e66acc5be123eab68b02f9ff4dce4396a520f39) to increase page load speed by reducing the number of critical assets.
   
* [added media print attribute](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b5166d91ed607a43e176f38cb4279960154fc04) to `print.css` so browser only loads this file @ print request.
    
* [inlined `style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b162585ce944eee45d1ccf2c05645263939443c) to head section of `index.html` file to prevent render blocking.
    
* [added class attributes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/ac71d65e25e245c2ee2474656749f7589668fde0) to html elements and [modified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/559d16d0fd21539e21087b8f92dc5c2c570c7bc8) to reference classes instead of tags to improve render time.

* [refactored and removed css styles](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/689c0c6a536943536f09fb785fef12b3fa61fd5d) from inlined `style.css` not pertinate to `index.html` to reduce file size.
    
* [minified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/60b3f8b28c99db25f823cca20793b0a4ee905877) to reduce file size.
    
* moved small screen media css from style.css to a new file `small-screen.css` and [added media max-width attribute to link tag](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/22090fe4bd832fe426d81d33262230208528ef24) so browser only loads this if screen width is less than 481px, this improves above the fold load.
    
* [removed the list item img tags](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/25961ba23b95a10309cb00c7a60acfed768db222) and replaced them with divs with ids for reference.&nbsp; Added corresponding css attributes for background images to inlined css.&nbsp; This improves the above the fold load.
    
* [added async attribute]() to `analytics.js` to prevent render blocking.
   
* added links to top of head to [preload image files](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/82230f27fe775a4e131b128636d8bb899e251243).&nbsp; This makes use browser idle time.

* finally, [minified file]() to decrease size.

Pagespeed test results before

![Initial pagespeed results screenshot before changes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Results/Pagespeed%20tests/index/initial/index-initial.png)

Pagespeed test results after

![Initial pagespeed results screenshot after changes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Results/Pagespeed%20tests/index/initial/index-initial.png)
  

<a id="docs/views/pizza.html"></a>

## [`docs/views/pizza.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/pizza.html)

* [inlined css from `style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/17cead1bc33fcd179e361132569e6e7da289998b) to decrease critical assets.

* [moved `bootstrap.css` link](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/7ea9b897473a3b960823d47f075fd497f7e6469c) to just above body closing tag and [added preload](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/13c014422b43b9c5deecf4e6210e7d0839036738) just after head tag opening.

* [minified `bootstap.css` and `main.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/6318964afbc7a9b5730cee1ae3ce0c5a27acb319) to decrease file sizes.

* finally, [minified `pizza.html`]() to decrease file size.

<a id="docs/project-2048.html"></a>

## [`docs/project-2048.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/project-2048.html)

* 
* 
* finally, [minified file]() to decrease size.

<a id="docs/project-mobile.html"></a>

## [`docs/project-mobile.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/project-mobile.html)

* 
* 
* finally, [minified file]() to decrease size.

<a id="docs/project-webperf.html"></a>

## [`docs/project-webperf.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/project-webperf.html)

* 
* 
* finally, [minified file]() to decrease size. 

<br></br>
<a id="css-files"></a>
# Changes made to the CSS files

<a id="docs/css/print.css"></a>

## [`docs/css/print.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/css/print.css)

* 
* 
* finally, [minified file]() to decrease size. 

<a id="docs/css/style.css"></a>

## [`docs/css/style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/css/style.css)

* [inlined style.css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b162585ce944eee45d1ccf2c05645263939443c) to head section of index.html file to prevent render blocking.
* [added class attributes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/ac71d65e25e245c2ee2474656749f7589668fde0) to html elements and [modified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/559d16d0fd21539e21087b8f92dc5c2c570c7bc8) to reference classes instead of tags to improve render time.
* [refactored and removed css styles](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/689c0c6a536943536f09fb785fef12b3fa61fd5d) from inlined style.css not pertinate to index.html to reduce file size.
* moved small screen media css from style.css to a new file *small-screen.css* and [added media max-width attribute to link tag](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/22090fe4bd832fe426d81d33262230208528ef24) so browser only loads this if screen width is less than 481px, this improves above the fold load.
* removed the list item img tags for index.html and replaced them with divs with ids for reference.&nbsp; [Added corresponding css attributes for background images](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/25961ba23b95a10309cb00c7a60acfed768db222) to inlined css.&nbsp; This improves the above the fold load.

<a id="docs/views/css/bootstrap-grid.css"></a>

## [`docs/views/css/bootstrap-grid.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/css/bootstrap-grid.css)

* 
* 
* finally, [minified file]() to decrease size.

<a id="docs/views/css/style.css"></a>

## [`docs/views/css/style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/css/style.css)

* 
* 
* 

<br></br>
<a id="js-files"></a>
# Changes made to the JS files

<a id="docs/js/perfmatters.js"></a>

## [`docs/js/perfmatters.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/js/perfmatters.js)

* 
* 
* finally, [minified file]() to decrease size.


<a id="docs/views/js/main.js"></a>

## [`docs/views/js/main.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/js/main.js)

* 
* 
* finally, [minified file]() to decrease size. 

<br></br>
<a id="image-files"></a>
# Changes made to the IMAGE files

<a id="docs/views/images/pizzeria.jpg"></a>

## [`docs/views/images/pizzeria.jpg`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/images/pizzeria.jpg)

* 
* 
* 

<a id="docs/views/images/pizza.png"></a>

## [`docs/views/images/pizza.png`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/images/pizza.png)

* 
* 
* 

<a id="docs/img/2048.png"></a>

## [`docs/img/2048.png`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/img/2048.png)

* 
* 
* 

<a id="docs/img/cam_be_like.jpg"></a>

## [`docs/img/cam_be_like.jpg`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/img/cam_be_like.jpg)

* 
* 
* 

<a id="docs/img/mobilewebdev.jpg"></a>

## [`docs/img/mobilewebdev.jpg`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/img/mobilewebdev.jpg)

* 
* 
* 

<a id="docs/img/profilepic.jpg"></a>

## [`docs/img/profilepic.jpg`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/img/profilepic.jpg)

* 
* 
* 

<a id="final-results"></a>

<br></br>
# My Final Results

## Pagespeed scores
I managed to do quite well with the pagespeed scores for index.html at **95%-desktop**(*passing 9 of 10 tests*) and **93%-mobile**(*passing 9 of 10 tests*).&nbsp; The only thing keeping me from achieving 100% and passing all 10 tests is the fact I was unable to utilize browser caching.&nbsp; As far as I understand from my research is that github does not offer this feature when hosting your pages/site with them.&nbsp; Since I am using their services and have no control over the backend I was unable to achieve the oh so desirable 100% :smiley:

<a id="final-pagespeed-scores"></a>
### Final pagespeed scores

### **`index.html`**
* **Before** Optimization
    * *[pagespeed insights](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Results/Pagespeed%20tests/index/initial/index-initial.png)*
    * *[timeline](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Results/Timelines/index/screenshots/Initial.png)*
* **After** Optimization
    * *[pagespeed insights](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fgo-0100-it.github.io%2Ffrontend-nanodegree-mobile-portfolio-master%2F)*
    * *[timeline]()*
### **`pizza.html`**
* **Before** Optimization
    * *[pagespeed insights]()*
    * *[timeline]()*
* **After** Optimization
    * *[pagespeed insights](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fgo-0100-it.github.io%2Ffrontend-nanodegree-mobile-portfolio-master%2Fviews%2Fpizza.min.html&tab=desktop)*
    * *[timeline]()*
### **`project-2048.html`**
* **Before** Optimization
    * *[pagespeed insights]()*
    * *[timeline]()*
* **After** Optimization
    * *[pagespeed insights](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fgo-0100-it.github.io%2Ffrontend-nanodegree-mobile-portfolio-master%2Fproject-2048.html&tab=desktop)*
    * *[timeline]()*
### **`project-mobile.html`**
* **Before** Optimization
    * *[pagespeed insights]()*
    * *[timeline]()*
* **After** Optimization
    * *[pagespeed insights]()*
    * *[timeline]()*
### **`project-webperf.html`**
* **Before** Optimization
    * *[pagespeed insights]()*
    * *[timeline]()*
* **After** Optimization
    * *[pagespeed insights]()*
    * *[timeline]()*
<hr></hr>

## 60 Frames Per Second(fps)
More to say about this soon.
### View optimized pages
* [`Pizza.html`](https://go-0100-it.github.io/frontend-nanodegree-mobile-portfolio-master/views/pizza.min.html)
* [Final Optimized site](https://go-0100-it.github.io/frontend-nanodegree-mobile-portfolio-master/)


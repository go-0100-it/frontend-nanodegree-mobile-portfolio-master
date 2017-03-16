<a id="top"></a>
# frontend-nanodegree-mobile-portfolio-master
Cloned from Udacity's [repo](https://github.com/udacity/frontend-nanodegree-mobile-portfolio "Click to open repo page").

This website was created by Cameron Pittman as a final project for Udacity's course [*__Website Performance Optimization__*](https://www.udacity.com/course/website-performance-optimization--ud884 "Click to open website").&nbsp; It was my task to optimize this site to meet the requirements explained in the [project outline](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/Project%20outline.md).

As per the project outline, I needed to improve the pagespeed score of the `index.html` page and achieve 60fps with the `pizza.html` page. Below you will find a list of all the files I changed, details of the changes I made and the corresponding results. To get and run this application see [here](#run-application "Go to run application section").


I modified the following files, follow the links to view changes.
* [**HTML**](#html-files "Go to HTML section")
    * [`docs/index.html`](#docs/index.html "Go to index.html section")
    * [`docs/views/pizza.html`](#docs/views/pizza.html "Go to pizza.html section")
* [**CSS**](#css-files "Go to CSS section")
    * [`docs/css/print.css`](#docs/css/print.css "Go to print.css section")
    * [`docs/css/style.css`](#docs/css/style.css "Go to style.css section")
* [**JS**](#js-files "Go to JS section")
    * [`docs/js/perfmatters.js`](#docs/js/perfmatters.js "Go to perfmatters.js section")
    * [`docs/views/js/main.js`](#docs/views/js/main.js "Go to main.js section")
* [**FINAL RESULTS**](#final-results "Go to RESULTS section")
    * [pagespeed scores](#final-pagespeed-scores "Go to pagespeed scores section")

<br></br>

<hr></hr>

This section briefly describes the changes I made to each file, the reasoning behind each change and has links to the corresponding commits.
<br></br>

<a id="html-files"></a>
# Changes made to the HTML files   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

<a id="docs/index.html"></a>

## [`docs/index.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/28204c082b2dc8ed8b92b53b04eae4453fd60b13/docs/index.html "View final version of index.html") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")
* [removed link to google fonts](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/4e66acc5be123eab68b02f9ff4dce4396a520f39 "View commit for changes made") to increase page load speed by reducing the number of critical assets.
   
* [added media print attribute](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b5166d91ed607a43e176f38cb4279960154fc04 "View commit for changes made") to `print.css` so browser only loads this file @ print request.
    
* [inlined `style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b162585ce944eee45d1ccf2c05645263939443c "View commit for changes made") to head section of `index.html` file to prevent render blocking.
    
* [added class attributes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/ac71d65e25e245c2ee2474656749f7589668fde0 "View commit for changes made") to html elements and [modified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/559d16d0fd21539e21087b8f92dc5c2c570c7bc8 "View commit for changes made") to reference classes instead of tags to improve render time.

* [refactored and removed css styles](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/689c0c6a536943536f09fb785fef12b3fa61fd5d "View commit for changes made") from inlined `style.css` not pertinate to `index.html` to reduce file size.
    
* [minified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/60b3f8b28c99db25f823cca20793b0a4ee905877 "View commit for changes made") to reduce file size.
    
* moved small screen media css from style.css to a new file `small-screen.css` and [added media max-width attribute to link tag](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/22090fe4bd832fe426d81d33262230208528ef24 "View commit for changes made") so browser only loads this if screen width is less than 481px, this improves above the fold load.

* downloaded and added `project-2048.jpg`, `project-mobile.jpg`, and `project-webperf.jpg` locally so I could optimize them.

* optimized images to drasticly reduce file size, I used the optimized images supplied by the [pagespeed insights page](https://developers.google.com/speed/pagespeed/insights "Link to pagespeed insights page") after running the pagespeed test.
    
* [removed the list item img tags](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/25961ba23b95a10309cb00c7a60acfed768db222 "View commit for changes made") and replaced them with divs with ids for reference.&nbsp; Added corresponding css attributes for background images to inlined css.&nbsp; This improves the above the fold load.
    
* [added async attribute]( "View commit for changes made") to `analytics.js` to prevent render blocking.
   
* added links to top of head to [preload image files](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/82230f27fe775a4e131b128636d8bb899e251243 "View commit for changes made").&nbsp; This makes use browser idle time.

* finally, [minified file](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/0babffb47e81a5e9f414bac067274e0b421d860f "View commit for changes made") to decrease size.
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/f3f05b14be42f78e022e76c87a53f285bf367fbb/doc-dev/index.html "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/f10e2a687f440dbb9e4e72111c65632329eaf359/index.html "View original version of code") - Udacity's repo
<br></br>
<br></br>
<hr>
<a id="docs/views/pizza.html"></a>

## [`docs/views/pizza.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/fb87f92e69607065153d8e7015dabc31eaefdcb7/docs/views/pizza.min.html "View final version of pizza.html") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* [inlined css from `style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/17cead1bc33fcd179e361132569e6e7da289998b "View commit for changes made") to decrease critical assets.

* [moved `bootstrap.css` link](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/7ea9b897473a3b960823d47f075fd497f7e6469c "View commit for changes made") to just above body closing tag and [added preload](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/13c014422b43b9c5deecf4e6210e7d0839036738 "View commit for changes made") just after head tag opening.

* added link to top of head section [preloading `main.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/1ad93946a398c39dc1c1c8f80cbcc0d9694eb0db#diff-11c9c8918fc38e223f20c608dd885d75).

* [minified `bootstrap-grid.css` and `main.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/6318964afbc7a9b5730cee1ae3ce0c5a27acb319 "View commit for changes made") to decrease file size.

* finally, [minified `pizza.html`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/fb87f92e69607065153d8e7015dabc31eaefdcb7 "View commit for changes made") to decrease file size.
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/doc-dev/views/pizza.html "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/3cb2c3a24e9595f4edbce11f4e5c3d878880ea00/views/pizza.html "View original version of code") - Udacity's repo
<br></br>
<br></br>
<hr>

<a id="css-files"></a>

# Changes made to the CSS files &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

<a id="docs/css/print.css"></a>

## [`docs/css/print.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/218417e008a546073a3987f5ca19cb144cdad696/docs/css/print.min.css "View final version of print.css") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* [added media print attribute](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b5166d91ed607a43e176f38cb4279960154fc04 "View commit for changes made") to `print.css` in `index.html` so the browser only loads this file @ print request.

* finally, minified file to decrease size.
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/20c6e1c72bcaa10cd33487bf9b4f56ebf9d5ee09/doc-dev/css/print.css "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/f30680be45f3334287f39461fe7e942f163e17e5/css/print.css "View original version of code") - Udacity's repo
<br></br>
<br></br>
<hr>
<a id="docs/css/style.css"></a>

## [`docs/css/style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/28204c082b2dc8ed8b92b53b04eae4453fd60b13/docs/index.html "View final version of style.css") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* [inlined style.css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/8b162585ce944eee45d1ccf2c05645263939443c "View commit for changes made") to head section of index.html file to prevent render blocking.

* [added class attributes](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/ac71d65e25e245c2ee2474656749f7589668fde0 "View commit for changes made") to html elements and [modified css](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/559d16d0fd21539e21087b8f92dc5c2c570c7bc8 "View commit for changes made") to reference classes instead of tags to improve render time.

* [refactored and removed css styles](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/689c0c6a536943536f09fb785fef12b3fa61fd5d "View commit for changes made") from inlined style.css not pertinate to index.html to reduce file size.

* moved small screen media css from style.css to a new file *small-screen.css* and [added media max-width attribute to link tag](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/22090fe4bd832fe426d81d33262230208528ef24 "View commit for changes made") so browser only loads this if screen width is less than 481px, this improves above the fold load.

* removed the list item img tags for index.html and replaced them with divs with ids for reference.&nbsp; [Added corresponding css attributes for background images](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/25961ba23b95a10309cb00c7a60acfed768db222 "View commit for changes made") to inlined css.&nbsp; This improves the above the fold load.
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/f3f05b14be42f78e022e76c87a53f285bf367fbb/doc-dev/index.html "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/f30680be45f3334287f39461fe7e942f163e17e5/views/css/style.css "View original version of code") - Udacity's repo
<br></br>
<br></br>
<hr>
<a id="docs/views/css/bootstrap-grid.css"></a>

## [`docs/views/css/bootstrap-grid.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/views/css/bootstrap-grid.css "View final version of bootstrap-grid.css") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* minified file to decrease size.

<br></br>
<hr>
<a id="docs/views/css/style.css"></a>

## [`docs/views/css/style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/4c3952aa1ee93b8248beff00bf2d2619009fd80d/docs/views/pizza.min.html "View final version of style.css") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* added  ` will-change:left;` and `backface-visibility:hidden;` to allow the browser the option to render the elements on a different layer.

* removed styles not used by `pizza.html` and minified file to decrease size.

* [inlined `style.css`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/17cead1bc33fcd179e361132569e6e7da289998b "View commit for changes made") into head section of `pizza.html` to reduce the number of critical resources.
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/7110139a4fe0d035a0075ba14bb4ea2f2094ad8d/doc-dev/views/pizza.html "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/f30680be45f3334287f39461fe7e942f163e17e5/views/css/style.css "View original version of code") - Udacity's repo
<br></br>
<br></br>
<a id="js-files"></a>

# Changes made to the JS files &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

<a id="docs/js/perfmatters.js"></a>

## [`docs/js/perfmatters.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/docs/js/perfmatters.min.js "View final version of perfmatters.js") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* [minified file](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/41042db21a2300bc1261b5916a9ea258f9ba14c9 "View commit for changes made") to decrease size.
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/master/doc-dev/js/perfmatters.js "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/f30680be45f3334287f39461fe7e942f163e17e5/js/perfmatters.js "View original version of code") - Udacity's repo
<br></br>
<br></br>
<hr>
<a id="docs/views/js/main.js"></a>

## [`docs/views/js/main.js`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/df3a4aa8f7c2d6fb4605ef1fc4a33146c07a16cf/docs/views/js/main.min.js "View final version of main.js") &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

* [removed the function `determineDx()`](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/663648e4965a4eecbb25b32cdd00ac3dbc8c8494#diff-535a60179c1ea8a9fb9dfafd7896fb9c "View commit for changes made") as it wasn't necessary or all that useful.

* [replaced](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/5872c8f8986eb9b0ffc40595fad0480ebc0ef39b "View commit for changes made") all `querySelector()` function calls with `getElementsById()`

* [replaced](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/663648e4965a4eecbb25b32cdd00ac3dbc8c8494 "View commit for changes made") all `querySelectorAll()` function calls with `getElementsByClassName()`

* [Pulled the items array value assignment](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/dd3689eb0b43b971dc7a4fe3177bc4c0eee74b81#L512 "View commit for changes made") from the `updatePositions()` function so it is only set once upon page load.

* Removed some work done with-in loops where it wasn't necessary to do the work at every iteration of the loop.

* [Assigned array length to variables](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/dd3689eb0b43b971dc7a4fe3177bc4c0eee74b81 "View commit for changes made") and passed to for loops so the browser isn't calculating this at every iteration of the loop.

* finally, [minified file](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/commit/df3a4aa8f7c2d6fb4605ef1fc4a33146c07a16cf "View commit for changes made") to decrease size. 
<br></br>

[**VIEW DEVELOPER COPY OF OPTIMIZED CODE**](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/blob/2bb80a48e09216304119d3a209f5c2f3248e44cf/doc-dev/views/js/main.js "View developer version of optimized code") - code commented with changes made

[**VIEW ORIGINAL CODE**](https://github.com/udacity/frontend-nanodegree-mobile-portfolio/blob/e3966768910e72aacb542b33610c3883b630766c/views/js/main.js "View original version of code") - Udacity's repo
<br></br>
<br></br>
<a id="final-results"></a>

# My Final Results &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

## Pagespeed scores
I managed to do quite well with the pagespeed scores for `index.html` at **95%-desktop**(*passing 9 of 10 tests*) and **93%-mobile**(*passing 9 of 10 tests*).&nbsp; The only thing keeping me from achieving 100% and passing all 10 tests is the fact I was unable to utilize browser caching.&nbsp; As far as I understand from my research is that github does not offer this feature when hosting your pages/site with them.&nbsp; Since I am using their services and have no control over the backend I was unable to achieve the oh so desirable 100% :smiley:

<a id="final-pagespeed-scores"></a>
### Final pagespeed scores &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

### **`index.html`**
* [**Before**](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fcameronwp.github.io%2Fudportfolio%2Findex.html&tab=mobile "Pagespeed insights score before optimization") Optimization
    
* [**After**](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fgo-0100-it.github.io%2Ffrontend-nanodegree-mobile-portfolio-master%2F&tab=mobile "Pagespeed insights score after optimization") Optimization
    
 <br></br>   
<hr></hr>

## 60 Frames Per Second(fps) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

I was able to achieve what I believe to be satisfactory results. Even though all the fps recorded weren't below 60, the vast majority were.  The fps achieved by the optimized code is drasticly improved from the original.

### **`pizza.html`**
* [**Before**](http://cameronwp.github.io/udportfolio/views/pizza.html "View page before optimizations were implemented") Optimization
    
* [**After**](https://go-0100-it.github.io/frontend-nanodegree-mobile-portfolio-master/views/pizza.min.html "View page after optimizations were implemented") Optimization


<br></br>
<hr></hr>

<a id="run-application"></a>

## To run this application &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [` ^ `](#top "Go to top of page")

1. On the [main repository page](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master "Go to main repository page") click &nbsp;![Clone or download button image](images/clone-download-btn.png)&nbsp; and download the project zip file or you can just click this button &nbsp;[![Download button image](images/download-btn.png)](https://github.com/go-0100-it/frontend-nanodegree-mobile-portfolio-master/archive/master.zip "Download project .zip file")&nbsp; to download the zipped files to your computer.

2. Unzip the file.

3. Browse the project to locate the `index.html` file.

4. Open `index.html` in the browser of your choice.

### Or you can view the [**Final Optimized site**](https://go-0100-it.github.io/frontend-nanodegree-mobile-portfolio-master/).
<br></br>


Modifications made:
----


- Minified all JS files
- Minified all CSS files

Index.html changes:

- Set media print attribute to css/print.css
- Moved Google Analytics script bottom of the page, right before closing body tag
- Set async attribute to http://www.google-analytics.com/analytics.js
- put all css.style in-line
- removed http request to google fonts stylesheet, and replaced with @font-face css rules, which makes direct requests to the woff2 file. It's still an http request, but it saves speed by skipping a step, removes superfluous requests to unnecessary languages (e.g. greek and devanagari),  and page speed insights seems to be fine with it.
- Set pizzeria image source to size adjusted, compressed google+ version

project-2048.html changes

- Moved style.css inline
- Added @font-face rules to directly request web fonts, rthater than going through google webfont stylesheet
- Moved Google Analytics script bottom of the page, right before closing body tag
- Set async attribute to http://www.google-analytics.com/analytics.js and pefmatters.js
- Set print media attribute on print.css
- Set image profile pic source to google+ compressed version
- Set 2048 image to cmpressed local version

project-webperf.html changes

- Set media print attribute to css/print.css
- Added @font-face rules to directly request web fonts, rthater than going through google webfont stylesheet
- Moved Google Analytics script bottom of the page, right before closing body tag
- Set async attribute to http://www.google-analytics.com/analytics.js and pefmatters.js
- Set print media attribute on print.css
- Set image profile pic source to google+ compressed version
- Set cam_be_like image to cmpressed local version

project-mobil.html changes

- Set media print attribute to css/print.css
- Added @font-face rules to directly request web fonts, rthater than going through google webfont stylesheet
- Moved Google Analytics script bottom of the page, right before closing body tag
- Set async attribute to http://www.google-analytics.com/analytics.js and pefmatters.js
- Set print media attribute on print.css
- Set image profile pic source to google+ compressed version
- Set mobilewebdev image to cmpressed and resized local version

views/main.js changes

- Modified DOM load event listener to only generate the amount of pizzas that the screen will hold, rather than a superfluous 200
- Moved items (.mover class counter) variable outside of scroll event listener, as it only needs to be loaded once - on load.
- Moved pizzaList and pizzasDiv variables outside of their respective loops, as they are constant variables
- Removed dx and newWidth from changePizzaSizes loop and replaced i with 0
- Applied requestAnimationFrame to ron on scroll events, which tracks scroll position, and only requests when there is not already a request initiated.
- Switched to transform rather than style.left (smoother and higher performance)
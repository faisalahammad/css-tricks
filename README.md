# CSS TRICKS AND MAGIG
Here you got all of CSS tricks what I was figuring out on my projects.

### Control Placeholder color
```css
input::-webkit-input-placeholder, textarea::-webkit-input-placeholder {
  color: #fff;
  opacity: 1;
}

input:-moz-placeholder, textarea:-moz-placeholder {
  color: #fff;
  opacity: 1;
}
```
**N.B: Please add your class or id name before selector to work with specific Form.**

---

### Add Custom Social Icons on WordPress Navigation Menu
```css
.class {
  text-indent: -9999px;
  background-image: url(http://link.com);
  background-repeat: no-repeat !important;
  margin-right: 10px !important;
  width: 50px;
}

.class:hover {
  background-color: transparent !important;
}
```
**N.B: Add class on NAV Menu**

---

### Add Caret Icon beside Dropdown menu (Parent li)
```css
.menu li a:after {
  color: #fff !important;
  content: ' ▼' !important;
}

.menu li > a:only-child:after {
  content: '' !important;
}
```
**N.B: Replace your class inside of `menu` **

---

### Make Responsive iframe (CSS Code)
First put your iframe inside of `iframe-container` class then write custom css on your child theme or external css file.

#### Example
```html
<div class="iframe-container">
  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d29192.452902694364!2d90.49141269583086!3d23.852123360864066!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755cbe13e12ca1b%3A0xe440738bb6817d87!2sPurbachal+New+Town!5e0!3m2!1sen!2sbd!4v1485459233926" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
</div>
```
```css
.iframe-container {
  position: relative;
  padding-bottom: 56.25%;
  padding-top: 35px;
  height: 0;
  overflow: hidden;
}
.iframe-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

---

### Make Responsive iframe (via Website)
* Use this site to make responsive -> [Responsive iFrame Generator](http://embedresponsively.com)

### Class Selector Wildcard
```css
div[class^="tocolor-"], div[class*=" tocolor-"] {
    color:red 
}
```
In the place of div you can add any element or remove it altogether, and in the place of class you can add any attribute of the specified element.

* `[class^="tocolor-"]` — starts with "tocolor-".
* `[class*=" tocolor-"]` — contains the substring "tocolor-" occurring directly after a space character.

---

### Make same size/height column
```css
.row {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display:         flex;
  flex-wrap: wrap;
}
.row > [class*='col-'] {
  display: flex;
  flex-direction: column;
}
```
We used css `flexbox` there.

---

### Browser specific CSS

```css
/***** Selector Hacks ******/

/* IE6 and below */
* html #uno  { color: red }
 
/* IE7 */
*:first-child+html #dos { color: red } 
 
/* IE7, FF, Saf, Opera  */
html>body #tres { color: red }
 
/* IE8, FF, Saf, Opera (Everything but IE 6,7) */
html>/**/body #cuatro { color: red }
 
/* Opera 9.27 and below, safari 2 */
html:first-child #cinco { color: red }
 
/* Safari 2-3 */
html[xmlns*=""] body:last-child #seis { color: red }
 
/* safari 3+, chrome 1+, opera9+, ff 3.5+ */
body:nth-of-type(1) #siete { color: red }
 
/* safari 3+, chrome 1+, opera9+, ff 3.5+ */
body:first-of-type #ocho {  color: red }
 
/* saf3+, chrome1+ */
@media screen and (-webkit-min-device-pixel-ratio:0) {
 #diez  { color: red  }
}
 
/* iPhone / mobile webkit */
@media screen and (max-device-width: 480px) {
 #veintiseis { color: red  }
}
 
/* Safari 2 - 3.1 */
html[xmlns*=""]:root #trece  { color: red  }
 
/* Safari 2 - 3.1, Opera 9.25 */
*|html[xmlns*=""] #catorce { color: red  }
 
/* Everything but IE6-8 */
:root *> #quince { color: red  }
 
/* IE7 */
*+html #dieciocho {  color: red }
 
/* Firefox only. 1+ */
#veinticuatro,  x:-moz-any-link  { color: red }
 
/* Firefox 3.0+ */
#veinticinco,  x:-moz-any-link, x:default  { color: red  }
 
 
 
/***** Attribute Hacks ******/
 
/* IE6 */
#once { _color: blue }
 
/* IE6, IE7 */
#doce { *color: blue; /* or #color: blue */ }
 
/* Everything but IE6 */
#diecisiete { color/**/: blue }
 
/* IE6, IE7, IE8 */
#diecinueve { color: blue\9; }
 
/* IE7, IE8 */
#veinte { color/*\**/: blue\9; }
 
/* IE6, IE7 -- acts as an !important */
#veintesiete { color: blue !ie; } /* string after ! can be anything */
```

Ref: [CSSTricks.com](https://css-tricks.com/snippets/css/browser-specific-hacks/)

---



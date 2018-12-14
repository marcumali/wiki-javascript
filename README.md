# Web Development Tools- JAVASCRIPT

[MARCUMALI](https://marcumali.github.io) | 
[MAIN](https://github.com/marcumali/wiki) | [HTML](https://github.com/marcumali/wiki-html) | [CSS](https://github.com/marcumali/wiki-css) | [JAVASCRIPT](https://github.com/marcumali/wiki-javascript) | [WORDPRESS](https://github.com/marcumali/wiki-wordpress) | [PHP](https://github.com/marcumali/wiki-php)

Guide and best practice of web development

## JavaScript

* when `.on('click', ... )` is used, allow keydown as well
* put listeners on `.js-classes` and toggle either `aria-attributes` (when present) or classes e.g. `.active`
* if a listener needs to address a certain ID or class pass it as an attribute. Exception may occur when using third party plugins.
* use .on('click', ... ) instead of .click() which is an alias for .trigger('click') that can not handle a _second argument. Additionally, what this means is that there's no way to assign a delegate via .click(...)_

## 1. Check viewport
GLOBAL:
```javascript
var Viewport = {};
Viewport.documentWidth = function(){
  var e = window, a = 'inner';
  if (!('innerWidth' in window )) {
	a = 'client';
	e = document.documentElement || document.body;
  }
  return { width : e[ a+'Width' ] , height : e[ a+'Height' ] };
};
```
USE:
```javascript
if( Viewport.documentWidth().width < 767 ){
	// do something
}
```

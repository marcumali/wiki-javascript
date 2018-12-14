# Web Development Tools- JAVASCRIPT

[MARCUMALI](https://marcumali.github.io) | 
[MAIN](https://github.com/marcumali/wiki) | [HTML](https://github.com/marcumali/wiki-html) | [CSS](https://github.com/marcumali/wiki-css) | [JAVASCRIPT](https://github.com/marcumali/wiki-javascript) | [WORDPRESS](https://github.com/marcumali/wiki-wordpress) | [PHP](https://github.com/marcumali/wiki-php)

Guide and best practice of web development

## Check viewport
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

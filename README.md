# angular-bootstrap-colorpicker

This project is a simple port of [Stefan Petre](http://www.eyecon.ro/)'s
[bootstrap-colorpicker](http://www.eyecon.ro/bootstrap-colorpicker/) library.

## Installation

 1. Copy `css/colorpicker.css`, `img/*.png` and `js/bootstrap-colorpicker.js`
    to the appropriate directories in your project.
 2. Add the code from directive.js to your AngularJS project's directives file

## Usage

After installation, using this directive is simple.

```html
    <a href="" class="btn" colorpicker>Pick a color!</a>
```

Or, if you don't swing that way,

```html
    <colorpicker class="btn">Sup!</colorpicker>
```


## Diff against original library

As of 26th / July / 2012, the only core differences between this library and
Stefan's are as follows in the below diff.

```javascript
>       
330,331d329
<       var initialColor = (arguments[0] == "setColor") ? arguments[1] : null;
< 
333,341c331,332
<           var $this = $(this);
< 
<           $this.each(function() {
<               this.setAttribute("data-color", initialColor);
<           });
< 
<           console.log("Here is the this object", $this);
< 
<           var data = $this.data('colorpicker'),
---
>           var $this = $(this),
>               data = $this.data('colorpicker'),
343d333
< 
347,348c337
< 
<           if (typeof option == 'string' && option != 'setColor') data[option]();
---
>           if (typeof option == 'string') data[option]();
```


# HorizontalScroll
Create automatic div with horizontal scroll view for HTML5 or Intel App Framework

##REQUIRES:
JQuery v1.6 (or newer)

##HOW TO USE IT:
Place HTML code and execute JQuery function


##HTML (MINIMAL) -- For more info, see examples

```HTML
<div class="overflow">
  <div class="containers">
    <div class="each"> </div>
  </div>
</div>
```

##Script (JQuery) 
~~~JAVASCRIPT
/*
*  IMPORT .JS FILE OR COPY THIS FUNCTION
*/
// MAIN FUNCTION
(function ($) {
  $.fn.createHorizontalOverflow = function () {
    var width = 0;
    this.find('.containers').children('div').each(function () {
      width += $(this).outerWidth(true);
    });
    this.find('.containers').css('width', width + "px");
  };
}(jQuery));
// Execute when page is ready
// This can be modify for other porpuses. 
$(document).ready(function () {
  $('div.overflow').createHorizontalOverflow();
});
/*
*  END
*/
~~~

##CSS

~~~CSS
/*
*  IMPORT .CSS FILE OR COPY THIS STYLES
*/
  .overflow {
    width: 100%;
    overflow-x: scroll;
    overflow-y: hidden;
  }
  .overflow::-webkit-scrollbar {
    display: none;
  }
  .overflow .containers .each {
    border: none;
    float: left;
  }
 

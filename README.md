# JSClickEventDisable
JavaScript Disable click event targeted element

```JS

  const RecursiveUnbind = function($jElement) {

    $jElement.unbind();
    $jElement.removeAttr('onclick');
    $jElement.children().each(function () {
        RecursiveUnbind($(this));
    });
  }
  	 
   // PopUpContainer is getting clicked! blocked lightbox * 
    RecursiveUnbind( jQuery('Element') );
 
  // Reference: https://stackoverflow.com/questions/1755815/disable-all-click-events-on-page-javascript
```

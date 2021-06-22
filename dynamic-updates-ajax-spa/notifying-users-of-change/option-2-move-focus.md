# Option 2: Move the focus

## Overview

When new content appears as the direct result of a user action — such as activating a button — it may be appropriate to send the focus to that new content. A classic example is sending the focus to a modal dialog that pops up. Keyboard users need the focus to be sent to the dialog so they can interact with it.

## Accessibility Considerations

### The container where the focus is sent must have tabindex="-1". 

If the container is not set to tabindex="-1", the focus will not arrive successfully in all browsers, and screen readers may not read the text.

### The container must not be empty. 

You would not want to send the focus to an empty `<div>` or any other empty container, because even if the focus arrives successfully, the screen reader will have nothing to read. The screen reader will be silent, defeating the purpose of sending the focus in the first place.

### Don't move the focus unexpectedly.

Sending the focus should always be the result of either a user-initiated action, or some other critical event that demands the user's immediate attention. Don't send the focus just to make an announcement if moving the focus would disrupt the user's actions, or if the disruption is not critical. Use ARIA live regions to make announcements that do not steal the keyboard focus.

#### Sending the focus must be the last event, and it will probably be necessary to delay before sending the focus.

When content is loaded via AJAX, it sometimes takes a moment AFTER the AJAX is done loading for the AJAX content to be available to screen readers, especially if JavaScript is used to manipulate the new content after it is loaded, and especially if the keyboard focus happens to already be within the area that you intend to send the focus (either on the element itself or on a descendent of it).

If you send the focus too soon, the DOM node may not be available yet, or it may be empty, causing the screen reader to say nothing when the focus arrives on the node. Test the process in various screen readers and browsers. If any of them fail to read the content when the focus arrives, add a delay (1 to 2 seconds is plenty) before sending the focus.

In fact, to be on the safe side, it is best to add a delay with all AJAX load events before sending the focus.

#### Example

```html
<div id="decContainer"></div>
<script>   
$("#decButton").click(function(){
  $.ajax({
    url: "assets/html/module-dynamic/ajax/declaration.html", 
    type:'GET',
    cache: false,
    success: function(result){
      $("#decContainer").show().html(result);
      var decHeading = $("#decContainer h2:first");
      /* set tabindex="-1" so the heading can receive keyboard focus */
      decHeading.attr('tabindex','-1');
      setTimeout(function(){ 
        /* move focus to the heading after a delay of 1 second */
        $("#decContainer h2:first").focus(); 
      }, 1000);
    }
  });
}); 
</script>
```
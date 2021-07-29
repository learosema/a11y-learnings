# Virtual Buffer

## Screen readers create a copy of the web page

The ability to navigate through the content of a web page is achievable through the use of a "virtual buffer." The virtual buffer allows screen readers to convert HTML on the web page into a data structure that screen readers can parse effectively.

This feature provides an in-memory copy of the current Web page so a screen reader user can navigate through the page with the help of the screen reader's navigation commands.

## The virtual buffer can cause delays in reading dynamic updates

It takes time to copy the web content into the virtual buffer. Usually the update happens in a small fraction of a second, but even that small fraction of a second can interfere with the accurate reading of dynamic updates. The delay is especially noticeable with AJAX events.

If content loads via an AJAX request, you cannot send the focus immediately to the newly loaded content. You have to set a JavaScript timer to insert a delay between the completed AJAX event and sending the focus.

If you don't introduce a timed delay, the JavaScript will send the focus to a node in the DOM that is still empty or non-existent in the screen reader's virtual buffer (even though the node is not empty in the browser), because the screen reader hasn't had time to update its virtual buffer yet. The result is that the screen reader will say nothing.

Setting a JavaScript delay of approximately 0.5 to 1 second after the AJAX is confirmed to be finished is usually sufficient before sending the focus to the newly loaded content, at least for desktop computers.

For mobile devices, a delay of about 2 seconds is recommended, due to the slower processor speed (and possibly less efficient software algorithm) of mobile devices.

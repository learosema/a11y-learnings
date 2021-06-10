# Allowing mobile zoom

## The page MUST allow users to zoom in on mobile devices.

An important feature of responsive websites is the ability to zoom a mobile webpage in order to read small text, increase the touch target size of a link or other UI element, or compensate for poor contrast. 

For people with low (or slightly-less-than-perfect) vision or low mobility, this feature is especially important, but the need to use zoom on a responsive website is not limited to people with low vision or low dexterity — as many of us can attest to.

Unfortunately, too many developers choose to deliberately disable the ability to zoom websites in mobile browsers.

There are two properties on the meta viewport element that will effectively suppress pinch-to-zoom: user-scalable=no and maximum-scale=1.0.

### Note:

Note: With iOS 10, Safari now ignores attempts to disable zoom with the meta viewport properties.

### Example

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0; user-scalable=1" >
```

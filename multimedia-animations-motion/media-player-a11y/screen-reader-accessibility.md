# Screen Reader accessibility

## All controls of a media player MUST present the correct names, roles, and values to screen reader users.

Native controls — like buttons, links, and form elements — will automatically present the correct information to screen reader users.

Custom JavaScript controls require correct ARIA markup to communicate the correct semantics to screen reader users. Refer to the ARIA Authoring Practices opens in a new window on the W3C website for detailed information on how to use ARIA correctly.

### Name

The name of the control could be things like "Play", "Pause" "Volume", and so on. Every control needs an accurate name or label. For native `<button>` elements, the name is communicated by the text within the label (e.g. `<button>Play</button>` will be read as "Play, button" by screen readers).

Custom buttons and controls may require the aria-label or aria-labelledby attributes (e.g. `<span role="button" tabindex="0" aria-label="Play">`), depending on how the items are represented in the markup.

### Role

Every control needs to be recognizable as a control by the screen reader and by the user. You can add roles to custom controls when necessary. 

In the case of a media player, the most common role will be `role="button"`. This is the proper role for a play/pause button, a feature to turn captions on and off, and any simple control along these lines. The proper role for a volume slider would be role="slider. Other roles may be appropriate in other circumstances.

### Value

When a slider is moved from left to right, or up to down, screen reader users need to hear the values change. A volume slider could say things like "50%", "40%", "30%", and so on as the volume is decreased. Refer to the [ARIA Authoring Practices for sliders](https://www.w3.org/TR/wai-aria-practices-1.1/#slider) for details on how to accomplish this.
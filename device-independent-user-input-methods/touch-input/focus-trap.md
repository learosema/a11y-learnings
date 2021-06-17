# Focus trap

## Touch/gesture focus MUST NOT be locked or trapped in a particular page element and the user MUST be able to navigate to and from all navigable page elements using standard touch actions or gestures.

Generally speaking, the same rules and techniques regarding keyboard traps apply equally to touch focus traps, but the focus behavior on touch devices with screen readers turned on in particular can be a bit finicky, especially when JavaScript is involved.

### onblur and onfocus:

If a script depends on an onblur or an onfocus event, depending on how the script is structured, there is a chance that the script will not work properly on a touch device with the screen reader turned on, because the screen reader focus (the item currently being read and highlighted) is not necessarily the same as the programmatic keyboard focus.

The screen reader can highlight and read a sentence or a paragraph or a link or a button without setting the programmatic focus on those items. If you use onblur or onfocus events, test them thoroughly with touch devices, both with the screen reader turned off and the screen reader turned on.

### aria-hidden="true":

If aria-hidden="true" is set on an element that is visible on the screen (this is almost always a bad thing to do), that can have a negative impact on the screen reader swipe behavior and may cause the screen reader to lose focus or to trap the focus.

Off-screen styles: The technique of hiding elements off screen (e.g. absolute positioning of an element far to the left, out of the visible viewport) can cause problems for mobile screen readers, even though the technique is considered relatively safe in desktop browsers and screen readers.

Various focus problems have been reported in different versions of iOS with regard to this CSS technique.

Overall, it is somewhat unpredictable which kinds of JavaScript behaviors will cause focus problems on touch devices — and the bugs are somewhat volatile, appearing and disappearing unexpectedly between releases — so it isn't particularly productive to document all the situations where keyboard traps and focus problems might occur.

The best advice is to simply test your scripts on mobile devices with the screen reader on and off, preferably on a variety of platforms and versions.
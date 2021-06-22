# Widget roles

## Overview

HTML has only a limited set of roles available, making it difficult to convey the identity or functionality of custom widgets such as hierarchical tree menus, or tab panels, for example.

ARIA doesn't add any new HTML elements, but it does add the role attribute, along with a list of roles that were not part of the HTML specification before. These new roles are:

- `alert`
- `alertdialog`
- `application`
- `dialog`
- `group`
- `log`
- `marquee`
- `menu`
- `menubar`
- `menuitem`
- `menuitemcheckbox`
- `menuitemradio`
- `progressbar`
- `separator`
- `slider`
- `spinbutton`
- `status`
- `tab`
- `tablist`
- `tabpanel`
- `timer`
- `toolbar`
- `tooltip`
- `tree`
- `treegrid`
- `treeitem`

The ability to designate an element as a tab or menu or toolbar is an important innovation for people who use screen readers. Sighted users have always had the advantage of being able to see the visual design, so if there is a tab list in the design, sighted users will probably recognize it as such because it looks like a tab list.

Blind users can't see the design, and their screen readers can't interpret the visual cues for them, so blind users probably won't know they've arrived at a tab list unless something in the markup explicitly identifies the element as a tablist. This is where ARIA can help. 

Using the ARIA roles `tablist`, `tab`, and `tabpanel`, a screen reader will be able to say something like "tab list with three items" (if there are three tabs in the tab list). A simplified version of a tab list is shown below.

```html
<ul role="tablist">
<li role="tab">Home</li>
<li role="tab">Products</li>
<li role="tab">Services</li>
</ul>

<div role="tabpanel">
<p>Info about the home page/p>
</div>

<div role="tabpanel">
<p>Info about products/p>
</div>

<div role="tabpanel">
<p>Info about services/p>
</div>
```

We would still need to add some additional properties and some JavaScript to make this example work as intended, but this at least shows the basic role structure of a typical tab list. (If you'd like to see a finished example, you can refer to the sample tab panel in the "ARIA Widget Examples" section of this module.)

### Note Don't invent roles!

You cannot invent your own roles, at least not if you want assistive technologies to understand them. Any role attribute that the browser or assistive technology does not understand will be ignored. Any content in the element will still be available as it would be normally, but your invented role will not be communicated to the user.

## Related links

- Article [WAI ARIA 1.0 - The Roles Model](https://www.w3.org/WAI/PF/aria/roles)

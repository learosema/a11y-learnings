# Skip Navigation Links

## A keyboard-functional "skip" link SHOULD be provided to allow keyboard users to navigate directly to the main content.

The main content of a web page rarely comes first in a typical layout. Before users can arrive at the main content, they must skip past features like the website's logo and branding, the site search, the login widget, and the main navigation. In some cases, a secondary navigation level also appears before the main content. The top section of a web page can be quite long. Providing a way to skip past all of the features at the top of a web page helps save keystrokes for keyboard users.

```html
<div id="skipnav"><a href="#mainContent">Skip navigation</a></div>

<!-- the header, navigation, etc. go here -->

<main id="mainContent" tabindex="-1">
    <!-- the main content goes here -->
</main>
```

`tabindex="-1"` makes the main content area programmatically focusable (also works without providing it in Chrome, but some browsers such as Safarirequire it that way).

## A skip link MUST be either visible at all times or visible on keyboard focus.

### Option 1: Make the link visible all the time

The most accessible — though also probably the least popular — way to include a "skip navigation" link in a design is to make it visible all of the time. All users, whether sighted or blind, will be able to take advantage of "skip navigation" links like this.

### Option 2: Make the link visible on keyboard focus

Designers tend not to like the look of visible "skip navigation" links, so they tend to hide them from sighted users. That can be acceptable, as long as the link becomes visible when it receives keyboard focus. The link can be hidden by default, using the CSS clip technique, then made visible by removing the CSS clip when the link receives focus.

#### Note

Do NOT use display:none to hide "skip navigation" links, because that will make them unavailable to keyboard users, including screen reader users.

#### Good example: Display on focus

```html
<head>
  <title>Museum Information</title>
  <style>
    #skipnav a {
      position: absolute;
      clip: rect(0 0 0 0);
      border: 0;
      height: 1px; margin: -1px;
      overflow: hidden;
      padding: 0
      width: 1px;
      white-space: nowrap;
    }
    #skipnav a:focus {
      clip:auto;
      left:0;
      top:0;
      width:100%;
      height:auto;
      margin:0;
      padding:10px 0;
      background:#fdf6e7;
      border:2px solid #990000;
      border-left:none;
      border-right:none;
      text-align:center;
      font-weight:bold;
      color:#990000;
    }
  </style>
</head>
<body>
  <div id="skipnav"><a href="#mainContent">Skip navigation</a></div>
  <!-- document banner, navigation, etc. -->
  <main id="mainContent" tabindex="-1">
      <h1>Link will take users to this location.</h1>
      <!-- other content in the main content -->
  </main>
  <!-- other content on the web page -->
</body>
```

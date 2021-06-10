# Responsive objects and plugins

## Objects/plugins SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
As the viewport size changes, ensure that objects and plugins also adjust in size so they do not overflow the viewport.

### Technique 1: Set max-width:100% on the container

The techniques for making <object> elements and plugins will vary from one <object> and plugin to another, but one of the most basic concepts is to set max-width: 100% on the container around the <object> or plugin. If the element allows resizing, it can fill the container completely. Flash, Silverlight, SVG, and other types of elements are capable of filling up the full width of the container.

## Technique 2: Use vector images

Within the <object> or plugin itself, use vector-based elements whenever possible, to allow maximum clarity when users zoom in.
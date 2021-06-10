# Screen Size Breakpoints

Media queries give you the ability to create as many different style breakpoints as you like. If you really wanted to, you could create a set of styles for every size of smart phone on the market today, every tablet, and every screen of every kind. That would be a very long style sheet, and it would definitely be overkill.

## Create Only a Few Breakpoints

Keep your breakpoints to the minimum necessary for your design. A typical scenario would be to create breakpoints for three display sizes: small (phones), medium (tablets), and large (desktops). If your design is flexible enough, you may even be able to get away with breakpoints for just two sizes: small, and larger.

## Where Should You Set Your Breakpoints?

There is no one right answer as to where to set your breakpoints. The answer depends on your design. Set your breakpoints where your design needs them. It is helpful to know the approximate sizes for the ranges of device you want to accommodate, but you cannot predict which size devices your users will have, so make sure your design accommodates a broad range of sizes.

- Watches: up to about 320px
- Phones: about 320px
- Phones (plus size): up to about 600px
- Tablets: about 600px - 900px
- Desktop & Laptop: usually 1024px and larger

## Exact Device Breakpoints

For those who need more precise numbers, there are online resources that list the exact viewport dimensions of various devices:

- [Viewport Sizes](https://viewportsizer.com/devices/)

## Emulating Device Breakpoints

Nobody can buy every size of every kind of device, and nobody would want to. There are just too many devices and too many sizes to take into account. Fortunately, you can test your breakpoints using some viewport emulators.

### Note:

Viewport emulators show you an accurate representation of your media queries and styles. They are NOT an accurate representation of the functionality or features of the browser. Do not rely on these methods for testing JavaScript, ARIA, keyboard accessibility, or any other interactive features.

### Viewport emulators

- https://viewportemulator.com
- Firefox dev tools
- Chrome dev tools

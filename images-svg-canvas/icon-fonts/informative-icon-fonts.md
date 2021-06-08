# Informative Icon Fonts

## Informative icon fonts without accompanying visible text SHOULD be assigned role="img".

Even though icon fonts are technically fonts (like text), they act as images. It's best to assign role="img" to icon fonts in most circumstances so that blind users will be aware that an image is present.

When role="img" is assigned to icon fonts, screen readers will list the icon font among the list of all images on the page and will allow users to navigate to the icon font when navigating through graphics (e.g., when using the "G" key in JAWS, NVDA, or in scan mode in Narrator).

The examples below use icon fonts from the [Font Awesome](https://fontawesome.com/) collection.

### Example

Adding `role="img"` gives the font icon the proper semantics.

```html
<p>Have a great day 
    <span class="fa fa-smile-o" role="img" aria-label="Smiley face"></span></p>
```

## Informative icon fonts without accompanying visible text MUST have a text alternative.

Although it is possible to add alternative text via hidden text (using position:absolute; clip:rect(0 0 0 0), without assigning role="img", this usually isn't the best method, for three main reasons:

- The icon font is not recognized as an image.
- On mobile devices, the visible icon font is not available to screen reader users when using the "explore by touch" method.
- VoiceOver on OS X focuses separately on the icon font item and then on the hidden text, even when the icon font is set to aria-hidden="true".

### Example

```html
<p>Forms of payment accepted:<br>
   <span class="fa fa-cc-mastercard fa-2x" role="img" aria-label="MasterCard"></span> 
   <span class="fa fa-cc-visa fa-2x" role="img" aria-label="Visa"></span> 
   <span class="fa fa-cc-paypal fa-2x" role="img" aria-label="PayPal"></span>
</p>
```


## Actionable icon fonts without accompanying visible text MUST have a text alternative.

Actionable icon fonts include icon fonts used as links, buttons, controls, or any other interface element with which users can interact.

```html
<p>
   <a href="#">
      <span class="fa fa-facebook-official fa-2x" aria-label="Our Facebook page">
      </span>
   </a>
</p>
```

## The alternative text for informative icon fonts MUST be meaningful.

### Bad example

```html
<p>Enter your username 
   <button>
      <span class="fa fa-question-circle" aria-label="?"></span>
      <!-- screen readers will literally say 
      "question mark" or "question" -->   
   </button>
</p>
```


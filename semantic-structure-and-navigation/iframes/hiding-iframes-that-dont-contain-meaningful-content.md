# Hiding iframes that don’t contain meaningful content

## Hidden frames or frames that do not convey content to users SHOULD be hidden from assistive technologies using `aria-hidden="true"`.

Sometimes the content of an iframe is not important at all. It may contain only JavaScript, or it may be there purely for decorative purposes. If that's the case, you should hide the frame from screen readers using `aria-hidden="true"`.

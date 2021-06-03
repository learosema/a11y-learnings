# Best practices for landmarks
 
## All text SHOULD be contained within a landmark region.

## Multiple instances of the same type of landmark SHOULD be distinguishable by different programmatically determinable labels (aria-label or aria-labelledby).

## A page SHOULD NOT contain more than one instance of each of the following landmarks: banner, main, and contentinfo.

## The total number of landmarks SHOULD be minimized to the extent appropriate for the content.

There is no technical limit on the number of landmarks you can implement in a page, but one of the main purposes of landmarks is to allow blind users to quickly find and navigate to the appropriate landmark, so you should keep the total number of landmarks relatively low. If you don't, screen reader users will have to sort through too much extra information to find what they're looking for.

For example, just because you can mark a list of links as a navigation landmark doesn't mean that you always should. If you have, say, one to three navigation landmarks (each labeled with aria-label or aria-labelledby), users will have no problem. But if you have 15 to 20 navigation landmarks, it may take users a long time to figure out what all navigation lists are for, and which one contains the information they're looking for.


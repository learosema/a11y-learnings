# Prioritizing Accessibility Bugs

## Overview

So-called "regular" bug repairs and feature requests never get implemented en masse. Instead, they are prioritized based on things like business value, risk, user impact, etc. Similarly, the remediation of accessibility defects need to be prioritized.

Using the factors discussed below, you can assign a priority level to each identified issue, e.g. 1 (High) – 4 (Low). Over time, accessibility bugs can be remediated according to this prioritization. In this manner, a type of "dilution" occurs with respect to accessibility problems such that the overall negative impact of the accessibility problems becomes lower over time.

## Factors that Influence Priority

### User Impact

Since the goal of any accessibility remediation effort is to make the system more accessible, it makes sense to give priority to items that will have a high positive impact to the end user with disabilities. Conversely, it also makes sense to delay repair of things that will have a lower impact on the end user with disabilities. We recommend the following user impact rating system:

- Critical: This issue results in blocked content for individuals with disabilities. Until a solution is implemented content will be completely inaccessible, making the organization highly vulnerable to legal action.
- Serious: This issue results in serious barriers for individuals with disabilities. Until a solution is implemented, some content will be inaccessible, or significant a work-around is required, making the organization vulnerable to legal action. Users with disabilities may experience significant frustration when attempting to access content.
- Moderate: This issue results in some barriers for individuals with disabilities but would not prevent them from accessing fundamental elements or content. Users with disabilities may experience moderate frustration when encountering this issue.
- Minor: This is an issue that may inconvenience a user but would not cause significant frustration in accessing content or accomplishing tasks.

### Time to Remediate

If the goal of our remediation effort is to fix the system, it only makes sense to utilize developers' time wisely. Part of doing so is knocking out the easier things before the hard things, which means we can get further down the road towards an accessible system more quickly.

### Business Priority

This factor takes into account whether an accessibility defect occurs in the flow of a core business process — for instance the checkout process of an online store — versus content that is not part of the core mission of the business — such as social media widgets. Obviously, defects that are in a core business flow will have a higher priority than those that are not.

### Location of Issues

In any site, there will be those pages that get far more traffic than others. People commonly understand this concept as the 80/20 rule. In reality, it might be that 15% of your pages gets 90% of your traffic. Whatever the case, you will want to remediate issues which occur on the pages with the highest traffic before those that don't get much traffic at all.

### Volume

In cases where the exact same failure is found multiple times, the volume of the occurrences can be seen as a multiplier in terms of Impact. In other words, an issue that exists in 100 places is 100 times more impactful than something which happens only once. In this case, a large benefit can be realized quickly by fixing the templates or classes which cause the most common errors first.

### Impact on Interface and Operation

There may be times when an accessibility-related repair may be necessary which would have a significant impact on the user interface and/or operation of the interface as it is currently designed. One area where this happens frequently is in color contrast of primary site templates. In these cases, poor color contrast is used which is related to the organization's branding as a whole. Improving the color contrast would essentially require a redesign of the site. In this scenario, things which will require significant redesign will need to be given lower priority over things which will have little-to-no impact on the interface.

### Secondary Benefit

The Web Accessibility Initiative at the W3C has put together a series of resources that they call Developing a Web Accessibility Business Case for Your Organization. Interspersed throughout that "Business Case" are assertions that accessibility has secondary benefits—for instance, improvements for older populations. It stands to reason then, that issues which provide numerous secondary benefits can be given higher priority during remediation, especially if those benefits are mapped to a business need of your organization.

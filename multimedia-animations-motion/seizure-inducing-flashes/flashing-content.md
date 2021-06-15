# Flashing content

## Overview

Seizures are abnormal or erratic electrical impulses in the brain that interfere with a person's ability to process information or, in some cases, control voluntary muscle movement. Some seizures can result in violent convulsions that put a person at risk of injury.

Seizures can be caused by a wide range of circumstances including brain injury, dehydration, sleep deprivation, infections, fevers, drug overdoses, drug withdrawals, and even flashing lights. This last category is the one that is of interest to web developers.

## Photo-Epileptic Seizures

Putting flashing or strobe-type effects in videos, graphics, or animations can put some viewers — those with photosensitive epilepsy — at risk for seizures. 

Seizures caused by flashing lights are sometimes known as photo-epileptic seizures. One of the most well-documented cases of flashing lights causing seizures was a Pokémon cartoon in 1997 that sent 685 children to the hospital when they experienced seizures as a result of an intense scene with flashing lights.

The movie Breaking Dawn featured an intense scene with flashing lights that caused people to experience seizures in the movie theater.

Even content that does not trigger seizures can trigger dizziness, nausea, or disorientation in some viewers. This will be discussed further in the next section on Animations and Motion.

## A page MUST NOT contain content that flashes more than 3 times per second, unless that flashing content is sufficiently small, and the flashes are of low contrast and do not exceed general flash thresholds or red flash thresholds.

Content that flashes or flickers more than 3 times per second may trigger a seizure in people who have photosensitive epilepsy or other types of photosensitive seizure disorders. It is important to not create content that may cause seizures for your users.

If content that flashes more than 3 times per second is small enough or below certain contrast thresholds, the risk for triggering a seizure is greatly reduced. Therefore, content that flashes more than 3 times per second is permitted as long as one of the following conditions are met:

### The flashing area is "small enough."

So, what is small enough? WCAG defines "small enough" as: "less than 25% of 10 degrees of visual field (which represents the central area of vision in the eye)."

Calculating that size for all possible screen sizes would be time consuming and laborious, so the W3C has also provided a rule of thumb to provide a safe threshold for users on a wide variety of screen types.

The details of the calculations used to create the recommendation can be found in the WCAG technique document [G176: Keeping the flashing area small enough](https://www.w3.org/TR/WCAG20-TECHS/G176), but it boils down to this: "...any single flashing event on a screen (there is no other flashing on screen) that is smaller than a contiguous area of 21,824 sq pixels (any shape), would pass the General and Red Flash Thresholds."

For example, a flashing area of 200px x 100px would meet this condition.

### The contrast of the flashing content is "low enough."

So, how do we determine what contrast is low enough? As with the maximum size threshold for flashing content, the W3C provides a highly technical formula to calculate contrast in their definition of ["general flash and red flash thresholds"](https://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html#general-thresholddef).

In this case, the W3C's recommendation is to use a tool to assess flashing content such as The Trace Center's [Photosensitive Epilepsy Analysis Tool (PEAT)](https://trace.umd.edu/peat/), a free, downloadable resource for developers to identify seizure risks in their web content and software.

To be on the safe side, you should consider eliminating ALL flashes, but small flash areas or very low contrast flashes may be acceptable from a seizure perspective (even though they are still likely to be annoying and distracting, which can be an issue for users with attention deficit disorder or cognitive disabilities).

## Testing Flashing Content

Testing the number of flashes per second — to determine accessibility compliance or failure — can be somewhat tricky. There is a free software tool, [PEAT](https://trace.umd.edu/peat) that can be of use, and there is a service called the [Harding Test](http://www.hardingtest.com/). To be on the safe side, though, anything that noticeably flashes multiple times per second is probably risky, and it would be best to remove it or fix it so it doesn't flash.
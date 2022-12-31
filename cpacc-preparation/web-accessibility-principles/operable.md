# Operable

## Defining Operability: A Declaration of (Device) Independence

Operability is about making the input methods of web content functionally available to a wide range of input devices, including:

- mouse or touchpad
- keyboard
- touchscreen
- voice recognition software
- other specialized input devices (most of which emulate the keyboard or mouse)

## Not Everyone Uses a Computer Like You Do

You may be able to use a mouse and touchpad just fine, but that doesn't mean that everyone can. Someone with tremors in their hands would find a hard time using mouse or touchpad, because such devices require fine muscle control and precise movements.

Similarly, not everyone can use a keyboard. Some people have little or no movement in their limbs and may need to rely on a device that senses movements in their cheek muscles, or that tracks the gaze of their eyes across the screen, or that interprets their speech as voice commands.

## Everything Has to Work

The goal of operability is to ensure that web components work. All features—particularly navigation and dynamic or interactive components—must be functional, no matter what input device a person is using. If any part of the web content is not available with a given input device, the content is essentially broken for that user, even if the features are available through other input devices.

## In, Within, Through, and Out

You have to be able to navigate into web components, use the features within them, navigate through them, and navigate out of all of them, no matter what input device you're using. If any of these aspects of operability does not work with an input device, some users will be unable to use the web component.

For example, keyboard users must be able to navigate into a JavaScript drop-down menu, select a link within that menu, or move past the menu if they want to, all without using a mouse.

Keyboard users must also be able to navigate into a video player, use all of its controls—such as play, pause, volume, mute, rewind, fast forward, captions, audio descriptions, full screen, etc.—and then navigate out of the media player without a mouse.

Touchscreen users must be able to activate functionality that is triggered with mouse hover events, even though there isn't a clear mechanism on many touchscreens for handling hover events.

Flash content is a particular concern here, because Flash objects can create a keyboard trap. Users may be able to navigate into the Flash object, and they may even be able to use the features inside of it, but chances are that they won't be able to navigate out of the Flash object with the keyboard, especially in browsers other than Internet Explorer (Adobe worked more closely with Microsoft on the keyboard trap problem than it did with Mozilla, Google, or other browser makers).

## Scripting for Device Independence

Plain web content without any scripting or dynamic features is mostly device-independent by default. You don't have to do anything special to make standards links or form elements work with multiple devices. If you leave them alone, they'll work just fine.

It gets trickier, though, when you start creating dynamic interactions with scripts. Scripts are powerful, and they can override the default behaviors of pretty much any native component. You can even create your own components from scratch. That gives you a lot of power and flexibility.

It also creates a lot of liability, because you can break the functionality of native components or create device-specific custom components that are unusable with the input methods that you didn't take into account.

To the extent possible, you should use device-independent event handlers (such as onfocus, onblur, and onselect), rather than device-specific event handlers (such as onmouseover, onmouseout, and ondblclick).

Sometimes, though, you need to use both. You may need to supply a mouse-specific event handler and a redundant keyboard-specific event handler in some circumstances. Be sure to test it both ways, and to also test on touchscreens.

## Control the Focus

When you create dynamic interactions, always pay close attention to the location of the programmatic focus. Usually the programmatic focus is the same as the keyboard focus.

Most browsers will highlight the programmatic focus with a dotted line or glowing colored line around the element. When you create a popup modal dialog, ensure that the focus automatically lands on the modal dialog.

When a user exits the modal dialog, ensure that the focus returns to the previous focus location. Don't let the focus get lost, because when that happens, usually the focus reverts back to the top of the document, and the user is forced to navigate back down to the previous location, wasting the user's time and efforts.

## Timing

In addition to ensuring that things work with various devices, you have to ensure that people have enough time to interact with the content.

A detailed form—such as a mortgage loan application, a college admissions application, or tax forms (yikes!)—can take a long time to fill out, even if you are completely physically able.

You wouldn't want to force an automatic session timeout when a user is in the middle of filling out a form like this, because there is a chance that the user might lose all of the data entered and have to start over again.

Session timeouts are allowable as long as you give the user sufficient warning, for example in a popup notification. Just ensure that the notification is accessible! (Users need to get into, within, through, and out of the notification.)

## Keyboards: The (almost) Universal Input Device

You can accomplish near-universal operability of your web content by making it keyboard-accessible. People without disabilities use keyboards.

Blind people use keyboards instead of mouse or touchpad devices because they can't see where the mouse pointer is on the screen, making the mouse rather useless.

People with some kinds of motor disabilities use keyboards (in some cases special adaptive keyboards) because they can't control the movements of a mouse or touchpad. Even most touchscreens have onscreen keyboards, and they allow navigation through interface components in a way that emulates using the tab key, arrow keys, enter key, and/or escape key on a keyboard. What's more, most specialized input devices emulate the functionality of the keyboard. Devices that sense simple movements in a person's cheek or elbow or other body part, for example, can be adapted to emulate keystrokes for typing text or for navigating the interface. The input process is often slower with these special hardware and software combinations; given enough time, users of these technologies can do all that non-disabled users can do, as long as the content and interface have been made keyboard-accessible.

In saying that the keyboard is the near-universal input device, don't take this to mean that you should ignore mouse users. You still need to make content accessible to them, and you still need to test for mouse accessibility. In fact, there are some specialized input devices that emulate mouse functionality, such as through eye gaze tracking or other means. You wouldn't want to write scripts that only allowed keyboard access, for instance. It just means that you don't need to test with every conceivable hardware and software combination to ensure that you've taken into account all of the possibilities. If you can use web content with a keyboard and with a mouse, chances are very high that you can use it on most every other device. There are exceptions, as you might imagine, but those exceptions are uncommon.

## See Also:
The official Web Content Accessibility Guidelines, [Principle 2: Operability.](http://www.w3.org/TR/WCAG20/#operable)
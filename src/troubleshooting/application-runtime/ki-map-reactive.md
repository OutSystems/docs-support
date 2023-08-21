---
tags: runtime-mobileandreactiveweb;  
summary: Known issues with related to the OutSystems Map UI Pattern.
locale: en-us
guid: c870a0bf-e68a-4fab-94e5-d5d0ed9e3493
app_type: mobile apps, reactive web apps
platform-version: o11
figma:
---

# Known issues with the Map component for Reactive Web apps

<div class="info" markdown="1">

Applies only to Mobile Apps and Reactive Web Apps

</div>

This list contains known issues currently being investigated by OutSystems. You can use it to see if an issue affecting you is already known and decide when to upgrade. If you have any questions, comments, or need some assistance, you can post a question on the [Support tab of the Forge component](https://www.outsystems.com/forge/component-discussions/9909/OutSystems+Maps).

## Changing the Offset property in a Map with both Map center and Markers position using coordinates with Auto Zoom

Changing the **Offset** property on a Map with both Map center and Markers position using coordinates with Auto Zoom won't show the final map with the correct offset values.

**Status:** We're currently evaluating the impact of this issue and figuring out how it can be fixed.

## Marker Popup doesn't close with ESC key when the popup contains links

When the marker popup is customized to use any type of links, the popup can't be closed with the ESC key. The only way to close the popup is by clicking on the "x" on the right corner of the popup.

**Workaround:** When the popup has hyperlinks, click inside it before using the ESC key.

**Status:** We're currently understanding the impact and how can this be fixed.

## Polyline and Polygon shapes sometimes have dragging issues

When the map has draggable and non-draggable shapes and we try to drag a shape that has the allowDrag configuration set to False, if we then want to drag-and-drop a draggable polyline/polygon, those shapes might not change their position. It looks like the problem is google provider derived.

**Workaround:** Click again on the non-draggable shape and then try to repeat the action on the draggable shape.

**Status:** We're currently understanding the impact and how can this be fixed.

## SearchPlaces has a CSS problem while scrolling the page with the dropdown suggestions opened.

Depending on the CSS of the SearchPlaces container, when the suggestions dropdown appears, if we then try to scroll on the page with that dropdown still opened, the element doesn't scroll with the page.

**Status:** We're currently understanding the impact and how can this be fixed.

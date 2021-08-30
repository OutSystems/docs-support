---
summary: Test your aps on the OutSystems Reactive Web and Mobile runtime with a new version of React.
tags:
---

# Technical Preview - Reactive Web and Mobile runtime on React 16

<div class="warning" markdown="1">

This is an archived page. OutSystems uses React 16 as the default React for the app runtime since Platform Server 11.12. 

</div>

Reactive Web and Mobile Apps use React 15 for the app runtime. OutSystems plans to update to a newer version of React, which may introduce breaking changes in your apps. To anticipate possible breaking changes in the app behavior, you have an option to turn on **Runtime using React 16 Technical Preview**.

It's an OutSystems strong recommendation that you use the React 16 technical preview to test your apps and address all potential issues before React 16 becomes the new runtime default.

## Checking for issues

Once you activate React 16 technical preview in your platform, verify the app works correctly.

* See the [known issues](#known-issues) section to learn about the issues OutSystems identified and working to fix in a future OutSystems release.
* See the [side effects](#side-effects) section to read about how new features and changes in React 16 affected the app runtime.

<div class="info" markdown="1">

Only the apps you **publish or republish** after activating **Runtime using React 16** technical preview in LifeTime use the new React 16 runtime.  

</div>

## Side effects

Here is a list of the side effects due to the differences between React 15.0.2 and React 16.13.1. For all the release notes since React 15.0.2, see the [React GitHub releases page](https://github.com/facebook/react/releases).

### Widgets ignore tampered events 

Widgets ignore events that you create or change by JavaScript. For example, OnChange Event Handlers fail to execute if you change the event before reaching the widget. This typically impacts scenarios where an input is having its value filtered / formatted / masked with JavaScript extensibility.

This issue affects the following Forge components:

* [Input Masks Library](https://www.outsystems.com/forge/component-overview/2258/input-masks-library)
* [Input Masks Mobile](https://www.outsystems.com/forge/component-overview/5289/input-mask-mobile)

For related React documentation see [Improving inputs](https://reactjs.org/blog/2017/06/13/react-v15.6.0.html#improving-inputs).

### All attributes show in the HTML

All unknown HTML attributes now show in the resulting HTML. React previously removed all attributes except **data-** from the output. Due to this change, the runtime now applies the CSS rules that were ignored.


For related React documentation see [DOM Attributes in React 16](https://reactjs.org/blog/2017/09/08/dom-attributes-in-react-16.html).

### Option HTML element only allows text as children

By definition, the `option` HTML element only allows text as children. This is now enforced by React 16 and all children of an `option` element are now stringified, which may result in rendering `[object Object]` when that children is another HTML element, like a `span`.

This affects custom implementations of a native dropdown making use of HTML Element widgets with an `option` tag. This pattern can instead be implemented using a Dropdown widget with the "Options Content" property set to `Text Only`.

A temporary workaround is to remove the children of the `option` element and create a `label` attribute with the desired text.

## Known issues

Here is the list of known issues that the OutSystems development team identified and is now **working to fix in a stable runtime release**.

### Pending

There are no pending known issues at the moment.

<div class="info" markdown="1">

Found an issue? Let us know! Post a [new question with the **technical preview** tag](https://www.outsystems.com/forums/tag/6875/technical-preview/) in Forums.

</div>

### Fixed

This is the list of fixed known issues.

#### The first screen shows as default when no default exists

Fixed in Platform Server 11.10.1, issue RAR-356.

If you don't set a screen as default, the app uses the first screen of the module as the default. Additionally, the app no longer shows "No Default Screen" error screen.

#### No navigation after pending refresh

Fixed in Platform Server 11.10.1, issue RAR-422.

In cases where a user needs to refresh the screen, the app still shows the origin screen after refreshing instead of navigating to the destination screen.

#### No rollback failure message

Fixed in Platform Server 11.10.1, issue RAR-423.

When an app rolls back an upgrade, there's no message notifying the user that the upgrade failed.

#### Overriding back navigation handler doesn't work

Fixed in Platform Server 11.10.2, issue RAR-333.

If you register a back navigation handler, the app triggers it, but also navigates back to the previous screen.

#### No animation on leaving the screen

Fixed in Platform Server 11.10.2, issues RAR-439 and RAR-445.

There's no animation when users leave the current screen.

## Send feedback

If you experience issues with this technical preview, let us know by posting a [new question with the **technical preview** tag](https://www.outsystems.com/forums/tag/6875/technical-preview/) in Forums.

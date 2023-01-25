---
summary: MABS 6 may cause some breaking changes in your builds after you upgrade from MABS 5. Here is information how to address the issues.
tags:
locale: en-us
guid: f5ab33b1-bc12-4d9f-bf96-16c6c4d11690
app_type: traditional web apps, mobile apps, reactive web apps
---

# MABS 6 breaking changes and known limitations

<div class="info" markdown="1">
For common issues and solutions, check also <a href="https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Troubleshooting_the_Mobile_Apps_Generation" title="Troubleshooting article for Mobile Building Service">Troubleshooting the Mobile Apps Generation</a>.
</div>

After you start building your apps with MABS 6, you may experience some breaking changes and known limitations. Check this document for more information about the issues and how to fix them.

<div class="info" markdown="1">

The most significant change in MABS 6, compared to MABS 5, is the introduction of WKWebView, which makes you mobile apps compliant with Apple's requirements for publishing the app in the App Store. This implies dropping support for iOS 10.

</div>

## Breaking changes

Here is the list of MABS 6 breaking changes, with the instructions on how to fix the issues that may result from the changes.

### XHR / Fetch requests to OutSystems servers don't work

**Symptom**

XHR / Fetch requests to OutSystems servers fail.

**Workaround**

Custom JavaScript nodes for XML HTTP Requests work only with the servers that implement CORS. iOS apps now load from `outsystems://` and not `https://`, so the `document.origin` returns `outsystems://hostname.domain`. All requests to `https://hostname.domain` are considered cross-origin because the
protocol is different between the origin and the target. This makes WKWebView enforce CORS, which is currently not implemented by OutSystems servers. The XHR / Fetch requests to other servers depend on whether those servers implement CORS.

You can try these workarounds:

* Use a Server Action. Starting with MABS 6 with WKWebView, Server Actions calls are made through the native code instead of XHR and they're not subject to CORS validations.
* Implement CORS on the server. If you have access to the backend configuration, ensure that CORS is implemented correctly and that the application origin header value is allowed.
* Use a Cordova plug-in such as [cordova-plugin-advanced-http](https://github.com/silkimen/cordova-plugin-advanced-http) to "proxy" the HTTP requests using native code (outside WKWebView), as this bypasses CORS altogether.

### Cookies from OutSystems servers aren't accessible from document.cookie

**Symptom**

Cookies from the OutSystems servers aren't accessible from `document.cookie`.

**Workaround**

Since `document.cookie` is not available in MABS 6, use the internal API to display cookies: `OutSystemsNative.Http.getCookies()`.

### RedirectToURL Event fails

**Symptom**

The RedirectToURL Event fails on MABS 6.

**Workaround**

Because the iOS applications from MABS 6 load with `outsystems://`, and not `https://`, redirects with the absolute URLs to another OutSystems app fail.

![RedirectToURL Event property](images/event-redirecttourl-prop.png?width=300)


You can try these workarounds with RedirectToUrl:

* In MABS 6: for iOS use the custom scheme `outsystems://`, for Android use `https://`.
* In MABS 5.X: and earlier: use `https://` for both iOS and Android.
* If you're targeting different MABS versions and platforms, implement custom logic that checks platform in use (MABS 6 or earlier) and sets the correct URL (`outsystems://` or `https://`).

Additionally, use the relative URLs whenever applicable.

As a best practice, open URLs by using the InAppBrowser plug-in, as this way you maintain the context of the current app. Note that when using the InAppBrowser plug-in you should always use `https://` for both Android and iOS, independently of the MABS version.

## Known limitations

Here are the MABS 6 known limitations.

### Web Inspector doesn't show Network information

**Symptom**

Safari Web Inspector doesn't show Network information about Server Actions requests.

**Workaround**

Since January 2020, MABS 6 comes with the [network inspector feature](https://success.outsystems.com/Documentation/11/Developing_an_Application/Troubleshooting_Applications/Inspect_the_HTTP_requests_in_Mobile_Apps_for_iOS). Rebuild your apps and use this feature to troubleshoot the app network issues in iOS.

### Images don't render in iOS when using Content Security Policy

**Symptom**

After generating a mobile app with MABS 6, some or all images, fonts, videos, scripts, or stylesheet resources, don't load when running the app in iOS. Upon inspection in Safari, you can see one or more error messages similar to this in the console:

`Refused to load the image 'http://subdomain.example.com/path/to/image' because it violates the following Content Security Policy directive: "img-src 'self' data: subdomain.example.com blob:".`

**Cause**

Due to some changes in MABS 6 that require mobile apps to load using `outsystems://` when running in iOS devices, some less strict Content Security Policy (CSP) directives such as `img-src 'self' data: subdomain.example.com` are now violated when loading resources from such hosts. The violations don't occur when running in Android because the Android still loads applications using `https://`, just like in MABS 5.

**Workaround**

You can fix this issue by updating the CSP configuration **for mobile apps** and ensuring that all URL expressions are prefixed with `https://`. You can find some examples in the document [Apply Content Security Policy](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Apply_Content_Security_Policy#mobile-apps).

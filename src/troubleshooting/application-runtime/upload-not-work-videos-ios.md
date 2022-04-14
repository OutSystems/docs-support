---
summary:
locale: en-us
guid: fef0d982-a3ee-45db-93e7-cd3f26aecd0d
---

# Known issue - Upload widget not working for videos in iOS 10.3

It came to our attention that mobile applications built using OutSystems were having problems uploading videos on iOS devices with versions 10.3.1, 10.3.2, 10.3.3.

**Am I affected by this?**

This issue happens if you have an iOS mobile app and use it to upload videos from the file system to the server.

Note that videos filmed through the upload widget will still work, only the ones selected from the file system will fail.

**Technical information**

At versions 10.3.x Apple introduced some changes to the UIWebView that broke the ability to upload videos to input type="file" fields, used in the upload widget.

According to Cordova this issue was already reported to them, and their response is that this is an Apple problem and they won’t fix it. ([https://issues.apache.org/jira/browse/CB-12664](https://issues.apache.org/jira/browse/CB-12664))

**What we did and are doing**

We tried different workarounds but were not able to read the video files because the access is always blocked to the WebView.

We are communicating with Apple about the matter, trying to solve the issue that is impacting our developers.

This is an underlying technology problem, and we are limited in what we can do to fix the problem.


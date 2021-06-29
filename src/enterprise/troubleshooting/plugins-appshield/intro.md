---
summary: Troubleshooting OutSystems AppShield mobile plugin.
tags: support-mobile
---

# Troubleshooting the OutSystems AppShield mobile plugin

The issues related to the AppShield plugin, and how to resolve them.

## Using AppShield with Google AppsSigning requires encoding

<div class="info" markdown="1">

OutSystems fixed this issue. You should upgrade your Platform Server and LifeTime to a newer version.

</div>

If you have Google Play App Signing feature enabled in the Google Play Console your app may crash. Logcat, once you deobfuscate the logs, shows a RepackagingException. Applies to LifeTime 11.6.1 and earlier and Platform Server 11.10 and earlier.

In LifeTime, if you edit the **Extensibility Configurations**, you must encode the value of the  **GooglePlayAppSigningCertificate** key. To encode the value of the certificate, follow these steps:

1. In Google Chrome developer tools, open the console.
2. Run the following JavaScript code: `encodeURIComponent("[public-key-certificate]")`.
3. Copy the output of the command as the new value for the **GooglePlayAppSigningCertificate** key.

For more information about Google app signing, see [Google Play App Signing](https://developer.android.com/studio/publish/app-signing#app-signing-google-play).

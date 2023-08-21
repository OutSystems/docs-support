---
summary: 
locale: en-us
guid: A62F7870-428F-4AAB-B786-F8F347B0A4C6
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Troubleshoot SSO sessions for Traditional Web Apps

Server requests coming from Reactive or Mobile Web apps do not refresh Traditional Web app sessions. This means that even though the user might be interacting with the Reactive Web app, but not with the Traditional Web app, the idle session timeout of the Traditional Web app will be reached. Therefore, when the user tries to access the Traditional Web app, they must log in again.

One way to mitigate this is for the Reactive and Mobile Web apps to request a traditional app page, which extends the Traditional Web app session.

To avoid having to explicitly call the traditional app page in the code, a possible approach is to extend the send action from the [XmlHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) to perform an additional request target at the Traditional Web page.

To achieve this, follow these steps:

1. Create a simplified traditional app, with the same user provider as the reactive or mobile app, containing a blank screen.

    The traditional application’s web screen will be targeted by the reactive and mobile apps.

1. In each reactive or mobile app module, do the following:
    
    (a) In the **Client Actions**, add the **OnApplicationReady** action (if it doesn't already exist).

    (b) Inside the action, add a JavaScript node with the following code, replacing the ``<ModuleName>``with the traditional module name, the ``<ScreenName>`` with the traditional screen name, the ``<TimeoutMs>`` with the request timeout in milliseconds and the ``<RequestInterval>`` with the minimum waiting time the traditional web page should be requested:

    ```javascript
        const Logger = 
        require("OutSystems/ClientRuntime/Main").Internal.Logger;
        const logXHRError = (err) => {
            Logger.trace("XMLHttpRequest", err);
        }

        (function(xhr) {
            const originalSend = xhr.send;
            var nextTraditionalRequestTimestamp = 0;

            xhr.send = function() {
                try {
                if(nextTraditionalRequestTimestamp < Date.now()) {
                    fetch("/<ModuleName>/<ScreenName>.aspx", {signal: 
        AbortSignal.timeout(<TimeoutMs>)}).catch(logXHRError);
                nextTraditionalRequestTimestamp = Date.now() + 
        <RequestInterval>;
                }
            } catch (err) {
                logXHRError(err);
            }
            return originalSend.apply(this, arguments);
            };
        }
        )(XMLHttpRequest.prototype);
    ```

    Note that the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) is used in this example. This executes the request asynchronously which ensures little or no impact on the original request.

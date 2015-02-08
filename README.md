# Android-JavascriptInterface-Sample

Call Java (Android) methods from Webview using Javascript

## How To

1. Create a class named `JSInterface` inside any Activy or other Intent
2. Create a public method with `@JavascriptInterface` annotations (<span style="color: red">DO NOT MISSPEL THIS</span>)
        ```java
            public class JSInterface {
            ...
            @JavascriptInterface
            public void toastMe(String text) {
                Toast.makeText(mContext, text, Toast.LENGTH_SHORT).show();
            }
        }
        ```
3. Call `JSInterface.toastMe(text)` from Webview's Javascript instance
        ```javascript
        var text = "I want to be toasted";
        JSInterface.toastMe(text);
        ```

## Screenshot

![Toast](screen/toast.png)
![Notification](screen/notification.png)

# fblogin_swift2
Basic Swift 2 application using the Facebook 4.8 SDK

###Follow the [Facebook Quick Start](https://developers.facebook.com/quickstarts/?platform=ios).

1. **Don't forget to import the frameworks and select "Copy items if needed" in the Options.**
2. Copy the settings from the Facebook Quick Start into your applications's plist file.
3. In ViewController.swift file `import FBSDKLoginKit` and add the following code to the viewDidLoad method:
```
let loginButton = FBSDKLoginButton.init()
loginButton.center = self.view.center
self.view.addSubview(loginButton)
```
4. In AppDelegate.swift `import FBSDKShareKit` and add the following method:
```
func application(application: UIApplication, openURL url: NSURL, sourceApplication: String?, annotation: AnyObject) -> Bool {
        return FBSDKApplicationDelegate.sharedInstance().application(
            application,
            openURL: url,
            sourceApplication: sourceApplication,
            annotation: annotation)
    }
```
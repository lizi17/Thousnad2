PasscodeLock
=========
##Intrudoction

![screenshot](https://raw.github.com/ch8908/Thousnad2/master/PasscodeLock/demoImage.jpg)

This project shows you how to create a "Passcode Lock" window.

You can custom your "Passcode Lock" view via customizng **AbstractPasscodeLockViewController**


##How to use:

####Create "Passcode Lock" related view controllers

* Create your "Passcode Lock" view controllers by inheriting **AbstractPasscodeLockViewController**. You should have 3 view controllers for:
  1. Enable passcode lock.
  2. Change passcode.
  3. Verify passcode.  


* Implement <code>- (void) onFilled:(NSString*) result </code> in each ViewControllers. <code>- (void) onFilled:(NSString*) result </code> will be called when user input 4 digits. This is where you can verify the passcode.

###Show "Passcode Lock" window

* Create a instance of **PasscodeLockWindow** class at <code>youAppNameAppDelegate.m</code>.  
```objc
@property (nonatomic, readwrite, retain) PasscodeLockWindow* passcodeLockWindow;
```

* Using the method <code>[self.passcodeLockWindow show]</code> to show up the "Passcode Lock" window.
```objc
- (void) applicationDidEnterBackground:(UIApplication*) application
{
      [self.passcodeLockWindow show];
}
```

##Requirements
* iOS >= 4.3
* non-ARC

[View the original post](http://ch8908.github.com/blog/2013/01/27/passcodelock/)
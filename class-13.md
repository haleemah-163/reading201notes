#### The past, present and future of local storage for Web Applications 
##### Cookies are limited to about 4 KB of data — enough to  
##### slow down your application (see above), but not enough to be terribly useful
##### From your JavaScript code, you’ll access HTML5 Storage through the localStorage
#####  object on the global window object. Before you can use it, you should
##### detect whether the browser supports it :
#### Check for HTML5 Storage 
 ``` function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
} 
```
##### or using Modernizer:
``` if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
} 
``` 
##### If you want to keep track programmatically of when the storage area changes,
#####  you can trap the storage event. The storage event is fired on the window 
#####  whenever setItem(), removeItem(), or clear() is called and actually changes something. 
##### For example, if you set an item to its existing value or call clear() when there
#####  are no named keys, the storage event will not fire, because nothing actually 
##### changed in the storage area.
##### The storage event is not cancelable. From within the handle_storage callback function,
##### there is no way to stop the change from occurring. It’s simply a way for the browser 
##### to tell you, “hey, this just happened. There’s nothing you can do about it now;
#####  I just wanted to let you know.”
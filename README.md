Blank Intel XDK HTML5 Web App Project
=====================================

See [LICENSE.md](<LICENSE.md>) for license terms and conditions.

Project File Information
------------------------

The `icon.png` and `screenshot.png` files are not required by your project.
They are included for use by the Intel XDK template/demo panel and have no use
within a real app. You can safely delete them from your project directory.

Uncomment the `cordova.js` script file reference inside the `index.html` file
if you want to convert this app into a Cordova app, which will provide your
app with access to Cordova APIs. You must use the "upgrade to Cordova" option
on the **Projects** tab to convert this project to a Cordova project. Once
that has been done you can add Cordova APIs to your application by using the
*Plugins* section on the **Projects** tab.

Project Details
---------------

Use this project as a starting point for an Intel XDK HTML5 mobile web app.
One key file (`init-dev.js`) contains the initialization code needed to manage
the "ready" event. This file manages the Cordova "deviceready" event and the
standard browser "documentready" event init events in a way that allows you to
run your app in either a Cordova or web app environment. This init code works:

* within the the Intel XDK Simulate tab (and old Emulate tab)

* in the Intel XDK App Preview application (Test tab)

* when you run your app inside a standard Browser

* in an app built using Apache Cordova (aka Cordova CLI) of PhoneGap

When `init-dev.js` completes execution it issues a custom `app.Ready` event.
Use this event to start your application, rather than waiting on "deviceready"
or "documentready" or "windowload" or similar events. You should not have to
modify anything in `init-dev.js` to use this code. Also, `init-dev.js` has
been written so that it is not dependent on any external libraries or specific
webviews. It has been tested with the following webviews and browsers:

* Android 2.3, 4.0-4.3, 4.4, 5.x, 6.x and 7.x

* iOS 6, 7, 8, 9 and 10

* Windows 8 Phone, Windows 8.x and Windows 10

* Crosswalk

* Chrome Desktop Browser

* Internet Explorer 10 and 11 and Microsoft Edge

This blank project works well for converting an existing web app into a mobile
web app. One of the biggest issues encountered when porting a web app to a
mobile app is resolving the init sequence of the web app with the init
sequence required of a mobile app. This gets especially difficult when large
third-party libraries are part of the app. Due to the additional burden of
initializing the underlying native code layer, developers sometimes have
trouble getting their code that runs in a desktop browser to initialize in an
HTML5 hybrid webview. Frequently this is due to the significant difference in
resources between the desktop browser and the mobile webview (e.g., less
memory, lower performance and a reduced feature set).

There are many comments in the files in this project. Please read those
comments for details and further documentation. In particular, see the
comments in the `index.html` file for recommendations on how to load your
third-party libraries relative to your application code and the special
Cordova library.

There are a large number of `console.log()` messages contained within
`init-dev.js`. They can be used to debug initialization problems and understand
how the file works. It is highly recommended that you leave those
`console.log()` messages in that file, they will not unduly slow down or burden
your application. Set `dev.LOG = true` to enable the `console.log()` messages in
`init-dev.js` and set it to false for release code, it is normally set to false.

BTW: the "`dev`” prefix refers to "device" in this context, not "develop,"
because it grew out of a desire to build a more reliable and flexible "device
ready" detector.

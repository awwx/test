---
layout: page
title: foo
---

For example, consider what happens when a user navigates to the app's web page for the first time, when they don't have the application cached yet. The browser will load the app as if it were a standard online application not using an app cache; and then the browser will also populate the app cache in the background. The second time the user opens the web page the browser load the app from the cache. Why? Because the browser never waits for the app cache to loaded. The first time the user opens the page the cache hasn't been loaded yet, and so the browser loads the page incrementally from the server as it does for web pages that aren't cache enabled.

As another example, suppose the user has previously opened the web page and so has an old copy of the application in the app cache. The user now returns to the web page, and in the meantime a new version of the application has been published. What happens? Since the browser never waits for the app cache, it will at first display the old version of the web page. Then, as Meteor makes its livedata connection and sees that a code update is available, the page will reload with the new code.

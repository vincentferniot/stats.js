Stats.js
========

#### Javascript Performance Monitor ####


This class provides a simple info box that will help you monitor your code performance.

* **FPS** Frames rendered in the last second. The higher the number the better.
* **MS** Milliseconds needed to render a frame. The lower the number the better.
* **MB** MBytes of memory allocated. Make sure it doesn't keep incrementing. (Webkit-based browsers only)


### Screenshots ###

![stats_js_fps.png](http://mrdoob.github.com/stats.js/assets/stats_js_fps.png)
![stats_js_ms.png](http://mrdoob.github.com/stats.js/assets/stats_js_ms.png)
![stats_js_mem.png](http://mrdoob.github.com/stats.js/assets/stats_js_mem.png)


### Usage ###

	var stats = new Stats();

	// Align top-left
	stats.domElement.style.position = 'absolute';
	stats.domElement.style.left = '0px';
	stats.domElement.style.top = '0px';

	parentElement.appendChild( stats.domElement );

	setInterval( function () {

		stats.update();

	}, 1000 / 60 );


### Enable MB ###

* **Chrome**
  * Linux: `/opt/google/chrome/google-chrome --enable-memory-info`
  * Windows: `"C:\Program Files\Google\Chrome\Application\chrome.exe" --enable-memory-info`
  * MacOS: `/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --enable-memory-info`

* **Safari** 
  * MacOS: Open `~/Library/Preferences/com.apple.Safari.plist` file for editing, and add & set enabled a boolean preference *WebKitMemoryInfoEnabled* ([pic](http://mrdoob.github.com/stats.js/assets/safari_enablemem.png))


### Bookmarklet ###

Albeit theorically not as accurate the widget can also be easily inserted to **any site** using the bookmarklet.
[Follow the instructions](http://mrdoob.com/blog/post/707).


### Change Log ###

2011 05 28 - **r6** (4.103 KB, gzip: 1.384 KB)

* Updated check for memory accesible browsers.
* Renamed MEM to MB for consistency reasons.


2010 09 21 - **r5** (3.800 KB)

* Different color per mode.
* Added MEM mode. (Webkit-based browsers only)
* Force text left aligned.


2010 06 11 - **r4** (2.235 KB)

* Added MS mode.


2010 05 12 - **r3** (1.241 KB)

* Switched to module pattern code style.
* Removed `position = 'absolute'`.


2010 03 01 - **r2** (2.177 KB)

* Simplified.


2010 02 21 - **r1**

* Accurate FPS calculation. (thx Spite!)

 
2009 08 09 - **r0**

* Base code.

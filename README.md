# HiGoogleFonts
HiGoogleFonts allows you to add a Google font picker to easily display a list of Google fonts. This font picker is used along with our select jQuery plugin. The picker shows an instant preview of the font style without loading the font.

[Demo](https://cdn.rawgit.com/saadqbal/HiGoogleFonts/master/index2.html)
======


Usage
======

To use the HiGoogleFonts library, just include the code below in your in your page in **_5 easy steps_**. Check the index for a simple example:

Step 1.
------

Clone Repo: `git clone https://github.com/saadqbal/HiGoogleFonts.git`

Step 2.
-------

Install dependencies: `bower install`

Step 3.
-------

Include the style sheet. Add the following line into your page header:
```javascript
<link rel="stylesheet" href="css/fonts.css">
```

Step 4.
-------

Include the required libraries. Add the following lines into your page header after style sheets:
```javascript
<script src="https://code.jquery.com/jquery-1.12.0.min.js"></script>
 <script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.3/js/select2.full.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/webfont/1.5.18/webfont.js"></script>
<script src="js/fonts.js"></script>

```


Step 5.
-------

Now add the code below to the body to load all the fonts:


```javascript

<select id="select_fontfamily"></select>
<p style="font-size: 20px;">This is the preview of the font selected</p>


<script type="text/javascript">
$(document).ready(function() {

	$( "#select_fontfamily" ).higooglefonts({			
		selectedCallback:function(e){
			console.log(e);
		},
		loadedCallback:function(e){
			console.log(e);
			$("p").css("font-family", e);
		}			
	});

  });

</script>
```


npm and bower
==============

**npm**

  * `$ npm install higooglefonts`

**bower**  
  * `bower install higooglefonts`



Events
======

HiGoogleFonts provides an event system that developers can hook into. It gives you notifications of the font loading sequence.

  * `selectedCallback` - This event is triggered when a font is selected but not yet loaded.
  * `loadedCallback` - This event is triggered when the font is loaded and is ready to be applied. This is where you should apply font to an element.


Bug tracker
-----------

Have a bug? Please create an issue here on GitHub.

https://github.com/saadqbal/HiGoogleFonts/issues


Authors
-------

**Asad Iqbal**

+ http://twitter.com/saadqbal
+ http://github.com/saadqbal



Copyright and license
---------------------

Copyright 2016 Hiwaas, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

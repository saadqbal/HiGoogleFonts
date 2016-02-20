# HiGoogleFonts
HiGoogleFonts allows you to add a Google font picker to easily display a list of Google fonts. This font picker is used along with our select jQuery plugin. The picker shows an instant preview of the font style without loading the font.


Usage
======

To use the HiGoogleFonts library, just include the code below in your in your page in **_3 easy steps_**. Check the index for a simple example:

Step 1.
------

Include the style sheets. Add the folowing lines into your page header:
```javascript
<link rel="stylesheet" href="css/select2.css">
<link rel="stylesheet" href="css/fonts.css">
```

Step 2.
------

Include the required libraries. Add the folowing lines into your page header after style sheets:
```javascript
<script src="js/jquery.js"></script>
<script src="js/select2.full.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/webfont/1.5.18/webfont.js"></script>
<script src="js/fonts.js"></script>
   
```


Step 3.
------

Include the required libraries. Add the folowing lines into your page header after style sheets:

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
	}); // Makes all the links green.

  }); 
  
</script>
```

Events
======

HiGoogleFonts provides an event system that developers can hook into. It gives you notifications of the font loading sequence.

  * `selectedCallback` - This event is triggered when a font is selected but not yet loaded.
  * `loadedCallback` - This event is triggered when the font is loaded and is ready to be applied.
 
  
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
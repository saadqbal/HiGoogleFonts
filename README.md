# HiGoogleFonts
HiGoogleFonts allows you to add a Google font picker to easily display a list of Google fonts. This font picker is used along with our select jQuery plugin. The picker shows an instant preview of the font style without loading the font.


Usage
-----------

To use the HiGoogleFonts library, just include the code below in your in your page before the body close tag. Check the index for a simple example:



```javascript
<script src="js/jquery.js"></script>
    <script src="js/select2.full.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/webfont/1.5.18/webfont.js"></script>
    <script src="js/fonts.js"></script>
    <link rel="stylesheet" href="css/select2.css">
     <link rel="stylesheet" href="css/fonts.css">
    <script type="text/javascript">
    $(document).ready(function() {
     
		$( "#select_fontfamily" ).higooglefonts({
			selectId: "#select_fontfamily",
			selectedCallback:function(e){
				console.log(e);
		    },
			loadedCallback:function(e){
				console.log(e);
				$("p").css("font-family", e);
		    }			
		}); // Makes all the links green.

      }); /// documentReady() ends here
	  
    </script>
```


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
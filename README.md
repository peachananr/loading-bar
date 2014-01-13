#Loading Bar by Pete R.
A little jQuery plugin that will let you add a Youtube-like loading bar to all your ajax links 
Created by [Pete R.](http://www.thepetedesign.com), Founder of [BucketListly](http://www.bucketlistly.com)

License: [Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/deed.en_US)

[![Loading Bar](http://www.thepetedesign.com/images/loading_bar_image.png "Loading Bar")](http://www.thepetedesign.com/demos/youtube_loadingbar_demo.html)


## Demo
[View demo](http://www.thepetedesign.com/demos/youtube_loadingbar_demo.html)

## Usage
To add a Youtube-like loading bar to your website, simply include the latest jQuery library found [here](http://jquery.com/download/) together with `jquery.loadingbar.js` and `loadingbar.css` into your document's `<head>` and simply call the function as shown below:
  
````javascript
$(".ajax-call").loadingbar({
  replaceURL: false, /* You can visibly change the URL of the browser to reflect the clicked links by toggling this to true. Default is false. May not work in old browsers. */
	target: "#loadingbar-frame", /* The container's selector where you want the ajax result to appear. Default is #loadingbar-frame */
	direction: "right", /* The direction where the the loading bar will progress. Default is right. */
	
	/* Default Ajax Parameters.  */
	async: true, 
	complete: function(xhr, text) {},
	cache: true,
	error: function(xhr, text, e) {},
	global: true,
	headers: {},
	statusCode: {},
	success: function(data, text, xhr) {},
	dataType: "html",
	done: function(data) {}
});
````
Note: For options listed under Default Ajax Parameters, simply refer to [jQuery.ajax doc](http://api.jquery.com/jQuery.ajax/) for more info. 

For HTML markups, all you need is a link and a container to show the result:
  
````html
<a href="YOUR-URL" class="ajax-call">..</a>
<div id="loadingbar-frame"></div>
````
Make sure you change the "YOUR-URL" into the URL you want the script to load. 


## Further Customization
Sometime you may want each links to have its own ajax command, for example one for `POST` and another for `GET`. With this script you can do this by simply following markup rules as shown in the example below:

````html
<a href="http://api.dribbble.com/players/jackietrananh/shots?callback=?" 
data-datatype="json" data-type="GET" data-target="#frame">Click Me</a>
````
This example shows how I was able to call the Dribbble's API with a data markup. Simply assign `data-target` with a selector to define the target container, `data-type` to define the type of ajax call you want and `data-datatype` to define the type you want to receive. 

Now, each individual links will perform using its own settings.

## Other Resources
- Tutorial (Coming Soon)

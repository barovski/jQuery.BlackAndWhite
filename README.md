This plug-in can easily convert every colored image (in an html page) into a B&W greyscale image.
Read the plugin API on here http://www.gianlucaguarini.com/canvas-experiments/jQuery.BlackAndWhite/demo.html.

#Usage

1 Include the plug into the page:


<pre>
    &lt;script src="js/jQuery.BlackAndWhite.js"&gt;&lt;/script&gt;
</pre>

2 Set the image wrappers using the css:

<pre>
.bwWrapper {
    position:relative;
    display:block;
}
</pre>

3 Initialize the plug in on window load (no <code>$(document).ready()</code>):



<pre>
$(window).load(function(){
    $('.bwWrapper').BlackAndWhite({
        hoverEffect : true, // default true
        // set the path to BnWWorker.js for a superfast implementation
        webworkerPath : false,
        // for the images with a fluid width and height 
        responsive:true,
        // to invert the hover effect
        invertHoverEffect: false,
        speed: { //this property could also be just speed: value for both fadeIn and fadeOut
            fadeIn: 200, // 200ms for fadeIn animations
            fadeOut: 800 // 800ms for fadeOut animations
        },
        onImageReady:function(img) {
        	// this callback gets executed anytime an image is converted
        }
    });
});
</pre>



## IMPORTANT

the script works only for the images hosted on the same server in which the page is loaded!


## Plugin Showcase


*   [Teocomi.com](http://teocomi.com/photos/)
*   [Deejay.it](http://www.deejay.it/dj/extra/widget)
*   [United Designers](http://www.unitedesigners.it/#!/124-tailored-branding)

If your want add a new entry please fork this README file

---------



## THANKS

Thanks to Jeffrey Way for the inspiration ( http://jeffrey-way.com/ )

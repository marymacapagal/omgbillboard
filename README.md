#OMGBillboard

jQuery plugin for adding the old, blinds billboard effect to a set of images.
(You can see a working demo here: http://labs.marymacapagal.com/omgbillboard/)

##Licensing
Same license as jQuery (MIT). In a nutshell: you can use this plugin for free for any purpose you want. If it causes you any grief or damage, I'm not liable. (https://github.com/marymacapagal/omgbillboard/blob/master/MIT-License.txt)


##How to use
Just call OMGBillboard on a container with img elements like so:
```javascript
	$("#container").OMGBillboard();
```
The plugin will grab all `<img>` inside `#container` and put them on a rotating slideshow.


###Available settings
It would be better if you specify the image and height of your image:
```javascript
	$("#container").OMGBillboard({
		'imgHeight':750,
		'imgWidth':500
		});
```

And better-er if you go crazy and override these default options:
```javascript
	$("#container").OMGBillboard({
		'imgWidth': 600,
		'imgHeight': 400,
		'numSlices': 10,
		'sliceClass': 'slice',
		'rotateSpeed': 500,
		'changeSpeed': 5000,
		'bgColor': '#000'
	});
```

###Default values
* **imgWidth** and **imgHeight** - Integer values (in pixels) of the width and height of the billboard. Set this to the size of your images. Defaults are 600 and 400, respectively.
* **numSlices** - Integer. The number of slices to divide your images into. Default is 10.
* **sliceClass** - String. The CSS class to be assigned to slices. Default is **slice** but you can change it in case you're using that name somewhere else in your CSS.
* **rotateSpeed** - Integer in milliseconds of how long it takes to flip close and flip open an image. Default is 500 ms.
* **changeSpeed** - Integer in miliseconds of how long to display an image before replacing it with another one. Default is 5000 ms.
* **bgColor** - String. Any acceptable value for color in CSS. Default is #000.

###Multiple billboards in one page?
Yes you can!

Create billboards with the same settings:
```javascript
	$("#container, #bottom_ad, .sidebar_ads").OMGBillboard({
		'imgHeight':300,
		'imgWidth':700,
		'bgColor':'#f00'
	})
```

Or specify a different setting per container:
```javascript
	$("#container").OMGBillboard({'imgHeight':100, 'imgWidth':600});
	$(".sidebar_ads").OMGBillboard({'imgHeight':600, 'imgWidth':200});
	$("#bottom_ad").OMGBillboard({'imgHeight':250, 'imgWidth':1000, 'bgColor':'orange'});
```


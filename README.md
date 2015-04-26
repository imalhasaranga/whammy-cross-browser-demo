#whammy cross browser demo 

Currently whammy webm encoder supports only for the browsers which support webp image format
but at this moment only chrome and opera are the only browsers that support for webp format. 

this effort is to show that with some slight modification we still can use whammy.js to run in all the browsers.

How to use 

```

//how to initialize
var whammy_cross = new WhammyCrs();
whammy_cross.reset();
whammy_cross.progress = function(presentatge){
	//calls when webm encodes and shows presentage	
}

whammy_cross.onConvert = function(convetedcount){
	//number of frames converted 
}


//according to a specific rate each frame data should pass to whammy_cross object

whammy_cross.addFrame(ctxz.getImageData(0,0,w,h).data,w,h);

//at the end, encode for webm
whammy_cross.setFrameRate(framerate);
whammy_cross.encodeWEBM(function(videoBlob){
		var url = window.URL.createObjectURL(videoBlob);
		document.getElementById('awesome').src = url; 
		document.getElementById('download').style.display = '';
		document.getElementById('download').href = url;
});

```

#### Supported Browsers 

1. IE > 10
2. Chrome 
3. Opera 
4. Firefox
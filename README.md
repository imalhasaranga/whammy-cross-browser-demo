#whammy cross browser demo 

Currently whammy webm encoder supports only for the browsers which support webp image format
but at this moment only chrome and opera are the only browsers that support for webp format. 

this effort is to show that with some slight modification we still can use whammy.js to run in all the browsers.

##### FUTURE IMPROVEMENTS 

when running this file in your local browser you will notice that first clock tick takes lot of time and having a performance problem
that is because I'm encoding the image retrived by the canvs to webp manually using  'libwebp-0.1.3.min.js'  but my understanding is that by using a web worker 
we can avoid this issue. 
I'll try to implement it soon. 
#rorriM Web
.bew fo noisrev tnereffid a su evig
give us a different version of web.
##Usage
 - Step 1
     - Download or copy the source code down until you get rorrim.html file.
 - Step 2
     - Use a browser to open it. And you will get a mirrored web page.
 - Step 3
     - Add: "?" + your destination behind url, 
     - e.g. 
         - .../rorrim.html?www.bilibili.com

#####Have fun.
##Keywords
CSS,HTML
##Details
```css

	<html>
	<head>
	    <title>mirror</title>
	    <style type="text/css" media="screen">
	        #iframe {
	
	            /* several filter for different version of browser*/
	            -webkit-transform: matrix(-1,0,0,1,0,0);/* Safari & Chrome */
	            -moz-transform: matrix(-1,0,0,1,0,0);   /* Firefox */
	            -ms-transform: matrix(-1,0,0,1,0,0);    /* IE 9 */
	            transform: matrix(-1,0,0,1,0,0);        /* Internet Explorer 10、Firefox、Opera */
	            -o-transform: skew(0deg, 180deg) scale(-1,1);   /* Opera */
	
	            /* IE */
	            position: absolute;
	            filter: progid:DXImageTransForm.Microsoft.BasicImage(mirror 1);
	
	            /* fill the screen*/
	            width: 100%;
	            height: 100%;
	            top: 0px;
	            left: 0px;
	
	            /* disable the border */
	            border: none;
	        }
	    </style>
	</head>
	<body>
	    <iframe id="iframe" src="http://www.bilibili.com"></iframe>
	    <script type="text/javascript">
	        var str = location.href;                 /* get url in browser*/
	        str = str.indexOf("?") != -1 ? str.substr(str.indexOf("?") + 1) : "";
	        /* find and get the parameters after */
	        if (str.length > 0)
	            document.getElementById('iframe').src = "http://" + str;
	    </script>
	</body>
	</html>

```

The total code is short here. The main code we write here is in CSS, These filters here is in every version of browser to do the mirror effect. 

Else part is to ignore the border of the iframe and made it full the screen.




 
 
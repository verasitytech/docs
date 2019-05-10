# Youtube - integration with iframe
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Youtube_iframe.png)
 
1. Add Youtube Iframe API script tag to the page
```
<script src="https://www.youtube.com/iframe_api"></script>
```

2. Add SDK script tag to the page
```
<script src=“https://nobuffer.net/sdk/kilosdk.js"></script>
```

3. Add iframe for the video you want to use
3.1. Get the iframe code. On the Youtube video page: Share > Embed
3.2. Add the id parameter to the iframe element
3.3. Enable Youtube Iframe API: add ```?enablejsapi=1``` to the video URL parameter

4. Create the function that will run once the Youtube API finished loading (use exact name, as per Youtube API)
```
function onYouTubeIframeAPIReady() {}
```

5. Initialise SDK
```
kilosdk.init({
		videoId: <unique video id>,
		player: { type: 'YoutubePlayer',
			instance:  <iframe id>,
		modules: [{type: 'Reward'}]
});
```

# Youtube - integration with Youtube Player API
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Youtube_api.png)
 
1. Add Youtube Iframe API script tag to the page
```
<script src="https://www.youtube.com/iframe_api"></script>
```

2. Add SDK script tag to the page
```
<script src=“https://nobuffer.net/sdk/kilosdk.js"></script>
```

3. Create a placeholder div for embedding Youtube Player

4. Create the function that will run once the Youtube API finished loading (use exact name, as per Youtube API)
```
function onYouTubeIframeAPIReady() {}
```

5. Create Youtube Player instance
```
let player = new YT.Player(<placeholder div id>, {
		height: <video height>,
		width: <video width>,
		videoId: <Youtube video id>
});
```

6. Initialise SDK
```
kilosdk.init({
		videoId: <unique video id>,
		player: { type: 'YoutubePlayer',
			instance:  <Youtube player instance>,
		modules: [{type: 'Reward'}]
});
```


#### Youtube Iframe API

You can check Youtube Iframe API docs here: [https://developers.google.com/youtube/iframe_api_reference](https://developers.google.com/youtube/iframe_api_reference)
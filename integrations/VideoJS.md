# Video JS Integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/VideoJS.png)
 
1. Add VideoJS stylesheet and script tags to the page
```
<link href="https://vjs.zencdn.net/7.4.1/video-js.css" rel="stylesheet">
<script src="https://vjs.zencdn.net/7.4.1/video.js"></script>
```

2. Add SDK script tag to the page
```
<script src="https://nobuffer.net/sdk/kilosdk.js"></script>
```

3. Add video element to the page

4. Create a VideoJS Player instance and pass it to SDK. You can check the VideoJS docs for additional configuration options
```
instance: videojs(<video element id>, {controls: true})
```

5. Initialise SDK
```
kilosdk.init({
	videoId: <unique video id>,
	player: { type: 'VideoJSPlayer',
		instance:  videojs(<video element id>, {controls: true}),
	},
	modules: [{type: 'Reward'}]
});
```


#### Video JS Docs

[https://videojs.com](https://videojs.com)
Documentation main page: [https://docs.videojs.com ](https://videojs.com)
Player setup: [https://docs.videojs.com/tutorial-setup.html](https://videojs.com)

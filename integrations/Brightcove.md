# Brightcove Integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Brightcove.png)
 
1. Add SDK script tag to the page
```
<script src="https://nobuffer.net/sdk/kilosdk.js"></script>
```

2. Add Brightcove Player to the page; add the id parameter to the element

3. Initialise SDK
```
kilosdk.init({
		videoId: <unique video id>,
		player: { type: 'VideoJSPlayer',
			instance: videojs(<brightcode element id>)},
		modules: [{type: 'Reward'}]
});
```

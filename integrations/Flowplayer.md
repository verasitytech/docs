# Flowplayer Integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Flowplayer.png)
 
1. Add SDK script tag to the page
```
<script src="https://nobuffer.net/sdk/kilosdk.js"></script>
```

2. Add Flowplayer to the page; add the id parameter to the flowplayer div element

3. Initialise SDK
```
kilosdk.init({
	videoId: <unique video id>,
	player: { type: 'FlowplayerPlayer',
		instance: <flowplayer div element>
	},
	modules: [{type: 'Reward'}]
});
```

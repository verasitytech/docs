# Vimeo Player Integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Vimeo.png)
 
1. Add SDK script tag to the page
```
<script src=“https://nobuffer.net/sdk/kilosdk.js"></script>
```

2. Add Vimeo script tag to the page
```
<script src="https://player.vimeo.com/api/player.js"></script>
```

3. Add placeholder div for embedding Vimeo video

4. Create Vimeo Player instance and pass it to SDK
```
instance: new Vimeo.Player(document.getElementById(<div element id>), {
		url: <vimeo video URL>,
		width: <player width>
});
```

5. Initialise SDK
```
kilosdk.init({
		videoId: <unique video id>,
		player: { type: 'VimeoPlayer',
			instance: new Vimeo.Player(
					document.getElementById(<div element id>),
					{url: <vimeo video URL>, width: <player width>}
			)
		},
		modules: [{type: 'Reward'}]
});
```
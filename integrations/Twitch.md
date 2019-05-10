# Twitch Player integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Twitch.png)
 
1. Add SDK script tag to the page
```
<script src="https://nobuffer.net/sdk/kilosdk.js"></script>
```

2. Add placeholder div for embedding Twitch Player

3. Add Twitch Player API script tag to the page
```
<script src= "https://player.twitch.tv/js/embed/v1.js"></script>
```

4. Create Twitch Player object
```
new Twitch.Player(<placeholder div id (from step 2)>, {
	width: <player width>,
	height: <player height>,
	video: <video ID from Twitch>
});
```

5. Initialise SDK
```
kilosdk.init({
	videoId: <unique video id>,
	player: { type: 'TwitchPlayer',
		instance: <Twitch Player instance>,
	},
	modules: [{type: 'Reward'}]
});
```

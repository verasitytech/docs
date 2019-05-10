# JWPlayer Integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/JWPlayer.png)
 
1. Add SDK script tag to the page
```
<script src=“https://nobuffer.net/sdk/kilosdk.js"></script>
```

2. Add JWPlayer script tag to the page
```
<script src=“https://content.jwplatform.com/libraries/<your JWPlayer lib ID>.js"></script>
```

3. Add placeholder div element for embedding JWPlayer

4. Setup JWPlayer
```
jwplayer(<div element id (step 3)>).setup({
		file: <video URL>,
		Image: <poster URL>,
		height: <video height>,
		width: <video width>
});
```

5. Initialise SDK
```
kilosdk.init({
		videoId: <unique video id>,
		player: { type: 'JWPlayer',
			instance: jwplayer(<div element id (step 3)>)},
		modules: [{type: 'Reward'}]
});
```

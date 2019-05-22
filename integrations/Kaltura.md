# Kaltura Player Integration
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/Kaltura.png)

1. Add Kilo SDK script tag to the page
```
<script src="https://nobuffer.net/sdk/kilosdk.js"></script>
```

2. Add Kaltura embed code to the page

3. Initialize Kilo SDK
```
kilosdk.init({
	videoId: <unique video id>,
	player: { type: 'KalturaPlayer',
		instance: document.getElementById(<katura div id>)
	},
	modules: [{type: 'Reward'}]
});
```

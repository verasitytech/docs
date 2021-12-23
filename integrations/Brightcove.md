# Brightcove integration
## Using VeraPlayer with Brightcove content

To use Verasity player on your web site and be able to playback videos from your Brightcove account simply add the following iframe to the destination web page:
```
<iframe src="https://nobuffer.net/b-player/?v=01234567890123&cid=abcd1234efgh" id="verasity_player" allowfullscreen=""></iframe>
```
URL from iframe src attribute has parameters that are passed to the player.

```v=01234567890123``` video id from Brightcove, change 01234567890123 to the actual id of the video you'd like to play

```cid=abcd1234efgh``` client id, contact us via player@verasity.io to obtain your client id.

### &nbsp;
### &nbsp;

## Adding Rewards to Brightcove player

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
		instance: videojs(<brightcode element id>)
	},
	modules: [{type: 'Reward'}]
});
```

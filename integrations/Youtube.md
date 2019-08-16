# Youtube - integration with iframe
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/youtube_player_integration_with_iframe.png)

    <script src="https://nobuffer.net/sdk/kilosdk.js"></script>
    <iframe id="[YOUTUBE_PLAYER_CONTAINER_ID]" src="[YOUTUBE_PLAYER_SRC]?enablejsapi=1"></iframe>
    <script>
        kilosdk.init({
            videoId: '[VIDEO_ID]',
            player: {
                type: 'YoutubePlayer',
                instance: '[YOUTUBE_PLAYER_CONTAINER_ID]'
            },
            modules: [{type: 'Reward'}]
        });
    </script>

####1. Add SDK script tag to the page

    <script src="https://nobuffer.net/sdk/kilosdk.js"></script>

####2. Add iframe of the video you want to use

1. Get the iframe code. On the Youtube video page: Share > Embed
2. Add the id parameter to the iframe element
3. Enable Youtube Iframe API: add `?enablejsapi=1` to the video URL parameter

####3. Initialise SDK

    kilosdk.init({
        videoId: '[VIDEO_ID]',
        player: { type: 'YoutubePlayer',
            instance:  '[YOUTUBE_PLAYER_CONTAINER_ID]',
        },
        modules: [{type: 'Reward'}]
    });

# Youtube - integration with Youtube Player API
![image](https://raw.githubusercontent.com/verasitytech/docs/master/integrations/img/youtube_player_integration_with_player_api_result.png)

    <script src="https://nobuffer.net/sdk/kilosdk.js"></script>
    <div id="[YOUTUBE_PLAYER_CONTAINER_ID]"></div>
    <script>
        var YOUTUBE_PLAYER_PROPERTIES = {
            height: '[VIDEO_HEIGHT]',
            width: '[VIDEO_WIDTH]',
            videoId: '[YOUTUBE_VIDEO_ID]'
        };
        kilosdk.init({
            videoId: '[VIDEO_ID]',
            player: {
                type: 'YoutubePlayer',
                instance: '[YOUTUBE_PLAYER_CONTAINER_ID]',
                option: YOUTUBE_PLAYER_PROPERTIES
            },
            modules: [{type: 'Reward'}]
        });
    </script>

####1. Add SDK script tag to the page

    <script src="https://nobuffer.net/sdk/kilosdk.js"></script>

####2. Create a div for embedding Youtube Player with id

    <div id="[YOUTUBE_PLAYER_CONTAINER_ID]"></div>

####3. Prepare an object containing following properties:
               
- `width` (number) – width of the video player. Default value is 640.
- `height` (number) – height of the video player. Default value is 390.
- `videoId` (string) – YouTube video ID that identifies the video that the player will load.
- `playerVars` (object) – object containing properties that can be used to customize the player.
- `events` (object) – object containing properties of events that API fires and functions (event listeners) that API will call when those events occur. In example, constructor indicates that nPlayerReady function will execute when onReady event fires and that onPlayerStateChange function will execute when onStateChange event fires.

#####3.1 Copy videoId

Get the `videoId`. On the Youtube video page click `Share` button and copy `[YOUTUBE_VIDEO_ID]` from URL like `https://youtu.be/[YOUTUBE_VIDEO_ID]` or from browser address bar.

#####3.2 Initialise the object

    var YOUTUBE_PLAYER_PROPERTIES = {
        height: '[VIDEO_HEIGHT]',
        width: '[VIDEO_WIDTH]',
        videoId: '[YOUTUBE_VIDEO_ID]'
    };

####4. Initialise SDK

    kilosdk.init({
        videoId: '[VIDEO_ID]',
        player: {
            type: 'YoutubePlayer',
            instance: '[YOUTUBE_PLAYER_CONTAINER_ID]',
            option: YOUTUBE_PLAYER_PROPERTIES
        },
        modules: [{type: 'Reward'}]
    });

<br>

### Youtube Iframe API

You can check Youtube Iframe API docs here: [https://developers.google.com/youtube/iframe_api_reference](https://developers.google.com/youtube/iframe_api_reference)

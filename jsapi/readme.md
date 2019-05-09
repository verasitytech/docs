# Rewards JavaScript API

### Methods:

#### on
method lets you subscribe to any SDK event

```kilosdk.on('sampleEvent', eventListener);```

`'sampleEvent'` - string defining event type

`eventListener` - listener function that should be called when event is emitted

##### Event listener

```
(data) => {
    // event emited, do something...
}
```

`data` - object holding values passed from SDK with the event. Data object always holds `videoId` and 'playerId' parameters to make it easier to identify particular player instance on a page with multiple players.

`data.videoId` - an id that identifies your video content (is unique for each video) and initially is passed to SKD on instantiation.

`data.playerId` - an id that identifies particular player instance on the page, if not set explicitly on SDK instantiation - will be random number

#### off
method allows you to unsubscribe from any SDK event

```kilosdk.off('sampleEvent', eventListener);```

### Event types:

#### 'ready'
emitted when particular instance of rewarding module is fully initialized

##### event data:
`data.videoId` - an id that identifies your video content (is unique for each video) and initially is passed to SKD on instantiation.

`data.playerId` - an id that identifies particular player instance on the page, if not set explicitly on SDK instantiation - will be random number

#### 'registrationComplete'
emitted when user has successfuly created account in rewarding module and confirmed email address

##### event data:
`data.videoId` - an id that identifies your video content (is unique for each video) and initially is passed to SKD on instantiation.

`data.playerId` - an id that identifies particular player instance on the page, if not set explicitly on SDK instantiation - will be random number

#### 'reward'
emitted when rewarding module tries to reward the user only occurs for signed in users

##### event data:
`data.success` - `true` if user received a reward, `false` if user was not given a reward, for example if user got maximum allowed number of rewards already.

`data.videoId` - an id that identifies your video content (is unique for each video) and initially is passed to SKD on instantiation.

`data.playerId` - an id that identifies particular player instance on the page, if not set explicitly on SDK instantiation - will be random number

#### 'videoComplete'
emitted at the very end of video content playback, means that viewer has reached 100% mark of video content timeline

##### event data:
`data.rewarded` - `true` if user received a reward during watching this video `false` in any other situation (no reward given, user not signed in, etc.)

`data.videoId` - an id that identifies your video content (is unique for each video) and initially is passed to SKD on instantiation.

`data.playerId` - an id that identifies particular player instance on the page, if not set explicitly on SDK instantiation - will be random number

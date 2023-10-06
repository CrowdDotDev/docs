# Slack integration

## Data tracked

Activities

* When a member joins a channel
* Messages
* Replies in threads

Historical import

* No limitation

Not tracked

* Reactions

Refresh period

* 20 minutes.

## How to install

To connect Slack with crowd.dev, watch this video or follow the outlined steps below: \[block:embed] { "html": "\<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2F3gnKRoGf2bw%3Ffeature%3Doembed\&display\_name=YouTube\&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D3gnKRoGf2bw\&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2F3gnKRoGf2bw%2Fhqdefault.jpg\&key=f2aa6fc3595946d0afc3d76cbbd25dc3\&type=text%2Fhtml\&schema=youtube" width="854" height="480" scrolling="no" title="YouTube embed" frameborder="0" allow="autoplay; fullscreen" allowfullscreen="true">", "url": "https://www.youtube.com/watch?v=3gnKRoGf2bw", "title": "How to track messages and reactions in your Slack | crowd.dev", "favicon": "https://www.google.com/favicon.ico", "image": "https://i.ytimg.com/vi/3gnKRoGf2bw/hqdefault.jpg" } \[/block]

### 1. Connect Slack bot

Go to the [Integration settings](https://app.crowd.dev/integrations) and follow the steps to connect Slack.

### 2. Add Slack bot to channels

To fetch data from Slack, you need to add the crowd.dev Slack bot to all channels.

There are two options for this:

#### Option 2.1: Adding the bot directly from the channel

This is the quickest option if you do not have many channels. Simply go to the channel and type: @Crowd.dev and send the message. \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/f15f2e3-slack-1.png", "slack-1.png", 470, 85, "#aac9db" ] } ] } \[/block]\
A pop-up will appear. Simply click _Add to Channel_ and the bot will be able to get all messages from this channel. \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/c214dab-slack-2.png", "slack-2.png", 501, 258, "#eaefef" ] } ] } \[/block]\


#### Option 2.2: Adding from the channel settings

Alternatively, you can add the bot in bulk from the channel settings.

1. On the sidebar, right-click on the first channel where you would like the integration to be and click on _Open channel details_
2.  Head over to the _Integrations_ tab and click on _Add an App_ \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/3ba88aa-slack-3.png", "slack-3.png", 1132, 1450, "#efedea" ] } ] } \[/block]

    \

3.  Search for "Crowd.dev" and click on _Add app_ \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/8c9fab5-slack-4.png", "slack-4.png", 1386, 576, "#f5f6f6" ], "sizing": "80" } ] } \[/block]

    \

4. Once the app is added, if you go to the channel where you added the app you will see a message like this

\[block:image] { "images": \[ { "image": \[ "https://files.readme.io/4297cd0-slack-5.png", "slack-5.png", 904, 128, "#f8f7f5" ], "sizing": "80" } ] } \[/block]\
\
5\. Clicking on the logo, a menu will appear with an option to add the integration to more channels. \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/d8d9fbe-slack-6.png", "slack-6.png", 880, 502, "#b2b6bc" ], "sizing": "80" } ] } \[/block]\
6\. Now you can select the channel that you want to connect. \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/c050588-slack-7.png", "slack-7.png", 1096, 454, "#e0e1e0" ], "sizing": "80" } ] } \[/block]\
7\. Repeat steps 5 and 6 for each channel that you would like the Crowd.dev integration to have access to.

\-- That’s it! Crowd.dev can now fetch all messages and reactions from your Slack community. 🥳

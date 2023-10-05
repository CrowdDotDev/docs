# Conversations & Community Help Center

## Introduction

With [Conversations](https://app.crowd.dev/conversations), crowd.dev automatically detects discussions that are going on in your community. On the one hand, this will help you to **keep a better overview of discussed topics**. What's even more exciting is that you can use Conversations to **auto-generate Community Help Center**. Thereby, you can:

* Auto-generate support content
* Make your community discoverable by Google
* Reduce duplicate questions and support effort

Take a look at this [example](https://open.crowd.dev/crowd), which is created based on our Discord community.

## How to set-up

### General set-up

To set up your community help center, simply navigate to the [Conversations page](https://app.crowd.dev/conversations).

\[block:callout] { "type": "warning", "title": "Refresh settings", "body": "If you have used the Community Help Center before August 5, 2022, you have to refresh the Settings by saving them once. After this, you should be able to see the new Community Help Center settings (including auto-publishing)." } \[/block] Click _Settings_ and fill out the following details.\


**General**

* **Community Name**: Display name of your community
* **Community Slug**: Unique identifier for your community (will be later used to create your public URL: open.crowd.dev/{communitySlug} - can’t be changed later!\


**Community links**

* **Website**: URL of your community/company (the link behind Home)
* **Discord URL**: Permanent Discord invite link (will be used to let visitors join your Discord) - learn [here](https://support.discord.com/hc/en-us/articles/208866998-Invites-101) how to create one
* **Slack URL**: Permanent Slack invite link (will be used to let visitors join your Slack)
* **GitHub URL**: Link to your GitHub organization page or repo\


**Auto-publishing** For auto-publishing conversations to your community help center, you have three options:

* **None**: No conversation is going to be published automatically.
* **Specific channels**: Conversations from selected channels will automatically be published.
* **All channels**: All conversations will automatically be published.

Once you choose an option and save it, it will affect all past conversations in that channel!\


**Theming**

* **Logo URL**: The logo that will be displayed in the upper right corner. (Recommended size: 240x60 pixels)
* **Favicon URL**: The icon that will be displayed in the browser tab. (Recommended size: 32x32 pixels)
* **Colors**: The different colors of your community help center. We recommend playing around with it to see how it affects the appearance.

\
That's it. Click \*save\* and your community help center will automatically be created/changed.\


### Custom domain set-up (Premium only)

To set up a custom domain to your help center, simply navigate [here](https://app.crowd.dev/conversations).

Click on the _Settings_ button and add your custom domain (ex: [help.crowd.dev](https://help.crowd.dev)) into the following input:

Next, add your a _CNAME_ record to your DNS pointing to [open.crowd.dev](https://open.crowd.dev) like the following example:

\[block:image] { "images": \[ { "image": \[ "https://files.readme.io/c01347c-custom-domain-dns.png", "custom-domain-dns.png", 1223, 451, "#fbfbfc" ] } ] } \[/block]

## Review and edit existing Conversations

You should see conversations in a list view: \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/a4ff66d-conversations-2.png", "conversations-2.png", 2712, 1318, "#f0f1f2" ] } ] } \[/block]\
You can click on each conversation and view it in detail: \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/c4b3146-conversations-3.png", "conversations-3.png", 2726, 966, "#f5f5f5" ] } ] } \[/block]\
You can also edit the title of the conversation by clicking on the ✏️ icon. Please note: A changed title will affect your titleSlug before you publish a conversation for the first time: _open.crowd.dev/{tenantSlug}/{titleSlug}_

\


## Filter & Sort Conversations

Active communities often have 100s and 1000s of conversations. To stay on top of it, the conversations module has a variety of filter and sorting options:

* **Title**: Filter or sort by keywords in the conversation title (usually the first message of conversation)
* **Status**: Filter by the publishing status of the conversation (published/unpublished)
* **Number of Activities**: Sort by the number of activities/replies a conversation received
* **Last active**: Sort by the timestamp of the latest activity/reply that got added to the conversation
* **Platform**: Filter by platform (Discord, Slack, Github, etc.)
* **Channel**: Filter by channel (e.g. #support on your Discord)

To sort conversations, simply click on the table header to sort the referring column either ascending or descending.

To filter conversation, either use the quick filters on top (for _Status_ and _Platforms_) or click on _Filters_, select your desired options, and confirm with _Apply Filters_. \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/0e267ce-Bildschirmfoto\_2022-06-30\_um\_10.44.39.png", "Bildschirmfoto 2022-06-30 um 10.44.39.png", 2728, 1324, "#9c9b9b" ] } ] } \[/block]

\[block:image] { "images": \[ { "image": \[ "https://files.readme.io/64d3661-Bildschirmfoto\_2022-06-30\_um\_10.45.48.png", "Bildschirmfoto 2022-06-30 um 10.45.48.png", 2710, 936, "#f8f8f9" ] } ] } \[/block]\


## Auto-publish Conversations

To auto-publish conversations to your community help center, simply go to the settings and choose an auto-publishing option. You can choose between:

* **None**: No conversation is going to be published automatically.
* **Specific channels**: Conversations from selected channels will automatically be published.
* **All channels**: All conversations will automatically be published.

Once you picked an option and saved it, it will affect all past conversations in that channel!

## Publish selected Conversations

To publish selected conversations to your community help center, you have two options:

\


**Option 1: Bulk publish conversations in the conversations list view**

This option also works well with filters and helps you to publish several conversations at once. (Tip: To maximize the number of selected conversations, you can set the pagination to 100/page at the bottom of the table.) \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/259957c-conversations-5.png", "conversations-5.png", 2710, 1324, "#eef0f3" ] } ] } \[/block]\


**Option 2: Publish a conversation in the conversations list view** \[block:image] { "images": \[ { "image": \[ "https://files.readme.io/cea224e-conversations-4.png", "conversations-4.png", 2726, 966, "#f5f4f5" ] } ] } \[/block] After publishing, your conversation will be shown on **open.crowd.dev/{tenantSlug}**.

You can simply use _Unpublish Conversations_ to remove them from the public page again.\


## What’s next

Please note that this feature is currently in alpha. For the next releases we plan to:

* Add more filters and pre-selection support to identify Conversations worth publishing

What else are you missing? Feel free to [add it to our public roadmap](http://crowd.dev/roadmap).

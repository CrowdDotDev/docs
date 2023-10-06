---
description: Sync topics, posts, and replies from your Discourse forum
---

# Discourse integration

## Data tracked

Historical import

* We create activities for all topics and posts and also create members for all users who performed these activities.

Incremental import

* We create activities for all new topics, posts, users who joined your forum, and likes on posts. Members are created for all users who perform these activities.

## How to install

### API Key

To create API in your Discourse instance, you should be an admin.

1. First, click on the setting and go to the Admin panel.

<figure><img src="https://files.readme.io/c579bb9-image.png" alt=""><figcaption></figcaption></figure>

2.  Go to the API tab and click on `New API Key.`\


    <figure><img src="https://files.readme.io/48fc4b8-image.png" alt=""><figcaption></figcaption></figure>
3.  Give your API key some description, set the user level of `Single User`, select `system` user (it is available in all Discourse instances) and tick Global Key.\


    <figure><img src="https://files.readme.io/fdc4d37-image.png" alt=""><figcaption></figcaption></figure>
4. Copy your API key and paste it into crowd.dev.

![](https://files.readme.io/b368b53-image.png)

### Webhooks

Once you configure API connection in crowd.dev, you will see a section with `Payload URL` and `Webhook Secret` to configure webhooks in Discourse.

1. Go to an admin panel in your Discourse instance

<figure><img src="https://files.readme.io/c579bb9-image.png" alt=""><figcaption></figcaption></figure>

2. Go to API tab, and then to Webhooks tab inside it. Click on `New Webhook` button.

<figure><img src="https://files.readme.io/9eec6ee-image.png" alt=""><figcaption></figcaption></figure>

3. Paste your `Payload URL` and `Secret` which you copied from crowd.dev app

<figure><img src="https://files.readme.io/5bdc6dd-image.png" alt=""><figcaption></figcaption></figure>

4. Scroll down and check `Send me everything` option (ignore all other options)\


<figure><img src="https://files.readme.io/f567f9d-image.png" alt=""><figcaption></figcaption></figure>

5. Scroll down a bit more and check both options

<figure><img src="https://files.readme.io/92ed01b-image.png" alt=""><figcaption></figcaption></figure>

6.  After you configured everything, go back to crowd.dev app and click `Connect`. Now, you will receive webhooks.\


    <figure><img src="https://files.readme.io/3a5a23c-image.png" alt="" width="375"><figcaption></figcaption></figure>
7.  If you want to verify webhooks are configured properly, you can click on settings (see picture below) and then click on `Verify webhook`. Before clicking this button, make sure to do some action in Discourse - e.g. logging in / out, liking a post, or using a `Ping` button in webhooks section.\


    <figure><img src="https://files.readme.io/84357ca-image.png" alt="" width="375"><figcaption></figcaption></figure>

![](https://files.readme.io/cc4594b-image.png)

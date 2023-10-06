# Webhooks

Webhooks allow you to automate workflows, for example whenever a new member joins or a new activity happens in your community. Simply pick a trigger, set a filter (e.g., to only trigger when the activity happens on Discord), and set it live. You now have a webhook that you can use to, for example, build workflows in Zapier or Make. We'll expand this feature in the upcoming months and turn it into a proper workflow builder within the crowd.dev app.

![](https://files.readme.io/676861c-Screenshot\_2022-10-27\_at\_15.22.25.png)

## To set up a Webhook

* Navigate to **Settings** (at the bottom of the lefthand navbar)
* Click the **Automations** view
* Click the **add automation** button
* Select **Webhook** from the dropdown
* Next you can choose a trigger - an event that will "fire" the webhook. E.g, when a user stars your repo, crowd.dev will immediately send you information about this user. There are basically two types of triggers - new activity trigger and new member trigger. The first one fires when some event happens (which you specify), and the second one fires when a new member joins the community. The new activity trigger webhook returns info about an event, new member webhook returns info about a new member. From the drop-down just click whichever you would like to happen.

#### To specify a new member webhook

* Choose **New member joined your community**
* From the dropdown choose one or more platforms you would like to trigger this webhook for
* Specify a url where data will be submitted (posted) when the event happens. This can be a url on your server, on in a service like Zapier or Make.com.
* Lastly, click **Add webhook**

![](https://files.readme.io/13946df-Screenshot\_2022-10-27\_at\_15.32.53.png)

#### To specify a new activity webhook

* Choose **New activity happened in your community**
* From the dropdown on the left choose one or more platforms you would like to trigger this webhook for
* From the dropdown on the right select the activity types you want to trigger the webhook
* You also have the option to specify specific keywords that will trigger a webhook, for example, you can choose to be notified whenever someone in Discord writes a message including the keyword "community"
* Specify a url where data will be submitted (posted) when the event happens. This can be a url on your server, on in a service like Zapier or Make.com.
* Lastly, click **Add webhook**

![](https://files.readme.io/3835a93-Screenshot\_2022-10-27\_at\_15.26.50.png)
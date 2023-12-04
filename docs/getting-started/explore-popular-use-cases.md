---
description: How go-to-market teams commonly use crowd.dev to grow
---

# 🗺 Explore popular use cases

crowd.dev helps you unify your developer data, surface insights in that data, and enable your go-to-market team to act on those insights.&#x20;

To get started with crowd.dev, try a few of our most popular use cases:

* [Find high-intent accounts in your developer data](explore-popular-use-cases.md#find-high-intent-accounts-in-your-developer-data)
* [Sync data with Hubspot](explore-popular-use-cases.md#sync-data-with-hubspot)
* [Send notifications to Slack](explore-popular-use-cases.md#send-notifications-to-slack)
* [Send notifications with Webhooks](explore-popular-use-cases.md#send-notifications-with-webhooks)
* [Identify key contacts in your developer data](explore-popular-use-cases.md#identify-key-contacts-in-your-developer-data)
* [Find and nurture influential contacts](explore-popular-use-cases.md#find-and-nurture-influential-contacts)
* [Re-engage slipping away contacts](explore-popular-use-cases.md#re-engage-slipping-away-members)
* [Identify sales opportunities](explore-popular-use-cases.md#identify-sales-opportunities)
* [Conduct product research](explore-popular-use-cases.md#conduct-product-research)
* [Find relevant content to engage with](explore-popular-use-cases.md#find-relevant-content-to-engage-with)
* [View live metrics and track growth](explore-popular-use-cases.md#view-live-metrics-and-track-growth)

***

### Find high-intent accounts in your developer data

Finding high-intent accounts in your developer data is the most commonly used use case. There is a variety of ways to go about this. One way is to combine filters on the "Organization" page&#x20;

Navigate to “Organizations” in the left-hand menu. This page gives us a full view of all the organizations in our ecosystem. To find high-intent accounts, “Filter” by “# of contacts” is “equal or greater than” and input 5. Then select "Filter" again and select “# of activities” is “equal or greater than” and enter 50. Now you can see all of the organizations that have a lot of employees engaged in your community. Lastly, you can filter to only include recent activities. To do this, click “+ Add filter” and select “Last activity date”, then click the drop-down arrow and select “is after”. Enter the date you want to see activity from and click “Apply”. You can leave the sorting as is and click “Add view”.

This combination of filters will show organizations with more than 5 contacts that have collectively taken over 50 activities. Giving us insight into the larger active organizations in our ecosystem.

### Sync data with Hubspot

With our Hubspot integration, you can sync crowd.dev data with Hubspot and vice versa. This gives your go-to-market team a full view of your user journey and lets them receive relevant purchase intent signals easily.

To connect Hubspot with crowd.dev, navigate to the "Integrations" page, click "Connect" and follow the steps. For more detailed information, you can view the Hubspot integration doc [here](https://docs.crowd.dev/docs/getting-started/integrations/hubspot-integration).

### Send notifications to Slack

Slack notifications allow you to receive notifications in a selected Slack channel. For example, you can configure it to receive a message whenever a new contact is detected. Pick a trigger, set a filter, and push it live.

To connect Slack with crowd.dev, navigate to the "Automations" page, click "Add automation" and follow the steps. For more detailed information, you can view the Slack integration doc [here](https://docs.crowd.dev/docs/guides/automations/slack-notifications).

### Send notifications with Webhooks

To get notified about key activities in your community, navigate to the [Automations tab](https://app.crowd.dev/settings?activeTab=automations) in the settings. Here, you can create webhooks for every activity that happens in your community. Follow the following steps:

1. Click “Add webhook”.
2. Choose the trigger “New activity happened in your community”
3. Refine the activities that trigger the webhook by applying filters for platform, activity type, or keywords.
4. Define a Webhook URL where the webhook should be sent, e.g., from an automation tool like [Make](https://make.com/).
5. Go to Make and create a workflow with a webhook as a trigger point. You can now use the webhook payload to send a notification to Slack or an email to your team.

If you need help with setting up webhooks, send an email to [help@crowd.dev](mailto:help@crowd.dev).

### Identify key contacts in your developer data

Navigate to the contacts page by selecting “Contacts” on the left sidebar. This page gives us a full view of all the contacts in your ecosystem. On this page, you can toggle the top menu to see different segments of contacts, like “new and active” or “most engaged”. Stay on the “All contacts” section and combine filters to get a clear picture of active senior developers in your ecosystem.

To do this, click “Filters” in the top right corner.  Select “Seniority Level”, then click on the filter and enter the keyword “senior”. Now you have a view of all senior developers, but we want to see which ones have actively engaged by forking your GitHub repo. To do this click on “Filters” in the top right corner again, select “Activity type”, and click on “Forked”. Now you have a full view of all the senior developers in your ecosystem who have also forked your Github repo.&#x20;

We can find the most engaged contacts relative to other contacts by sorting by “Engagement Level”. If you click on this contact you can view their profile. Our enrichment populates the profile with up to 20 developer attributes. If they are a good fit, you can tag them as a key contact and use this data and history to do personalized outreach.&#x20;

<figure><img src="../.gitbook/assets/docs-contact-profile.png" alt=""><figcaption></figcaption></figure>

### Find and nurture influential contacts

Navigate to the Contacts page and click on the[ Influential view](https://app.crowd.dev/contacts?search=\&relation=and\&order.prop=lastActive\&order.order=descending\&settings.bot=exclude\&settings.teamMember=exclude\&settings.organization=exclude\&reach.operator=gte\&reach.value=500). This will show you all contacts that have more than 500 followers (called “Reach”) on their social profiles combined across the platforms you connected (e.g., GitHub). By default, they are sorted by Reach, but you could also go on and apply filters to e.g., only see influential contacts that joined in the last 30 days or only those that have a high engagement level.&#x20;

Once you have identified contacts with high reach, you can try engaging them with a message. To do so, click on one of their identities (e.g., Twitter or Email) and draft a private message. We recommend keeping it short and sweet to increase the likelihood of a response.

Here is an example:

_Hey (name of contact),_

_I am (your name), the (your role) of (community name). We’ve noticed you are one of our most involved community members, so we wanted to thank you for contributing to our community. We really appreciate it! Is there anything I can do to help you?_

### Re-engage slipping away contacts

To re-engage contacts that are slipping away and engaging less with your product, navigate to the Contacts page and click on the[ Slipping away view.](https://app.crowd.dev/contacts?search=\&relation=and\&order.prop=lastActive\&order.order=descending\&settings.bot=exclude\&settings.teamMember=exclude\&settings.organization=exclude\&engagementLevel.value=fan,ultra\&engagementLevel.include=true\&lastActivityDate.operator=lt\&lastActivityDate.value=2023-09-07) This will show you all the contacts with a high engagement level (between 7-10) but have not completed any activities in your community in the last 14 days. We recommend re-engaging those contacts, for example, by sending them an email or a Discord message.

### Conduct product research

crowd.dev is a great tool for product discovery, you can learn what people have to say, for example, about certain problems or features you are providing. crowd.dev collects all of your contacts’ feedback, making them easily searchable for you. To conduct product research, navigate to the [Activities module](https://app.crowd.dev/activities) and type in a keyword. You can then refine the search results by applying different filters (e.g., sentiment or platform). Here is an example that shows activities for our “twitter integration” with a negative or neutral sentiment:&#x20;

<figure><img src="../.gitbook/assets/docs-activities-research.png" alt=""><figcaption></figcaption></figure>

### Find relevant content to engage with

Our Eagle Eye app allows you to monitor different developer platforms to find relevant content to engage with, ultimately helping you to gain developers’ mindshare and grow your community.

Navigate to the [Eagle Eye app](https://app.crowd.dev/eagle-eye), type in a few keywords that are relevant to your niche, open the post by clicking on it, and leave a thoughtful comment. After that, you can mark the post as “engaged” to keep track of the posts that you engaged with through Eagle Eye.&#x20;

### Manage your task’s

To create tasks, you can leverage the [Tasks module](https://app.crowd.dev/task). Here you can create and manage tasks, relate them to contacts, and assign them to you or your teammates. Typical tasks we use are, for example, “reach out to this contact about our enterprise solution” or “follow up with this contact regarding their support request on Discord”.

You can also create tasks in a contact's profile view. You only need to switch to the “Tasks” tab and click “Add task”. This will open the same window for task creation.

Learn more about Tasks [here](https://docs.crowd.dev/docs/tasks).

### View live metrics and track growth

Our [reporting module](https://app.crowd.dev/reports) helps you easily tie different metrics together and share them with your team.

By default, you can find an example report in your workspace. Duplicate and modify it to tailor the report to your specific needs. If you want to share a report, publish it and copy and paste the public URL.

Learn more about Reports [here](../guides/reports/).

{% hint style="success" %}
Thanks for reading through this. We’d love to hear about your personal use cases for crowd.dev. Please feel free to reach out to use via [hello@crowd.dev](mailto:hello@crowd.dev) or drop a message in our [Discord community](http://crowd.dev/discord).
{% endhint %}


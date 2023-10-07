# Activity sentiment

We conduct a sentiment analysis for all activities with text. As a result, we calculate a sentiment score that goes from 0 to 100, with 0 being very negative and 100 being very positive.

To make the sentiment score more usable, we sort all activities into three ranges (that are also used on Home or to filter activities):

* 0-33: Negative sentiment
* 34-67: Neutral sentiment
* 68-100: Positive sentiment

For each activity, you can also see the sentiment score, which will show you the extent to which the activity is positive or negative.&#x20;

<figure><img src="https://files.readme.io/0664e55-Screenshot_2022-10-24_at_09.49.29.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**What is sentiment analysis?**

Sentiment analysis is an approach to natural language processing (NLP) that identifies the emotional tone behind a text. It is a popular way to determine and categorize opinions about products, services, or ideas.
{% endhint %}

### How is sentiment calculated?

To analyze activity sentiment, we use [AWS Comprehend](https://aws.amazon.com/comprehend/). For each activity, Comprehend returns four values:

* positive: the probability that the activity's sentiment is positive,
* negative: the probability that the activity's sentiment is negative,
* neutral: the probability that the activity has a neutral tone,
* mixed: the probability that the activity has positive and negative emotions.

The values always add up to 1.

For now, crowd.dev is only considering the positive, negative, and neutral values. Therefore, we use the positive and negative scores to compute a sentiment score from 0 to 100. Small values represent activities with negative sentiment, values close to fifty with neutral sentiment, and high values with positive sentiment.

The sentiment score is calculated by mapping the difference between positive and negative probabilities onto a scale of 0 to 100:

![equation](https://latex.codecogs.com/svg.image?50\&space;%5Ccdot\(%5Cmathrm%7Bpositive%7D\&space;-\&space;%5Cmathrm%7Bnegative%7D\)\&space;+\&space;50)

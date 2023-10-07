# Merge contacts

One community contact will often be active within your community on several platforms and user profiles. crowd.dev enables you to merge contacts so that you don't have duplicates and see all the data of one of your contacts in one place. There are two ways to merge contacts.

## Merge contacts based on suggestions

Our algorithm will detect whether two similar profiles belong to the same contact and will suggest you merge them. You will receive a notification on the top right corner of your contacts page when we have merge suggestions.

1. Click on **Merge suggestions** in the top-right notification
2. You will be taken to a **Merge suggestions** page where all suggestions will be displayed to merge two or more profiles into one
3. For each, you can click **Merge contacts** to merge or **Ignore suggestion** if you see there has been a mistake
4. In either view, you can choose which of the multiple profiles should be your **Primary contact** by clicking **Make primary**. This means if details conflict with each other, e.g., different profile images or a different contact since value, the values of the primary profile will be the default view in the contact profile.

### The algorithm to perform merge suggestions

Contact are analyzed based on usernames and emails to determine if they might be the same individual. The algorithm performs three types of checks:

* **Same Username Check**: Identifies contacts with the same username across different platforms. The algorithm considers these two contacts as likely to be the same individual. The confidence score for this scenario is 95%, which indicates a strong certainty but is not absolute.
* **Overlapping Email Check**: Finds contacts where at least one email is the same. Since email addresses are generally unique, the confidence score for this match type is set to 100, indicating a high likelihood that they are the same individual.
* **Similar Usernames Check**: Uses the Levenshtein Distance to measure the similarity between usernames from different platforms. The algorithm calculates a similarity score ranging between 0 and 1, where 0 means completely different and 1 means identical. They are considered potential matches if the similarity score is greater than 0.5. However, the confidence score will not exceed 0.95, as the email similarity check is considered more reliable.

The algorithm identifies new contacts hourly and performs the three checks. This provides a comprehensive list of potential merges, with varying confidence scores based on the level of similarity.

## Merge contacts manually

If the crowd.dev algorithm is not completely sure that two or more user profiles are the same contact, we will not automatically suggest you merge them. However, if you know that two or more profiles are actually the same, you can easily merge them manually.

1. Choose one of the contact profiles you would like to merge and click on the three dots in a contact card (either on the contacts' page or on the respective contact profile page)
2. Click the three dots icon, and in the dropdown, click the option **Merge contact**
3. In the pop-up, you will see the details of the contact you selected, and on the right side, you can search for the other contact profile you think belongs to this one
4. Select the member and click **Merge contacts**

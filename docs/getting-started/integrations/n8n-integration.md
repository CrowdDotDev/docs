---
description: Connect n8n with crowd.dev to access 5,000+ apps
---

# n8n integration

## How to install

To start using the integration, go to the [Integration settings](https://app.crowd.dev/integrations) and follow the steps to set up n8n.

## Supported operations

An operation is something an n8n node does, such as getting or sending data. There are two types of operation:

**Triggers** start a workflow in response to specific events or conditions in your services. When you select a Trigger, n8n adds a trigger node to your workflow, with the Trigger operation you chose pre-selected. When you search for a node in n8n, Trigger operations have a bolt icon Trigger icon.

**Actions** are operations that represent specific tasks or actions within a workflow, allowing you to manipulate data, perform operations on external systems, and trigger events in other systems as part of your workflows. When you select an Action, n8n adds a node to your workflow, with the Action operation you chose pre-selected.

### Triggers

The crowd.dev trigger node allows you to respond to events in crowd.dev and integrate crowd.dev with other applications. n8n has built-in support for a wide range of crowd.dev events, which include new activities and new members.

* **New Activity:** This trigger is activated when a new activity happens in your community platforms connected to crowd.dev. For example, someone starred your repo, sent a message in Discord, etc. You can make this trigger granular. For example, only activate it when someone opens a pull request on GitHub and mentions a specific keyword. On the other side of the spectrum, you can configure this trigger to be a "catch-all", but this setup is not recommended because it will be quite hard to distinguish between different events on n8n side. So, the recommended configuration is to keep this trigger as narrow as possible.
* **New Member**: This trigger is activated when a new member joins your community platforms connected to crowd.dev. In crowd.dev, a member is considered anyone who performed at least one action at your community platforms - e.g., joined a Discord server or did something on GitHub (the trigger is activated only once for each user). This trigger can be configured as a "catch-all" (all new member activities for all active platforms) or only for specific platforms.

### Actions

The crowd.dev node allows you to automate work in crowd.dev and integrate crowd.dev with other applications. n8n has built-in support for a wide range of crowd.dev features include creating, updating, and deleting members, notes, organizations, and tasks.

**Activity**

* **Create or update activity for a member** - _takes a member object and information about the activity and creates or updates an activity for this member in crowd.dev_
* **Create or update activity** - _takes an activity object and creates or updates an activity in crowd.dev based on sourceId of activity and platform_

**Member**

* **Create or update member** - _takes a member object and creates or updates a member in crowd.dev_
* **Update member** - _takes a member object and updates an existing member in crowd.dev based on memberId. Fails if the member doesn't exist._
* **Find task** - _returns a member object for an existing member based on memberId. Fails if the member doesn't exist._
* **Delete member** - _deletes an existing member based on memberId. Fails if the member doesn't exist._

**Organization**

* **Create organization** - _creates a new organization in crowd.dev_
* **Update organization** - _updates an existing organization in crowd.dev by `organizationId`. Fails if the organization doesn't exist._
* **Find organization** - _returns an organization object for an existing organization based on `organizationId`. Fails if the organization doesn't exist._
* **Delete organization** - _deletes an existing organization based on `organizationId`. Fails if the organization doesn't exist._

**Note**

* **Create note** - _create a new note in crowd.dev_
* **Update note** - _updates an existing note in crowd.dev by `noteId`. Fails if the note doesn't exist._
* **Find note** - _returns a note object for an existing note based on `noteId`. Fails if the note doesn't exist._
* **Delete note** - _deletes an existing note based on `noteId`. Fails if the note doesn't exist._

**Task**

* **Create task** - _creates a new task in crowd.dev_
* **Update task** - _updates an existing task in crowd.dev by `taskId`. Fails if the task doesn't exist._
* **Find task** - _returns a task object for an existing task based on `taskId`. Fails if the task doesn't exist._
* **Delete task** - _deletes an existing task based on `taskId`. Fails if the task doesn't exist._

**Automation**

* **Create automation** - _creates a new automation workflow in crowd.dev_
* **Destroy** - _destorys an automation workflow in crowd.dev_
* **Find** - _returns an automation object for an existing automation based on `automationId`. Fails if the automation doesn't exist._
* **List** - _lists all automation objects in crowd.dev_
* **Update** - _updates an existing automation in crowd.dev by `automationID`. Fails if the automation doesn't exist._

## Further links

* [n8n's crowd.dev integration overview](https://n8n.io/integrations/crowddev)
* [n8n's crowd.dev action docs](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.crowddev/)
* [n8n's crowd.dev trigger docs](https://docs.n8n.io/integrations/builtin/trigger-nodes/n8n-nodes-base.crowddevtrigger/)

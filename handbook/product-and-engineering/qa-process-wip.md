---
description: >-
  This section will describe the QA process we follow at crowd.dev and when to
  involve external help
---

# 🔎 QA process (WIP)

We believe it is essential to keep a lean development process and empower every engineer to do their own quality assurance. However, we understand that some situations could benefit from external help for doing QA.&#x20;

### Doing your own QA

Engineers should do their own QA for all bug fixes and minor features. The owner of the area of ownership for that specific feature is responsible for features having been battle-tested enough to be open to all users.

### Involving external help

#### When to ask for help

There are three cases where it is always okay to ask for external help:

* **We are delivering a milestone for an enterprise customer**: when working with enterprise customers, the development paradigm changes: we have a set of milestones that we need to achieve, and the requirements are precise and previously agreed upon. Therefore, it makes sense to get external QA help to ensure our clients get what we promised.
* **Developing a new integration**: integrations are sometimes tricky to test, and it's almost impossible to write automated tests. It's also a crucial part of crowd.dev, and we must ensure they are solid. We can get external help for this.
* **A change can potentially affect multiple other parts**: sometimes, we might have to change our core data structure, add new entities, or change how existing entities relate to each other. These cases can affect the functionality of the whole app, and doing the regressions can be time-consuming.

There might be other cases where we might need external QA. The area owner can send a message to Joan, giving short but proper arguments as to why it is needed.

#### How to ask for help

To ask for help, create a new issue in Linear with the _QA_ label, and assign it to our freelancer QA engineer. You should clarify in the issue description what the feature is, what it should be doing, and what should be tested. Feel free to point to any existing documentation.

#### The QA process when external help is involved

# ℹ Telemetry

We collect anonymized data from self-hosted versions in order to improve our product. This can be deactivated at any time, and any data that has already been collected can be deleted on request.

#### What data do we collect?

{% hint style="danger" %}
**Data privacy**

We collect as few data points as we can. Using our self-hosted version, we will never receive any personal information from you or your community members.
{% endhint %}

On self-hosted versions, we collect:

| Event                | Description                    | properties                                                      |   |
| -------------------- | ------------------------------ | --------------------------------------------------------------- | - |
| Tenant created       | Creation of a new tenant       | `id`, `createdAt`                                               |   |
| User created         | Creation of a new user         | `id`, `createdAt`                                               |   |
| Member created       | Creation of a new member       | `id`, `createdAt`                                               |   |
| Activity created     | Creation of a new activity     | `id`, `createdAt`, `timestamp`, `platform`, `communityMemberId` |   |
| Conversation created | Creation of a new conversation | `id`, `createdAt`, `platform`                                   |   |

#### Why collect telemetry data?

We collect telemetry data to

* Improve our product: reliable usage data helps us to evaluate features and fix bugs.
* Prove that people are actually using [crowd.dev](https://crowd.dev/): Sage metrics help us justify our existence to investors and potential new customers to keep this project alive.

#### Deactivating telemetry

To deactivate telemetry, simply set `SEGMENT_WRITE_KEY=""` in the environment files.

\

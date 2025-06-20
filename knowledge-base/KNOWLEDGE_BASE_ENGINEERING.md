# Knowledge Base - Engineering & AI/ML 👩🏽‍💻📱

Knowledge base for https://github.com/orgs/elimu-ai/projects/3?pane=info

## Software Engineering Principles 📝

### Maintainability

As an open-source organization, it is extra important that we design our software in such a way that new engineers are able to understand and maintain the code. Therefore, when building our software product, we follow these three design principles:

> [!NOTE]
> 1. **Operability**
> 
>    Make it easy for operations teams to keep the system running smoothly.
>
> 2. **Simplicity**
>
>    Make it easy for new engineers to understand the system, by removing as much complexity as possible from the system.
>
> 3. **Evolvability**
>
>    Make it easy for engineers to make changes to the system in the future, adapting it for unanticipated use cases as requirements change.

## Android Development 📱

### How to test `-SNAPSHOT` versions of internal libraries

See documentation per repo:
* `ai.elimu:model` (`// TODO`)
* [`ai.elimu.analytics:utils`](https://github.com/elimu-ai/analytics/blob/main/README.md#how-to-test--snapshot-versions-of-the-utils-library)
* [`ai.elimu.appstore:utils`](https://github.com/elimu-ai/appstore/blob/main/README.md#how-to-test--snapshot-versions-of-the-utils-library)
* [`ai.elimu.content-provider:utils`](https://github.com/elimu-ai/content-provider/blob/main/README.md#how-to-test--snapshot-versions-of-the-utils-library)
* [`ai.elimu.common-utils:utils`](https://github.com/elimu-ai/common-utils/blob/main/README.md#how-to-publish-a-snapshot-for-local-development--testing)

### How to collaborate on Git branches where `force-push` was used

If you are peer-reviewing a pull request which gets force-pushed after your initial review, use the following commands to synchronize your local branch:

```
git reset --hard
git fetch
git pull --rebase origin <branch name>
```

### Library dependencies

Some Android apps depend on other elimu.ai Android apps to be installed. See 
[flowchart](https://github.com/elimu-ai/wiki/blob/main/SOFTWARE_ARCHITECTURE.md#library-dependencies).

### Data Collection

To get an understanding of how data is collected from the Android apps, see https://github.com/elimu-ai/ml-datasets/blob/main/README.md#data-sources

## Game Development 🕹️

Most of our games use Cocos2d-x as their game engine:

| Game | Game Engine |
| -------- | -------- |
| [VoltAir](https://github.com/elimu-ai/VoltAir) | Qt |
| [Nya's Space Quest](https://github.com/elimu-ai/nyas-space-quest) | Cocos2d-x |
| [Nya's Space Quest: Quantity Discrimination](https://github.com/elimu-ai/nyas-space-quest-qd) | Cocos2d-x |
| [Seaworld](https://github.com/elimu-ai/seaworld) | Cocos2d-x |
| [Walezi](https://github.com/elimu-ai/walezi-android) | Pandam |
| Kitkit School (mainapp) | Cocos2d-x |
| [Sima](https://github.com/elimu-ai/sima) | Cocos2d-x |

## Web development 💻

### Applications

Android applications are managed using the Webapp's UI at `http://<language>.elimu.ai/application/list`, and downloaded through the Webapp's REST API endpoint at `http://<language>.elimu.ai/rest/v2/applications`.

### Content

Educational content is added using the Webapp's UI at `http://<language>.elimu.ai/content`, and downloaded through the Webapp's REST API endpoints at `http://<language>.elimu.ai/rest/v2/content/*`.

### Analytics

Data collected from our educational Android apps is uploaded through the Webapp's REST API endpoints at `http://<language>.elimu.ai/rest/v2/analytics/*`, and made available at `http://<language>.elimu.ai/analytics`.

## AI & Machine Learning 🤖

...

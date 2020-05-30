![xprize-no-text_banner](https://user-images.githubusercontent.com/15718174/82723985-51250780-9d05-11ea-8fc6-e800d9b414eb.png)
> A collection of educational Android apps teaches children basic literacy and numeracy in a fun and engaging way.

# elimu.ai Software Architecture


## Learning Platform

The [elimu.ai](http://elimu.ai) software is a _platform_ of educational content and Android apps.

Instead of having one large Android application containing everything, the [elimu.ai](http://elimu.ai) software has been architected such that there are many smaller applications, each with their own specific responsibility.

Broadly speaking, there are three categories of Android applications:
  1. Infrastructural applications
  1. Literacy apps/games
  1. Numeracy apps/games

![elimu ai Software Architecture](https://user-images.githubusercontent.com/15718174/82879896-30acb580-9f70-11ea-9489-b6a9a37e89bb.png)


## Software Dependencies 🔄

As depicted in the diagram above, several of the elimu.ai applications communicate with each other. As an example; When the app for reading storybooks ([Vitabu](https://github.com/elimu-ai/vitabu)) is opened, it asks the [content-provider](https://github.com/elimu-ai/content-provider) app to provide a list of storybooks. This means that the storybooks app depends on the content-provider app to be installed.


## Software Localization

See [LOCALIZATION.md](LOCALIZATION.md).


## Software Distribution 📦

When distributing the software, there are two main questions that need to be answered:
   1. Does the child already have access to an Android device?
   1. Does the device have access to an Internet connection?

Based on the answers to the above questions, the following are the required steps for distributing the software:

1. If a child already has access to an Android device _and_ access to an Internet connection, the household (e.g. parents) can download and install the software by:
   * Download the [elimu.ai Appstore](https://github.com/elimu-ai/appstore), which automatically downloads all the required infrastructural and literacy/numeracy apps/games.

1. If a child already has access to an Android device, but _no_ access to an Internet connection, the software can be installed by:
   * Download a ZIP file from the [elimu.ai](http://elimu.ai) website meant for _offline_ installation. This file contains all the Android apps, educational content, as well as an installation script (Unix/Windows).
   * Bring the file, a laptop, and a USB cable to the household.
   * Connect the USB cable to the Android device, and execute the installation script in order to automatically install all the Android APK files and content.

1. If a child does _not_ already have access to an Android device:
   * Obtain an Android device with 6" display or larger. Make sure the Android version installed on the device is [supported](https://github.com/elimu-ai/appstore#what-devices-are-being-used) by the elimu.ai software.
   * Download the [elimu.ai Appstore](https://github.com/elimu-ai/appstore), which automatically downloads all the required infrastructural and literacy/numeracy apps/games.
   * Bring the device to the household.


## Personalized Learning 🚀

For _personalized learning_ to be truly effective, each child should have their own Android device. The software is designed to automatically adapt the educational content and apps to the current knowledge level of the child, so if another child uses the same user account on the same Android device, the personalized learning will not work.

At the very least, a separate Android user should be created for each child if they have to share the same device. For more information on how Android user management works, see [Supporting Multiple Users | Android Open Source Project](https://source.android.com/devices/tech/admin/multi-user).

![Multi-User-Android-One](https://user-images.githubusercontent.com/15718174/83320709-9fde1e80-a27c-11ea-9201-83d0a1726914.jpg)


## Data Collection 📊

In order to measure how well the elimu.ai software is working, usage data is collected from the Android devices so that we can analyze the learning of each child. This enables us to carefully monitor how changes in code or content produce different learning outcome, as well as continuously improve the software.

The data is synced between the Android devices and the webapp's [REST API](https://github.com/elimu-ai/webapp/blob/master/README.md#rest-api) whenever an Internet connection is available.


---

## About the elimu.ai Community

![elimu ai-tagline](https://user-images.githubusercontent.com/15718174/54360503-e8e88980-465c-11e9-9792-32b513105cf3.png)

 * For a high-level description of the project, see https://github.com/elimu-ai/wiki/blob/master/README.md.
 * For project milestones, see https://github.com/elimu-ai/wiki/projects.

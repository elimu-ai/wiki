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

As depicted in the diagram above, several of the elimu.ai applications communicate with each other. As an example, when the app for reading storybooks ([Vitabu](https://github.com/elimu-ai/vitabu)) is opened, it asks the [content-provider](https://github.com/elimu-ai/content-provider) app to provide a list of storybooks. This means that the storybooks app depends on the content-provider app to be installed.



## Software Distribution 📦

When distributing the software, there are two main questions that need to be answered:
  1. Does the child already have access to an Android device?
  1. Does the device have access to an Internet connection?

Based on the answers to the above questions, the following are the required steps for distributing the software:
  1. If a child already has access to an Android device _and_ access to an Internet connection, the household (e.g. parents) can download and install the software by:
    1. ⬇️ Downloading the [elimu.ai Appstore](https://github.com/elimu-ai/appstore), which automatically downloads all the required infrastructural and literacy/numeracy apps/games.
  1. If a child already ...

## Personalized Learning 🚀

For _personalized learning_ to be truly effective, each child should have their own Android device. The software is designed to automatically adapt the educational content and apps to the current knowledge level of the child, so if another child uses the same user account on the same Android device, the personalized learning will not work.

At the very least, a separate Android user should be created for each child if they have to share the same device. For more information on how Android user management works, see [Supporting Multiple Users | Android Open Source Project](https://source.android.com/devices/tech/admin/multi-user).

![Multi-User-Android-One](https://user-images.githubusercontent.com/15718174/83320709-9fde1e80-a27c-11ea-9201-83d0a1726914.jpg)

## Data Collection 📊

...

---

## About the elimu.ai Community

![elimu ai-tagline](https://user-images.githubusercontent.com/15718174/54360503-e8e88980-465c-11e9-9792-32b513105cf3.png)

 * For a high-level description of the project, see https://github.com/elimu-ai/wiki/blob/master/README.md.
 * For project milestones, see https://github.com/elimu-ai/wiki/projects.

![xprize-no-text_banner](https://user-images.githubusercontent.com/15718174/82723985-51250780-9d05-11ea-8fc6-e800d9b414eb.png)
> A collection of educational Android apps teaches children basic literacy and numeracy in a fun and engaging way.

# elimu.ai Software Architecture 🏛

###### Table of contents
  1. [Learning Platform](#learning-platform)
  1. [Software Dependencies](#dependencies)
  1. [Software Scalability](#scalability)
  1. [Data Collection](#data-collection)
  1. [Artificial Intelligence (AI)](#ai)


<a name="learning-platform"></a>
## Learning Platform

The [elimu.ai](http://elimu.ai) software is a _platform_ of educational content and Android apps.

Instead of having one large Android application containing everything, the [elimu.ai](http://elimu.ai) software has been architected such that there are many smaller applications, each with their own specific responsibility.

Broadly speaking, there are three categories of Android applications:
  1. Infrastructural applications
  1. Literacy apps/games
  1. Numeracy apps/games

![elimu ai Software Architecture](https://user-images.githubusercontent.com/15718174/83595568-fb6a1e00-a594-11ea-990a-10c0bd62ed11.png)


<a name="dependencies"></a>
## Software Dependencies 🔄

As depicted in the diagram above, several of the elimu.ai applications communicate with each other. As an example; When the app for reading storybooks ([Vitabu](https://github.com/elimu-ai/vitabu)) is opened, it asks the [content-provider](https://github.com/elimu-ai/content-provider) app to provide a list of storybooks. This means that the storybooks app depends on the content-provider app to be installed.


<a name="scalability"></a>
## Software Scalability

The software platform is being built to handle scaling to many different languages. A collection of many smaller apps, all [categorized](https://github.com/elimu-ai/launcher/blob/master/README.md#pedagogy) by literacy/numeracy skills makes it possible to easily adjust the complete curriculum when localizing from one language to another.

The file size of the apps, games and multimedia is kept as small as possible in order to make the distribution easier in locations with limited Internet connectivity. In addition, the software has been designed to work offline so that it can be used in rural areas.

<a name="localization"></a>
### Localization

For instructions on how to add support for a new language, see [LOCALIZATION.md](LOCALIZATION.md).


<a name="crowdsourcing"></a>
### Content Crowdsourcing

Another way to ensure software scalability is through _crowdsourcing_. By using the [elimu.ai Crowdsource](https://github.com/elimu-ai/crowdsource) Android app or the [elimu.ai Webapp](https://github.com/elimu-ai/webapp), the crowd is able to upload and peer review educational content on the platform, and thus help speed up the expansion to more languages. As an example, such a task might involve transcribing a few audio recordings, peer reviewing existing audio transcriptions, translating a storybook, recording audio files for an entire storybook, labelling videos by content, etc.


<a name="distribution"></a>
### Distribution 📦

When distributing the software, there are two main questions that need to be answered:
   1. Does the child already have access to an Android device?
   1. Does the device have access to an Internet connection?

Based on the answers to the above questions, the following are the necessary steps for distributing the software:

1. If a child already has access to an Android device _and_ access to an Internet connection, the household (e.g. parents) can download and install the software by:
   * Download the [elimu.ai Appstore](https://github.com/elimu-ai/appstore).
   * Install and launch the Appstore. Then select the child's [mother tongue](PEDAGOGY.md) as the language of instruction.
   * Wait for the Appstore to automatically download all the required infrastructural and literacy/numeracy apps/games. (See [SOFTWARE_INSTALLATION.md](SOFTWARE_INSTALLATION.md))

1. If a child already has access to an Android device, but _no_ access to an Internet connection, the software can be installed by:
   * Download a ZIP file from the [elimu.ai](http://elimu.ai) website meant for _offline_ installation. This file contains all the Android apps, educational content, as well as an installation script (Unix/Windows).
   * Bring the file, a laptop, and a USB cable to the household.
   * Connect the USB cable to the Android device, and execute the installation script in order to automatically install all the Android APK files and content.

1. If a child does _not_ already have access to an Android device:
   * Obtain an Android device with 6" display or larger. Make sure the Android version installed on the device is [supported](https://github.com/elimu-ai/appstore#what-devices-are-being-used) by the elimu.ai software.
   * Download the [elimu.ai Appstore](https://github.com/elimu-ai/appstore).
   * Install and launch the Appstore. Then select the child's [mother tongue](PEDAGOGY.md) as the language of instruction.
   * Wait for the Appstore to automatically download all the required infrastructural and literacy/numeracy apps/games. (See [SOFTWARE_INSTALLATION.md](SOFTWARE_INSTALLATION.md))
   * Bring the device to the household.


<a name="data-collection"></a>
## Data Collection 📊

In order to measure how well the elimu.ai software is working, usage data is collected from the Android devices so that we can analyze the learning of each child. This enables us to carefully monitor how changes in code or content produce different learning outcome, as well as continuously improve the software.

The data is synced between the Android devices and the webapp's [REST API](https://github.com/elimu-ai/webapp/tree/master/src/main/java/ai/elimu/rest) whenever an Internet connection is available.

For assessing the learning outcome of the children, we are collecting data [categorized](https://github.com/elimu-ai/launcher/blob/master/README.md#pedagogy) according to the subtasks defined in the [Early Grade Reading Assessment](https://globalreadingnetwork.net/resources/early-grade-reading-assessment-egra-toolkit-second-edition) (EGRA) and [Early Grade Mathematics Assessment](https://www.globalpartnership.org/content/early-grade-mathematics-assessment-egma-conceptual-framework-based-mathematics-skills) (EGMA) standards.


<a name="ai"></a>
## Artificial Intelligence (AI) 🤖

Using [TensorFlow](https://www.tensorflow.org/), one machine learning model is trained per language, for each of these categories:

  * Handwriting recognition (letters)
  * Handwriting recognition (numbers)
  * [Content recommendation (storybooks)](https://github.com/elimu-ai/ml-storybook-recommender)
  * Content recommendation (videos)

The [elimu.ai Crowdsource](https://github.com/elimu-ai/crowdsource) Android app is used for _labeling_ handwritten letters and numbers.


---

## About the elimu.ai Community

![elimu ai-tagline](https://user-images.githubusercontent.com/15718174/54360503-e8e88980-465c-11e9-9792-32b513105cf3.png)

 * For a high-level description of the project, see https://github.com/elimu-ai/wiki/blob/master/README.md.
 * For project milestones, see https://github.com/elimu-ai/wiki/projects.

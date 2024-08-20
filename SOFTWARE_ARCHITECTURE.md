![xprize-no-text_banner](https://user-images.githubusercontent.com/15718174/82723985-51250780-9d05-11ea-8fc6-e800d9b414eb.png)
> A collection of educational Android apps teaches children basic literacy and numeracy in a fun and engaging way.

# elimu.ai Software Architecture 📐

###### Table of contents
  1. [Learning Platform](#learning-platform)
  1. [Software Dependencies](#dependencies)
  1. [Software Scalability](#scalability)
  1. [Data Collection](#data-collection)
  1. [Artificial Intelligence (AI)](#ai)


<a name="learning-platform"></a>

## Learning Platform

The elimu.ai software is a _platform_ of educational content and Android [apps](https://eng.elimu.ai/apps).

> [!NOTE]
> Instead of having one large Android application containing everything, the elimu.ai software has been architected such that there are many smaller applications, each with their own specific responsibility.

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

The software platform is being built to handle scaling to many different languages. A collection of many smaller apps, all [categorized](https://github.com/elimu-ai/launcher/blob/main/README.md#pedagogy) by literacy/numeracy skills makes it possible to easily adjust the complete curriculum when localizing from one language to another.

The file size of the apps, games and multimedia is kept as small as possible in order to make the distribution easier in locations with limited Internet connectivity. In addition, the software has been designed to work offline so that it can be used in remote areas.

<a name="localization"></a>

### Localization 🌐

For instructions on how to add support for a new language, see [LOCALIZATION.md](LOCALIZATION.md).


<a name="crowdsourcing"></a>

### Content Crowdsourcing ✍🏽

Another way to ensure software scalability is through _crowdsourcing_. By using the [elimu.ai Webapp](https://github.com/elimu-ai/webapp), the crowd is able to upload and peer review educational content on the platform, and thus help speed up the expansion to more languages.


<a name="data-collection"></a>

## Data Collection 📊

In order to measure how well the elimu.ai software is working, usage data is collected from the Android devices so that we can analyze the learning of each child. This enables us to carefully monitor how changes in code or content produce different learning outcome, as well as continuously improve the software.

The data is synced between the Android devices and the webapp's [REST API](https://github.com/elimu-ai/webapp/tree/main/src/main/java/ai/elimu/rest) whenever an Internet connection is available.

For assessing the learning outcome of the children, we are collecting data [categorized](https://github.com/elimu-ai/launcher/blob/main/README.md#pedagogy) according to the subtasks defined in the [Early Grade Reading Assessment](https://globalreadingnetwork.net/resources/early-grade-reading-assessment-egra-toolkit-second-edition) (EGRA) and [Early Grade Mathematics Assessment](https://www.globalpartnership.org/content/early-grade-mathematics-assessment-egma-conceptual-framework-based-mathematics-skills) (EGMA) standards.


<a name="ai"></a>

## Artificial Intelligence (AI) 🤖

Using [TensorFlow](https://www.tensorflow.org/), one machine learning model is trained per language, for each of these categories:

  * Handwriting recognition (letters)
  * Handwriting recognition (numbers)
  * [Content recommendation (storybooks)](https://github.com/elimu-ai/ml-storybook-recommender)
  * Content recommendation (videos)

We are also building machine learning models that work across languages. As an example, the same model used for predicting the reading level of English storybooks can be used for predicting the reading level of Hindi storybooks.

* [Storybook reading level prediction](https://github.com/elimu-ai/ml-storybook-reading-level)

---

<p align="center">
  <img src="https://github.com/elimu-ai/webapp/blob/main/src/main/webapp/static/img/logo-text-256x78.png" />
</p>
<p align="center">
  elimu.ai - Free open-source learning software for out-of-school children ✨🚀
</p>
<p align="center">
  <a href="https://elimu.ai">Website 🌐</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/elimu-ai/wiki#readme">Wiki 📃</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/orgs/elimu-ai/projects?query=is%3Aopen">Projects 👩🏽‍💻</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/elimu-ai/wiki/milestones">Milestones 🎯</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/elimu-ai/wiki#open-source-community">Community 👋🏽</a>
  &nbsp;•&nbsp;
  <a href="https://www.drips.network/app/drip-lists/41305178594442616889778610143373288091511468151140966646158126636698">Support 💜</a>
</p>

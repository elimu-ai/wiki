# elimu.ai Localization 🇺🇸🇵🇭🇮🇳

## Software Architecture

The elimu.ai software is architected such that a collection of infrastructural and educational Android apps can be re-used across a variety of languages. One [webapp](https://github.com/elimu-ai/webapp) can be configured per language for hosting the educational content:

[
  <img width="320" alt="Software Architecture" src="https://user-images.githubusercontent.com/15718174/83595568-fb6a1e00-a594-11ea-990a-10c0bd62ed11.png">
](https://github.com/elimu-ai/wiki/blob/main/SOFTWARE_ARCHITECTURE.md)

## Currently Supported Languages

A list of the currently supported languages is available at https://github.com/elimu-ai/model/blob/main/src/main/java/ai/elimu/model/v2/enums/Language.java


## How to Add Support for a New Language

When adding support for a new language to the [elimu.ai](http://elimu.ai) platform, there are two types of activities that need to be handled:

  1. Software Engineering: Add support for the new language to the code (webapp & Android apps/games)
  2. Content Creation: Add the educational content for the new language (using the [webapp](https://github.com/elimu-ai/webapp))


### Introduction

When adding support for a new language, there are 6 infrastructure components that need to be updated:

Component | Description
------------ | -------------
[model](https://github.com/elimu-ai/model) | Common Java classes shared amongst the webapp and appstore
[webapp](https://github.com/elimu-ai/webapp) | Web application for uploading and hosting Android apps and educational content
[appstore](https://github.com/elimu-ai/appstore) | Android Appstore application for downloading Android apps to tablets and installing them
[launcher](https://github.com/elimu-ai/launcher) |	Android application providing a structured path when accessing the educational apps
[content-provider](https://github.com/elimu-ai/content-provider)	| Android application which downloads educational content from the webapp's REST API to the device and provides it to other apps
[analytics](https://github.com/elimu-ai/analytics)	| Android application which collects usage activity from the educational apps and uploads it to the webapp's REST API

### Update Infrastructure Apps: Step-by-Step Guide

Perform the following steps in order to add a new language:

#### 1. [model](https://github.com/elimu-ai/model): Add the Language Code to the List of Supported Languages

*Time estimate: 30-60 minutes*

- Add the country code to https://github.com/elimu-ai/model/blob/main/src/main/java/ai/elimu/model/enums/Language.java
- Create a [pull request](https://github.com/elimu-ai/wiki/blob/main/CONTRIBUTING.md) for your changes (see [example](https://github.com/elimu-ai/model/pull/214/files)).
- Once your changes have been approved, the model library will be released with a new version number which can be found at https://github.com/elimu-ai/model/releases.

#### 2. [webapp](https://github.com/elimu-ai/webapp): Update the Model Library in the Webapp to the Latest Version

*Time estimate: 1-2 hours*

- The webapp needs to update its model dependency version to get access to use the newly added Language enum.
- Adjust the model version in [pom.xml](https://github.com/elimu-ai/webapp/blob/main/pom.xml) by updating the `<model.version>` attribute (see [example](https://github.com/elimu-ai/webapp/pull/1135/files)).
- Add Subdomain for the New Language
   - Next, we need to configure a subdomain for the new language, e.g. https://hin.elimu.ai for Hindi.
   - This subdomain will be used when visitors want to navigate the webapp using another content language than the default English. Also, the [appstore](https://github.com/elimu-ai/appstore) Android application will be using this subdomain when downloading applications and content for the new language. Similarly, the [analytics](https://github.com/elimu-ai/analytics) Android application will be uploading usage data to the same subdomain.
   - To initiate this domain and server configuration, notify us via info@elimu.ai or contact us via [Discord](https://discord.gg/9rz4XYJJDE).

### Update _Existing_ Educational Apps/Games: Step-by-Step Guide

...

### Upload _New_ Educational Apps/Games: Step-by-Step Guide

...

<a name="add-educational-content"></a>
### Add Educational Content: Step-by-Step Guide

...

#### Using Website

* Adding Letters [TODO]
* Adding Sounds (Allophones) [TODO]
* Adding Letter-Sound Correspondences [TODO]
* [Adding Words 💬](https://github.com/elimu-ai/webapp/blob/main/LOCALIZE.md#adding-words)
* Adding Numbers [TODO]
* [Adding Audio Recordings 🎶🎙️](https://github.com/elimu-ai/webapp/blob/main/LOCALIZE.md#adding-audio-recordings-%EF%B8%8F)
* Adding Storybooks [TODO]
* Adding Videos [TODO]

#### Using Crowdsourcing App

...

---

## About the elimu.ai Community

![elimu ai-tagline](https://user-images.githubusercontent.com/15718174/54360503-e8e88980-465c-11e9-9792-32b513105cf3.png)

 * For a high-level description of the project, see https://github.com/elimu-ai/wiki/blob/main/README.md.
 * For project milestones, see https://github.com/elimu-ai/wiki/projects.

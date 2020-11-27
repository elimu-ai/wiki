# elimu.ai Localization

## Software Architecture

The elimu.ai software is architected such that a collection of infrastructural and educational Android apps can be re-used across a variety of languages. One [webapp](https://github.com/elimu-ai/webapp) can be configured per language for hosting the educational content:

[
  <img width="320" alt="Software Architecture" src="https://user-images.githubusercontent.com/15718174/83595568-fb6a1e00-a594-11ea-990a-10c0bd62ed11.png">
](https://github.com/elimu-ai/wiki/blob/master/SOFTWARE_ARCHITECTURE.md)

## Currently Supported Languages

A list of the currently supported languages is available at https://github.com/elimu-ai/model/blob/master/src/main/java/ai/elimu/model/enums/Language.java


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
[analytics](https://github.com/elimu-ai/analytics)	| Android application which collects usage activity from the educational apps and uploads it to the webapp

### Update Infrastructure Apps: Step-by-Step Guide

Perform the following steps in order to add a new language:

#### 1. [model](https://github.com/elimu-ai/model): Add the Language Code to the List of Supported Languages

*Time estimate: 30-60 minutes*

Add the country code to https://github.com/elimu-ai/model/blob/master/src/main/java/ai/elimu/model/enums/Language.java

Create a [pull request](https://github.com/elimu-ai/wiki/blob/master/CONTRIBUTING.md) for your changes (see [example](https://github.com/elimu-ai/model/pull/214/files)).

Once your changes have been approved, the model library will be released with a new version number which can be found at https://github.com/elimu-ai/model/releases.

### Update _Existing_ Educational Apps/Games: Step-by-Step Guide

...

### Upload _New_ Educational Apps/Games: Step-by-Step Guide

...

<a name="add-educational-content"></a>
### Add Educational Content: Step-by-Step Guide

...

#### Using Website

...

#### Using Crowdsourcing App

...

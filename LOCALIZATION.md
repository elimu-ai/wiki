# elimu.ai Localization


## How to Add Support for a New Language

When adding support for a new language to the [elimu.ai](http://elimu.ai) platform, there are two types of activities that need to be handled:

  1. Add support for the new language to the code (Android apps/games)
  2. Add the educational content for the new language (using the [webapp](https://github.com/elimu-ai/webapp))


### Introduction

When adding support for a new language, there are 6 infrastructure components that need to be updated:

![software_architecture](https://user-images.githubusercontent.com/15718174/50562025-59dbfe80-0d08-11e9-9e86-3c69b860f0d3.png)

Component | Description
------------ | -------------
[model](https://github.com/elimu-ai/model) | Common Java classes shared amongst the webapp and appstore
[webapp](https://github.com/elimu-ai/webapp) | Web application for uploading Android apps and content
[appstore](https://github.com/elimu-ai/appstore) | Android Appstore application for downloading Android apps to tablets and installing them
[launcher](https://github.com/elimu-ai/launcher) |	Android application providing a structured path when accessing the educational apps
[content-provider](https://github.com/elimu-ai/content-provider)	| Android application which downloads educational content to tablets and provides it to other apps
[analytics](https://github.com/elimu-ai/analytics)	| Android application which collects usage activity from the educational apps and uploads it to the webapp

### Update Infrastructure Apps: Step-by-Step Guide

...

### Update Existing Educational Apps/Games: Step-by-Step Guide

...

### Upload New Educational Apps/Games: Step-by-Step Guide

...

### Add Educational Content to the Website: Step-by-Step Guide

...

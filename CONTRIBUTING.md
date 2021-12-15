# Contributing to the elimu.ai Community 👩🏽‍💻

The purpose of [elimu.ai](http://elimu.ai) is to provide disadvantaged children with access to quality 
basic education. We believe that a free quality education is the right of every child no matter her 
social or geographical background.

For this reason, we build educational software that teaches a child to read, write and calculate 
fully autonomously, without guidance from qualified teachers.

Since [elimu.ai](http://elimu.ai) is an open source project, anyone is welcome to contribute towards this 
goal. We welcome different skills, cultures, perspectives, attitudes, and experiences.

This document explains the step-by-step process and guidelines for contributing to any of the 
repositories in the elimu.ai [GitHub organization](https://github.com/elimu-ai).

Each repository has a maintainer responsible for reviewing code submitted by contributors. 
The appointment of maintainers and lead maintainers is based on previous contributions (meritocracy).

## Contributor Workflow 🔀

### Outside Contributor vs Core Contributor

The first step is to decide what _type_ of contributor you are. In general, every contributor would 
belong to one of the following:

   1. _Outside_ contributor
   
      Being an outside contributor means that you have not been added to the 
      elimu.ai [GitHub organization](https://github.com/elimu-ai). In practice this means that you 
      do not have access to create new repositories or repository branches.
      
   2. _Core_ contributor

      Being a core contributor means that you have been added to the elimu.ai 
      [GitHub organization](https://github.com/elimu-ai). This gives you access to create new 
      repositories and repository branches.

### How to Know Which Task to Work On

   1. Each application has its own GitHub repository. Start by identifying a repository in which you 
   would like to contribute: https://github.com/elimu-ai
   
   2. Look at the code in the repository to see if your skills match those required. If in doubt, 
   post your questions in the [Slack channel](https://join.slack.com/t/elimu-ai/shared_invite/zt-eoc921ow-0cfjATlIF2X~zHhSgSyaAw) 
   or send an e-mail to info@elimu.ai.
   
   3. When you have selected a repository, click the 
   ["Projects"](https://github.com/elimu-ai/appstore/projects) tab of the repository. Within each 
   project you will see a collection of issues, and the state of each one (_To do_, _In progress_, 
   _Done_). Feel free to start working on any issue in the left-hand "To do" column.
   
   4. If you feel lost, take a look at the issues labeled with `good first issue`. These are tasks 
   that are considered as good entry-points for first-time contributors. See 
   [example](https://github.com/elimu-ai/appstore/issues?q=is%3Aissue+is%3Aopen+label%3A"good+first+issue").
   
   5. You are also welcome to create new GitHub issues yourself. For example, if you have discovered 
   a bug, or want to suggest a new feature, press the "New issue" button.
      
### How to Implement and Submit Your Work

Once you have identified a task to work on, there is a specific workflow that you should follow. This 
workflow is mostly identical for both outside and core contributors, except from the way to create a 
new GitHub branch to work on (Step 1):

   1. If you are an outside contributor, _fork_ the repository to your own GitHub account. (If you are 
   a core contributor, you will create a new branch directly in the main repository.)

   2. Create a new _branch_ for the GitHub issue that you will be working on. If, for example the issue 
   you have picked is titled "Upgrade to the latest Gradle version" and has the issue number 57, 
   create a new branch with the title "57 Upgrade to the latest Gradle version". By having the issue 
   number in the branch name, it's easier to understand which issue the branch is for.
   
   3. Remember to include a reference to the GitHub issue number for each commit to make it easier for 
   future contributors to understand each code change. E.g. "#57 Upgraded to Gradle 4.1".
   
   4. Keep each commit small so that diffs are easy to read and understand for people looking at your 
   code in the future. A pull request should always be focused to doing one thing, for example fixing 
   a bug or adding a new feature, but not a mixture. Avoid large commits and pull requests which 
   attempt to do too much at once, as this makes code review difficult.
   
   5. If you want to add things like formatting fixes or refactoring, etc, do _not_ mix those with 
   the actual code change related to an issue. To make the actual code change easier to read, separate 
   refactoring into a new branch (and a new issue).
   
   6. Once you are ready to receive feedback on your branch, create a _pull request_ for merging it 
   into the `master` branch.

   7. Every pull request requires at least one approved peer review before being merged, so add at 
   least one person as a _code reviewer_ of your pull request. To find out who to add, click 
   "Insights" → "Contributors" too see an overview of the most active contributors for each 
   repository. If you are unsure who to add, use these: [`nya-elimuai`](https://github.com/nya-elimuai), 
   [`jo-elimuai`](https://github.com/jo-elimuai) and [`gscdev`](https://github.com/gscdev).
   
   8. Once your pull request has been reviewed and approved, it can be merged. The person who created 
   the branch (you) will be the person responsible for merging the branch. So the peers reviewing 
   your code will not merge the branch; that is your responsibility.
   
   9. If you consider the issue complete (code reviewed and tested), merge and delete the branch, and 
   move the GitHub issue to the "Done" column. Well done! 👏

<a name="workflow-example-webapp"></a>
## Workflow Example: [webapp](https://github.com/elimu-ai/webapp)

### Introduction

As an outside collaborator, you are free to fork the repository and create pull requests from your fork. 

However, as a core contributor who has been added to the [GitHub organization](https://github.com/elimu-ai), 
the work flow looks like this:

### Work Flow

1. Select a GitHub issue to work on. Either select an existing issue from https://github.com/elimu-ai/webapp/projects 
or create a new one.

2. Create a branch for the GitHub issue. For example, if your GitHub issue is titled "Update Java version" and has the issue number 567, create a new branch with the title "#567 Update Java version" by pressing the branch button (or by using GitHub Desktop):

   ![screen shot 2017-11-11 at 11 09 21](https://user-images.githubusercontent.com/1451036/32688430-d1b9fc88-c6d0-11e7-8e20-10a10c028d0a.png) .  ![screen shot 2017-11-11 at 11 10 56](https://user-images.githubusercontent.com/1451036/32688437-12fc5f6a-c6d1-11e7-9a38-b34479356522.png)

3. Switch to the branch you created and implement your code changes on that branch. Remember to include the GitHub issue 
for each commit to make it easier for future contributors to understand each code change.

4. Once ready for testing, create a pull request for your branch for merging it into the `master` branch. Your pull 
request needs at least one approved review in order to be merged. When assigning reviewers, add one or more of the project's 
[maintainers](https://github.com/elimu-ai/webapp/blob/master/CODEOWNERS):

   * [`nya-elimuai`](https://github.com/nya-elimuai)
   * [`jo-elimuai`](https://github.com/jo-elimuai)
   * [`gscdev`](https://github.com/gscdev)
   
   If the maintainers are too slow to get back to you, send an e-mail to info@elimu.ai or contact us via [Slack](https://join.slack.com/t/elimu-ai/shared_invite/zt-eoc921ow-0cfjATlIF2X~zHhSgSyaAw).
   
5. Once your pull request has been approved by at least one project maintainer, press the "merge" button. This will merge 
your code changes into the `master` branch and deploy them to the test servers at http://`<language>`.test.elimu.ai.

6. If all of the regression tests pass (see [Jenkins](http://jenkins.elimu.ai:8080), ask a maintainer to deploy the changes to the production servers at http://`<language>`.elimu.ai.


---

If any of the above steps are unclear, or you have any other questions or comments, please reach out via info@elimu.ai or [Slack](https://join.slack.com/t/elimu-ai/shared_invite/zt-eoc921ow-0cfjATlIF2X~zHhSgSyaAw). Thank you for contributing 😀


## elimu.ai Community - Open Source Contributors 🙌

&nbsp; | &nbsp; | &nbsp;
:---: | :---: | :---:
<img src="https://avatars1.githubusercontent.com/u/15718174?s=96&v=4" width="80" /><br />Nya Ξlimu<br />Literacy/Numeracy Tutoring | <img src="https://avatars1.githubusercontent.com/u/8291318?s=96&v=4" width="80" /><br />Gema Sánchez<br />Android Development | <img src="https://avatars2.githubusercontent.com/u/1451036?s=460&v=4" width="80" /><br />Jo G.<br />Software Architecture
<img src="https://avatars.githubusercontent.com/u/66638701?s=88&v=4" width="80" /><br />Somila Dayile<br />Content Creation & UX | <img src="https://avatars.githubusercontent.com/u/17663679?v=4" width="80" /><br />Umendra Rajapakshe<br />Web Development | <img src="https://avatars.githubusercontent.com/u/19628734?v=4" width="80" /><br />Keerthi<br />Web Development
<img src="https://avatars3.githubusercontent.com/u/25285328?s=96&v=4" width="80" /><br />George Karanja<br />Translation | <img src="https://avatars3.githubusercontent.com/u/523586?s=460&v=4" width="80" /><br />German Torres<br />Game Development | <img src="https://avatars0.githubusercontent.com/u/1878335?s=96&v=4" width="80" /><br />Diego Wald<br />Game Development
<img src="https://avatars3.githubusercontent.com/u/2552297?s=96&v=4" width="80" /><br />Olha Yevtushenko<br />Game Development | <img src="https://avatars3.githubusercontent.com/u/4211470?s=96&v=4" width="80" /><br />Thomas Barthélémy<br />Android Development | <img src="https://avatars0.githubusercontent.com/u/3321467?s=96&v=4" width="80" /><br />Vincent Barthélémy<br />Android Development
<img src="https://odesk-prod-portraits.s3.amazonaws.com/Users:moepwint:PortraitUrl_100?AWSAccessKeyId=AKIAIKIUKM3HBSWUGCNQ&Expires=2147483647&Signature=pVu9YEDnZxv7OBvu%2Fjtx2lKABiY%3D" width="80" /><br />Moe Pwint<br />UX/UI Design | <img src="https://avatars0.githubusercontent.com/u/150637?s=96&v=4" width="80" /><br />Bikash Agrawal<br />Big Data & Machine Learning | <img src="https://avatars3.githubusercontent.com/u/20489471?s=96&v=4" width="80" /><br />Mike Schälchli<br />AI & Machine Learning
<img src="https://avatars3.githubusercontent.com/u/15183317?s=96&v=4" width="80" /><br />Suman Dev<br />Android Development | <img src="https://avatars2.githubusercontent.com/u/20499268?s=460&v=4" width="80" /><br />Eli Hasson<br />Android Development | <img src="https://fiverr-res.cloudinary.com/t_profile_original,q_auto,f_auto/profile/photos/58798059/original/photo-2.JPG" width="80" /><br />Melissa Fabregas<br />Voice Acting | <img src="https://avatars3.githubusercontent.com/u/4281969?s=96&v=4" width="80" /><br />Tuan Ngyen<br />Android Development
<img src="https://avatars1.githubusercontent.com/u/556222?s=96&v=4" width="80" /><br />Michael Sladoje<br />AI & Machine Learning | <img src="https://avatars2.githubusercontent.com/u/19466943?s=96&v=4" width="80" /><br />Alin Mureșan<br />Content Creation

---

## About the elimu.ai Community

![elimu ai-tagline](https://user-images.githubusercontent.com/15718174/54360503-e8e88980-465c-11e9-9792-32b513105cf3.png)

 * For a high-level description of the project, see https://github.com/elimu-ai/wiki/blob/master/README.md.
 * For project milestones, see https://github.com/elimu-ai/wiki/projects.

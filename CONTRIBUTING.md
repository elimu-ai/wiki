# Contributing to elimu.ai 👩🏽‍💻

The purpose of [elimu.ai](https://elimu.ai) is to provide disadvantaged children with access to quality 
basic education. We believe that a quality basic education is the right of every child no matter her 
social or geographical background.

For this reason, we build educational technology that teaches a child to read, write and calculate 
fully autonomously, without guidance from qualified teachers.

Since [elimu.ai](https://elimu.ai) is an _open source_ project, anyone is welcome to contribute towards this 
goal. We welcome different skills, cultures, perspectives, attitudes, and experiences. Also see our 
[Code of Conduct](CODE_OF_CONDUCT.md).

This document explains the step-by-step process and guidelines for contributing to any of the 
repositories in the elimu.ai [GitHub organization](https://github.com/elimu-ai).

Each GitHub repository has a maintainer responsible for reviewing code submitted by contributors. 
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

   1. Each Android application has its own GitHub repository. Start by identifying a repository in which you 
   would like to contribute: https://github.com/elimu-ai. And to get an understanding of the overall software 
   architecture, see https://github.com/elimu-ai/wiki/blob/main/SOFTWARE_ARCHITECTURE.md.
   
      [<img width="320" alt="Software Architecture" src="https://user-images.githubusercontent.com/15718174/83595568-fb6a1e00-a594-11ea-990a-10c0bd62ed11.png">](https://github.com/elimu-ai/wiki/blob/main/SOFTWARE_ARCHITECTURE.md)
   
   2. Look at the code in the repository to see if your skills match those required. If in doubt, 
   post your questions in [Discord](https://discord.gg/9rz4XYJJDE) or send an e-mail to info@elimu.ai.
   
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
   create a new branch with a title like `chore: #57 Upgrade to the latest Gradle version`. By having the 
   issue number in the branch name, it's easier to understand which issue the branch is for.
   
   3. Remember to include a reference to the GitHub issue number for each commit to make it easier for 
   future contributors to understand each code change. E.g. `chore: #57 Upgrade to Gradle 4.1`.
   
   4. Keep each commit small so that diffs are easy to read and understand for people looking at your 
   code in the future. A pull request should always be focused to doing one thing, for example fixing 
   a bug or adding a new feature, but not a mixture. Avoid large commits and pull requests which 
   attempt to do too much at once, as this makes code review difficult.
   
   5. If you want to add things like formatting fixes or refactoring, etc, do _not_ mix those with 
   the actual code change related to an issue. To make the actual code change easier to read, separate 
   refactoring into a new branch (and a new issue).
   
   6. Once you are ready to receive feedback on your branch, create a _pull request_ for merging it 
   into the `main` branch.

   7. Every pull request requires at least one approved peer review before being merged, so add at 
   least one person as a _code reviewer_ of your pull request. To find out who to add, click 
   "Insights" → "Contributors" too see an overview of the most active contributors for each 
   repository. If you are unsure who to add, use these: [`nya-elimu`](https://github.com/nya-elimu), 
   [`jo-elimu`](https://github.com/jo-elimu) and [`gscdev`](https://github.com/gscdev).
   
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

1. Select a GitHub issue to work on. Either select an existing issue from https://github.com/elimu-ai/webapp/projects or create a new one.

2. Create a branch for the GitHub issue. For example, if your GitHub issue is titled "Update Java version" and has the issue number 567, create a new branch with the title "#567 Update Java version" by pressing the branch button (or by using GitHub Desktop):

   ![](https://user-images.githubusercontent.com/1451036/32688430-d1b9fc88-c6d0-11e7-8e20-10a10c028d0a.png) .  ![](https://user-images.githubusercontent.com/1451036/32688437-12fc5f6a-c6d1-11e7-9a38-b34479356522.png)

3. Switch to the branch you created and implement your code changes on that branch. Remember to include the GitHub issue for each commit to make it easier for future contributors to understand each code change.

4. Once ready for testing, create a pull request for your branch for merging it into the `main` branch. Your pull request needs at least one approved review in order to be merged. When assigning reviewers, add one or more of the project's 
[maintainers](https://github.com/elimu-ai/webapp/blob/main/CODEOWNERS):

   * [`nya-elimu`](https://github.com/nya-elimu)
   * [`jo-elimu`](https://github.com/jo-elimu)
   * [`gscdev`](https://github.com/gscdev)
   
   If the maintainers are too slow to get back to you, reach out to the [open source community](README.md#open-source-community) via chat or e-mail.
   
5. Once your pull request has been approved by at least one project maintainer, press the "merge" button. This will merge your code changes into the `main` branch and deploy them to the test servers at https://`<language>`.test.elimu.ai.

6. If all of the regression tests pass, ask a maintainer to deploy the changes to the production servers at https://`<language>`.elimu.ai.


---

If any of the above steps are unclear, or you have any other questions or comments, please reach out to the [community](README.md#open-source-community) via chat or e-mail. Thank you for contributing 😀


<a name="open-source-contributors"></a>
## elimu.ai - Open Source Contributors 🙌🏽

&nbsp; | &nbsp; | &nbsp;
:---: | :---: | :---:
[<img src="https://avatars1.githubusercontent.com/u/15718174?s=96&v=4" width="80" /><br />Nya Ξlimu](https://github.com/nya-elimu)<br />Literacy/Numeracy Tutoring | [<img src="https://avatars1.githubusercontent.com/u/8291318?s=96&v=4" width="80" /><br />Gema Sánchez](https://github.com/gscdev)<br />Android Development | [<img src="https://avatars2.githubusercontent.com/u/1451036?s=460&v=4" width="80" /><br />Jo G.](https://github.com/jo-elimu)<br />Software Architecture
[<img src="https://avatars.githubusercontent.com/u/66638701?s=88&v=4" width="80" /><br />Somila Dayile](https://github.com/So-Somila)<br />Content Creation & UX | [<img src="https://avatars.githubusercontent.com/u/17663679?v=4" width="80" /><br />Umendra Rajapakshe](https://github.com/UmenR)<br />Web Development | [<img src="https://avatars.githubusercontent.com/u/19628734?v=4" width="80" /><br />Keerthi](https://github.com/Keerthi4308)<br />Web Development
[<img src="https://avatars3.githubusercontent.com/u/25285328?s=96&v=4" width="80" /><br />George Karanja](https://github.com/georgekaranja)<br />Translation | [<img src="https://avatars3.githubusercontent.com/u/523586?s=460&v=4" width="80" /><br />German Torres](https://github.com/protito)<br />Game Development | [<img src="https://avatars0.githubusercontent.com/u/1878335?s=96&v=4" width="80" /><br />Diego Wald](https://github.com/diegowald)<br />Game Development
<img src="https://avatars3.githubusercontent.com/u/2552297?s=96&v=4" width="80" /><br />Olha Yevtushenko<br />Game Development | <img src="https://avatars3.githubusercontent.com/u/4211470?s=96&v=4" width="80" /><br />Thomas Barthélémy<br />Android Development | <img src="https://avatars0.githubusercontent.com/u/3321467?s=96&v=4" width="80" /><br />Vincent Barthélémy<br />Android Development
<img src="https://media.licdn.com/dms/image/D5635AQEEkh2dm2pCsA/profile-framedphoto-shrink_100_100/0/1697422174135?e=1698152400&v=beta&t=ubwg0KQtuFp6BjBDmhXmCjtJ0q7b-Scw5qgJXxjq284" width="80" /><br />Moe Pwint<br />UX/UI Design | <img src="https://avatars0.githubusercontent.com/u/150637?s=96&v=4" width="80" /><br />Bikash Agrawal<br />Big Data & Machine Learning | <img src="https://avatars3.githubusercontent.com/u/20489471?s=96&v=4" width="80" /><br />Mike Schälchli<br />AI & Machine Learning
<img src="https://avatars3.githubusercontent.com/u/15183317?s=96&v=4" width="80" /><br />Suman Dev<br />Android Development | <img src="https://avatars2.githubusercontent.com/u/20499268?s=460&v=4" width="80" /><br />Eli Hasson<br />Android Development | <img src="https://fiverr-res.cloudinary.com/t_profile_original,q_auto,f_auto/profile/photos/58798059/original/photo-2.JPG" width="80" /><br />Melissa Fabregas<br />Voice Acting | <img src="https://avatars3.githubusercontent.com/u/4281969?s=96&v=4" width="80" /><br />Tuan Ngyen<br />Android Development
<img src="https://avatars1.githubusercontent.com/u/556222?s=96&v=4" width="80" /><br />Michael Sladoje<br />AI & Machine Learning | <img src="https://avatars2.githubusercontent.com/u/19466943?s=96&v=4" width="80" /><br />Alin Mureșan<br />Content Creation | <img src="https://avatars.githubusercontent.com/u/1272158?v=4" width="80" /><br />Homayoun<br />Web3 Development
<img src="https://avatars.githubusercontent.com/u/17800493?v=4" width="80" /><br />Sajid Patel<br />Content Creation | <img src="https://avatars.githubusercontent.com/u/85966562?v=4" width="80" /><br />Jain Anuradha<br />Content Creation | <img src="https://avatars.githubusercontent.com/u/57134382?v=4" width="80" /><br />Sandun Abeysooriya<br />Web Development
<img src="https://avatars.githubusercontent.com/u/75719979?v=4" width="80" /><br />Anmol Kumar<br />Content Creation | <img src="https://avatars.githubusercontent.com/u/85234598?v=4" width="80" /><br />Bender Rodríguez<br />Web3 Development | <img src="https://avatars.githubusercontent.com/u/25884741?v=4" width="80" /><br />Shubham Vishwakarma<br />Web Development
<img src="https://avatars.githubusercontent.com/u/16896956?v=4" width="80" /><br />Arvind<br />Web Development | <img src="https://avatars.githubusercontent.com/u/7117993?v=4" width="80" /><br />Dalton Craven<br />Web3 Development | <img src="https://avatars.githubusercontent.com/u/75578392?v=4" width="80" /><br />John Grimm<br />Web3 Development
<img src="https://avatars.githubusercontent.com/u/23047698?v=4" width="80" /><br />Jairo<br />Web Development | <img src="https://avatars.githubusercontent.com/u/5686985?v=4" width="80" /><br />Harsh Acharya<br />Scaling & Distribution | <img src="https://avatars.githubusercontent.com/u/29434041?v=4" width="80" /><br />Amal Jos<br />Engineering QA
<img src="https://avatars.githubusercontent.com/u/1363884?v=4" width="80" /><br />Jaimin<br />Engineering QA | <img src="https://avatars.githubusercontent.com/u/87644499?v=4" width="80" /><br />Chiara Mazza<br />Linguistics | <img src="https://avatars.githubusercontent.com/u/866225?v=4" width="80" /><br />Sinu John<br />Android Development
[<img src="https://avatars.githubusercontent.com/u/4281969?v=4" width="80" />](https://github.com/tuancoltech)<br />Tuan Nguyen<br />Android Development |


---

elimu.ai - Free open source learning software for put-of-school children ✨🚀

[Website 🌐](https://elimu.ai) &nbsp; [Wiki 📃](https://github.com/elimu-ai/wiki#readme) &nbsp; [Projects 👩🏽‍💻](https://github.com/orgs/elimu-ai/projects?query=is%3Aopen) &nbsp; [Milestones 🎯](https://github.com/elimu-ai/wiki/milestones) &nbsp; [Community 👋🏽](https://github.com/elimu-ai/wiki#open-source-community)

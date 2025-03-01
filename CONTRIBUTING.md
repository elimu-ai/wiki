# Contributing to elimu.ai 👩🏽‍💻

The mission of elimu.ai is to build innovative learning software that empowers out-of-school 
children to teach themselves basic reading📖, writing✍🏽, and math🔢 within 6 months.

We believe that having the _opportunity_ to learn these foundational life skills should be 
the right of every child, not matter her social or geographical background. This is currently 
not the case for 10% of the human population of primary age (6-11 years old), who are out-of-school.

Since elimu.ai is an _open source_ project, anyone is welcome to contribute towards this 
goal. We welcome different skills, cultures, perspectives, attitudes, and experiences. Also see our 
[Code of Conduct](CODE_OF_CONDUCT.md).

This document explains the step-by-step process and guidelines for contributing to any of the 
repositories in the elimu.ai [GitHub organization](https://github.com/elimu-ai).

Each GitHub repository has maintainers responsible for reviewing code submitted by contributors. 
The appointment of maintainers is based on previous contributions (meritocracy).

## Contributor Workflow 🔀

### Outside Contributor vs Core Contributor

The first step is to decide what _type_ of contributor you are. In general, every contributor would 
belong to one of the following:

   1. _Outside_ contributor
   
      Being an outside contributor means that you have not been added to the 
      elimu.ai [GitHub organization](https://github.com/elimu-ai). In practice this means that you 
      do not have access to create new repositories or new repository branches.
      
   2. _Member_ contributor

      Being a member contributor means that you have been added to the elimu.ai 
      [GitHub organization](https://github.com/elimu-ai). This gives you access to create new 
      repositories and repository branches.

### How to Know Which Task to Work On

   1. Each Android app/game has its own GitHub repository. Start by identifying a repository in
   which you would like to contribute: https://github.com/elimu-ai. And to get an understanding
   of the overall software architecture, see https://github.com/elimu-ai/wiki/blob/main/SOFTWARE_ARCHITECTURE.md.
   
      [<img width="320" alt="Software Architecture" src="https://user-images.githubusercontent.com/15718174/83595568-fb6a1e00-a594-11ea-990a-10c0bd62ed11.png">](https://github.com/elimu-ai/wiki/blob/main/SOFTWARE_ARCHITECTURE.md)
   
   3. Look at the code in the repository to see if your skills match those required. If in doubt, 
   post your questions in our [Community Chat 👋🏽]([https://discord.gg/9rz4XYJJDE](https://github.com/elimu-ai/wiki/blob/main/README.md#community-chat))
   or send an e-mail to info@elimu.ai.
   
   4. When you have selected a repository, click the 
   ["Issues"](https://github.com/elimu-ai/appstore/issues) tab of the repository. Within each 
   project you will see a collection of issues. Feel free to start working on any issue that
   has not already been assigned to another contributor.
   
   6. If you feel lost, take a look at the issues labeled <kbd>good first issue</kbd>. These are tasks 
   that are considered as good entry-points for first-time contributors. Here are some examples:
      - https://github.com/elimu-ai/webapp/contribute
      - https://github.com/elimu-ai/content-provider/contribute
      - https://github.com/elimu-ai/analytics/contribute
      - https://github.com/elimu-ai/vitabu/contribute
      - https://github.com/elimu-ai/kukariri/contribute
   
   7. You are also welcome to create new GitHub issues yourself. For example, if you have discovered 
   a bug or want to suggest a new feature, press the "New issue" button.
      
### How to Implement and Submit Your Work

Once you have identified a task to work on, there is a specific workflow that you should follow. This 
workflow is mostly identical for both outside and member contributors, except from the way to create a 
new GitHub branch to work on (Step 1):

   1. If you are an outside contributor, _fork_ the repository to your own GitHub account. (If you are 
   a member contributor, you will create a new branch directly in the main repository.)

   2. Create a new _branch_ for the GitHub issue that you will be working on. If, for example the issue 
   you have picked is titled "Upgrade to the latest Gradle version", create a new branch with a title
   like `build(gradle): upgrade gradle`.
   
   3. Remember to include a reference to the GitHub issue number in each commit to make it easier for 
   future contributors to understand each code change. E.g. `closes #57`.
   
   4. Keep each commit small so that diffs are easy to read and understand for people looking at your 
   code in the future. A pull request should always be focused to doing one thing, for example fixing 
   a bug or adding a new feature, but not a mixture. Avoid large commits and pull requests which 
   attempt to do too much at once, as this makes code review difficult.
   
   5. If you want to add things like formatting fixes or refactoring, etc, do _not_ mix those with 
   the actual code change related to an issue. To make the actual code change easier to read, separate 
   refactoring into a new branch (and a new issue).
   
   6. Once you are ready to receive feedback on your branch, create a _pull request_ for merging it 
   into the `main` branch. Include a reference to the GitHub issue in the pull request's description,
   e.g. `closes #57`, so that the issue gets closed automatically when the pull request merges.

   7. Every pull request requires at least one approved peer review before being merged, so add at 
   least one person as a _code reviewer_ of your pull request. To find out who to add, click 
   "Insights" → "Contributors" too see an overview of the most active contributors for each 
   repository. If you are unsure who to add, use these: [`nya-elimu`](https://github.com/nya-elimu), 
   [`jo-elimu`](https://github.com/jo-elimu) and [`gscdev`](https://github.com/gscdev).
   
   8. Once your pull request has been reviewed and approved, it can be merged. The person who created 
   the branch (you) will be the person responsible for merging the branch. So your peers reviewing 
   your code will not merge the branch; that is your responsibility.

<a name="workflow-example-webapp"></a>
## Workflow Example: [webapp](https://github.com/elimu-ai/webapp)

### Introduction

As an outside collaborator, you are free to fork the repository and create pull requests from your fork. 

However, as a member contributor who has been added to the [GitHub organization](https://github.com/elimu-ai), 
the work flow looks like this:

### Work Flow

1. Select a GitHub issue to work on. Either select an existing issue from https://github.com/elimu-ai/webapp/issues or create a new one, and assign yourself to the issue.

2. Create a new branch for the GitHub issue:

   ![](https://user-images.githubusercontent.com/1451036/32688430-d1b9fc88-c6d0-11e7-8e20-10a10c028d0a.png) .  ![](https://user-images.githubusercontent.com/1451036/32688437-12fc5f6a-c6d1-11e7-9a38-b34479356522.png)

3. Switch to the branch you created and implement your code changes on that branch.

4. Once ready for testing, create a pull request for your branch for merging it into the `main` branch. Your pull request needs at least one approved review in order to be merged. When assigning reviewers, add one or more of the project's 
[maintainers](https://github.com/elimu-ai/webapp/blob/main/.github/CODEOWNERS):

   * [`nya-elimu`](https://github.com/nya-elimu)
   * [`jo-elimu`](https://github.com/jo-elimu)
   * [`gscdev`](https://github.com/gscdev)
   
   If the maintainers are too slow to get back to you, reach out to the [open source community](README.md#open-source-community) via chat or e-mail.
   
5. Once your pull request has been approved by at least one project maintainer, press the "merge" button. This will merge your code changes into the `main` branch and deploy them to the test servers at https://`<language>`.test.elimu.ai.

6. If all of the regression tests pass, ask a maintainer to deploy the changes to the production servers at https://`<language>`.elimu.ai.


---

Get to know some of our past and current open-source contributors and maintainers in [CONTRIBUTORS.md](CONTRIBUTORS.md).

If any of the above steps are unclear, or you have any other questions or comments, please reach out to the [community](README.md#open-source-community) via chat or e-mail. Thank you for contributing 🙌🏽

---

<p align="center">
  <img src="https://github.com/elimu-ai/webapp/blob/main/src/main/webapp/static/img/logo-text-256x78.png" />
</p>
<p align="center">
  elimu.ai - Free open-source learning software for out-of-school children 🚀✨
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

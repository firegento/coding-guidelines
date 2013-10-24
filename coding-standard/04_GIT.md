Git & Github
============

This file describes how to use Git and Github with a FireGento module.

Github
------
A FireGento module is hosted on the Github servers under the [FireGento Account](https://github.com/firegento/).
For every module there should be at least one responsible person who takes care of the module (start releases, look through issues, comment on pull requests, ..).

Commit Messages
---------------
A FireGento commit message will be following the pattern:

[~,+,-<TOPIC>] message between 50 and max 80 characters. <fixes:, closes:> #GITHUB_ISSUE_ID

GitHub issue reference are optional elements, but approved to be usefull.

Some details:
* ~ means nothing important changed
* - means you removed something
* + means you added something
* Possible TOPICS: BUGFIX, TASK, FEATURE, API, CONFIGURATION
* Possible GitHub commit commands: fix #xxx,fixes #xxx, fixed #xxx,close #xxx,closes #xxx,closed #xxx,resolve #xxx,resolves #xxx,resolved #xxx
* To just reference an issue use: #xxx

Some examples:

* [~TASK] renamend method to camelCase closes: #123
* [~BUGFIX] memory leak fixed in some helper method fixes: #1234
* [+FEATURE] added new GUI dialog to ask the user for some input. closes: #1235
* [-FEATURE] removed old code.

A detailed description can be found at [Flow commit messages](http://docs.typo3.org/flow/TYPO3FlowDocumentation/stable/TheDefinitiveGuide/PartV/CodingGuideLines/PHP.html#commit-messages) page.

git-flow
--------
We highly recommend the "git-flow" branching model for a FireGento module. Nonetheless it must at least contain at least a `master` and a `develop` branch.

### Initialise git-flow
Please navigate to the location of the FireGento module in your Terminal/Shell and then type `git flow init`.

After following the initialisation you should have an output like this:

```
Which branch should be used for bringing forth production releases?
   - master
Branch name for production releases: [master]
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []
```


### Rules
Using this branching model has some basic rules:

* Commits directly to the `master` branch are not allowed.
* Only `hotfix` and `release` branches are allowed to merge in the `master` branch. Both branches must be merged afterwards in the `develop` branch.
* The `master` branch should always represent the latest release, e.g. for MagentoConnect.
* git-flow automatically creates an annotated tag after using `git flow release finish ..`. Please make sure that this tag is pushed to the Github server (You can do this with `git push --tags`).


### Information about git-flow
You can read more about git-flow here:

* [installation how-to](https://github.com/nvie/gitflow/wiki/Installation)
* [gitflow on Github](https://github.com/nvie/gitflow)
* [blog post about git-flow](http://nvie.com/posts/a-successful-git-branching-model/)

If you are not really a shell guy, we recommend the programm [SourceTree](http://www.sourcetreeapp.com/) for working with git and git-flow.

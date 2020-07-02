Contributions
=============

Contributions to our FireGento modules are highly appreciated!


FireGento Contribution Process
------------------------------

![FireGento Contribution Process](http://f.cl.ly/items/143Q021a2D0u3I3o0l1O/firegento-contribution-process.jpg)

Kudos at Magento for providing a very useful Visio file at [github.com/magento/bugathon_march_2013/wiki/DevProcess](https://github.com/magento/bugathon_march_2013/wiki/DevProcess).


### Step 1: Fork the repository

To fork an repository, click on the Button **Fork** on every Github repository page.

![Fork Repository](http://f.cl.ly/items/1B0e1u3D1M0s393c2z1r/22.10.13_22_39-Bildschirmkopie.jpeg)


### Step 2: Clone the repository

```shell
git clone git@github.com:YOUR_USERNAME/REPOSITORY_NAME.git
# Clones your fork of the repository into the current directory in terminal on your computer
```

### Step 3: Initialize git-flow
```shell
git flow init
# Initializes git-flow for your repository
```

Please make sure that the branch name for production releases is `master` and the branch name for development is `develop`!

### Step 4: Make changes and push code
If you would like to fix issues, please use issue number as feature branch name.

```shell
git flow feature start <name of your feature>
# code your changes
git add .
git commit -m""
# repeat the last three lines until you finished
git flow feature finish <name of your feature>
git push origin develop
```

### Step 5: Create a pull request on Github

This [article](https://help.github.com/articles/using-pull-requests) describes in a very good way how to create a pull request on the Github platform.

Please make sure that you ALWAYS create pull request for the `develop` branch. Pull requests to the `master` branch will be closed.

The only exception are `hotfix` branches which are fixing critical bugs on the existing release.


### Step 6: Review the pull request (Only for FireGento Team)

The lead developers of the module have to review the pull request by going through the single commits. If the pull request is acceptable, they merge the pull request in the code base of the FireGento module.

Additional acceptance criteria:
* If a FireGento module is configured on Travis please make sure that the pull request branch passes the build.
* The FireGento module code base should pass the PHP_CodeSniffer check. Coding Standard violations have to be fixed by the developer of the pull request or the person who merges the pull request.
* tbd...

### Step 7: Show :heart: to contributors (Maintainers only) 

We added [all-contributors-bot](https://allcontributors.org/) to our repositories, so you can use this bot to add contributors to our README.de

- Basic usage: Add comment to issue or PR: `@all-contributors please add @Someone for code, doc and infra`
- you can choose from [different contribution types](https://allcontributors.org/docs/en/emoji-key)
- The bot creates PR with updated README.md and .all-contributorsrc file


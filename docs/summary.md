# Overview

<img src="https://lh3.googleusercontent.com/pw/ACtC-3dFE2kzBNDAjAIS-D6W4Eg0LeEmaADST58bf9X2728m2RYNSvaBEl8n00i2ZrXrhnx3tuEU0mI2fSmAyJavigX3RpTTHy8izjOIp23_xDLT-ZATtVvebHu8KvGGG7UEBFuwqE8jcQuiqIGYrtfW-j2GnQ=w999-h562-no?authuser=0" width=600>

This doc assumes you have downloaded the [SMK CLI](https://github.com/bcgov/smk-cli), 
 and have used it to author an SMK Based application.  The next question
you may have is how can I share this application.

There are a lot of different ways this could be accomplished including:
1. Using [Github pages](https://guides.github.com/features/pages/) to host / publish your application
1. Host on an existing Web Server your organization may have
1. Have DataBC Host your application in openshift.

This document is focused on the last option, host / publish using openshift.

# Overview

In order to deploy a new SMK application to openshift  you will need to complete
the following steps.

1. Published code to github
1. Add build / deploy files to your repository
1. Add Secrets to your repository

Once these requirements have been met, any pull request to the master/main branch 
will trigger the actions, which at a high level will:

1. Build a new docker image and store it in the packages associated with the repository.
1. Deploy the image to a dev openshift namespace
1. Comment on the github issue associated with the pull request, include the dev url

If the pull request is merged with the master branch that will trigger a prod deployment.

# Setting up Build / Deploy to Openshift

1. [Get your code into github](./githubRepoRequirements.md)
1. [Add the build / deployment code to your repo](./addBuildDeployFiles.md)
1. [Add Secrets to your repository](./.addSecrets.md)

# Administrative Documentation

Administrative docs include info on:
* creating a github personal access token
* how to init a net new openshift namespace

* [Administrative Documentation](./administration_guide.md)

# List of SMK related Github Repositories

* [SMK Command line](https://github.com/bcgov/smk-cli)
* [SMK Javascript library](https://github.com/bcgov/smk)
* [SMK Github Actions](https://github.com/bcgov/smk-actions)
* [SMK Helm Charts](https://github.com/bcgov/smk-helms)


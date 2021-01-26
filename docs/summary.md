# Overview

This doc assumes you have downloaded the [SMK CLI](https://github.com/bcgov/smk-cli), 
got it working and have used it to author a SMK Based application.  The next question
you may have is how can I share this application.

There are a lot of different ways this could be accomplished including:
1. Using [Github pages](https://guides.github.com/features/pages/) to host / publish your application
1. Host on an existing Web Server your organization may have
1. Have DataBC Host your application in openshift.

This document is focused on the last option.

# Overview

The following steps are required in order to publish an net new application.
Each step is described in more detail in the links

1. Code has been published to github repository
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








# Configure SMK based app for Deployment

To deploy an app to the openshift namespace the following steps need to be taken

1. populate the github repository with the following secrets:

    * GHCR_TOKEN : The personal access key that is used to pull the image from github packages to openshift (Github needs credentials to access images)
    * GHCR_USER : The username that is associated with the token
    * OPENSHIFT_SERVER_URL: The url to the openshift instance
    * OPENSHIFT_TOKEN_DEV: The api key for the service account created in openshift.  This is the token that allows github actions to communicate with openshift

1. Copy the contents of the folder (HERE) to .github/workflows in your project

1. Either create your own docker file or copy the dockerfile defined (HERE).

# Test 

To test, merge the changes you made above to the master branch, then make a trivial 
change, (edit readme or something), commit, and push to dev branch, then issue a pull
request, wait for it to complete, test the url that gets put in the issues, and finally
if it looks good deploy.



# MOVE THIS TO THE ACTIONS FOLDER

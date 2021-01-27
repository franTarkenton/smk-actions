# Adding Secrets

[Previous steps have copied github actions into your repository](./addBuildDeployFiles.md). Those actions
are configured to fire on Pull requests to either the 'main' or the 'master'
branches of the repository.

Actions are configured to do nothing unless all the secrets they require to 
communicate with github and openshift exist.

This is the step where we define those secrets, in essence arming
our deployment.

# Details

So go to github and navigate the repository that you want to deploy.
Before you do anything review this checklist:

1. The repository is owned by bcgov
1. DataBC staff are the administrators of the repository.  This is 
   important because we do not want to share the secrets we are putting 
   into the repository with anyone but DBC staff

# Populate Secrets

So to reiterate navigate to the repo in github, click on the repository
settings.  

<img src="./repo_settings.png" width="500">

Once in settings click on secrets

<img src="./repo_secrets.png" width="300">

Now at the top right there is button called "New Repository Secret", find it and click on it.

<img src="./add_new_secret.png" width="200">


# Secrets to Add

Now add the following secret definitions:

| Secret name | Description |
| ----------- | ------------ | 
| GHCR_TOKEN | this the token for your github service account |
| GHCR_USER | The username that is associated with the github service account |
| OPENSHIFT_SERVER_URL | The url to openshift, this is the same url that is passed when you login to openshift on the command line |
| OPENSHIFT_TOKEN_DEV | The api key for for the service account that is configured in the dev namespace | 
| OPENSHIFT_TOKEN_PROD | The api key for the service account that is configured in the prod namespace |

After these secrets have been populated you can test your flow by triggering the 
build deploy with a pull request to the master branch.



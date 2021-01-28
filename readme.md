# Simple Map Kit Github Actions

<img src="https://lh3.googleusercontent.com/pw/ACtC-3cDXfdy-1qrVv-laLoK-g33LyILuSlKP1p5kE4FgOzwzRBRqeKo3l0bBjNHR_cLv7ZGXMCX1zpNk6L8PGOFuDZPSsLkC-uhgyRNi18yDt3bVUdGUWxOl4qT4wrdsxbIU2KnwNkbPs-_MrWi4cIXZLQjkQ=w1186-h668-no?authuser=0" width="550">

Simple Map Kit (smk) is a javascript library and a CLI tool that facilitate
the construction of web maps.  The following links provide more information 
about SMK.  If you are brand new to creating web maps the
[smk command line tool]((https://github.com/bcgov/smk-cli))
(cli) is a great place to start.

* [SMK command line tool (CLI)](https://github.com/bcgov/smk-cli)
* [SMK javascript library](https://github.com/bcgov/smk)
* [SMK Helm Charts](https://github.com/bcgov/smk-helms)

## SMK Github actions

The objective for SMK is to make it as easy as possible for relatively non
technical people to be able to construct a web map, and at the same time
introduce those users to common patterns used when creating and deploying
a web application.

Part of that process is to make it as easy as possible to deploy smk based 
apps to openshift.  Build and deployment steps are taken care of by github
actions.  We wanted to be able to update / fix github actions that perform 
these steps without having to edit individual repositories.  In order to 
accomplish this github composite actions have been created and are located
in this repository.

## Deploy an SMK based app to Openshift

[User Guide to Deploy SMK to Openshift](./docs/summary.md)


# Next Steps

* could possibly save time by creating organization wide secrets, then would only grant access to them, instead of having to copy them all into the repo
* add and 'env' tag to the pr issue comments so you can distinguish between dev oc deploy and prod urls.  That said prod / dev are in the urls themselves.
* restrict the actions that can be run in the repo


# Simple Map Kit Github Actions

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




# Publishing to Github

This guide goes over very briefly how to go about publishing your SMK based app
to github.

# Details

If you do not already have a .gitignore file in the root directory of your application 
Create one now.  Either way be sure that the file includes the following entries:

```
node_modules
.env*
```

The pattern that we are promoting is a one to one relationship between github repositories 
and smk based applications.  If you follow this pattern you should be able to re-use the
deployment pipelines unaltered.  Deviation from this pattern will require you to edit
the github actions and possibly other aspects of build / deployment process.

# Repository Structure

Any SMK based application should have the following directory structure:

|  name | file / directory      | description |
| ------------------  | -----     | ----------  |
| assets              | directory | png files and style.css file |
| layers              | directory | possible embedded spatial data |
| package.json        | file      | created by smk cli |
| smk-config.json     | file      | created by smk cli |
| LICENSE             | file      | use apache, can copy from [here](../smk-publish-app/LICENSE) |
| code_of_conduct.md  | file      | copy from [here](../smk-publish-app/code_of_conduct.md) |
| index.html          | file      | created by smk cli |
| package-lock.json   | file      | create by smk cli  |
| readme.md           | file      | a description of your app |
| smk-init.js         | file      | created by smk cli |
| .gitignore          | file      | describes files to omit from github |

# Publish to Github

Once your code reflects the structure described above you are in a position 
to publish to github.

This guide should hopefully be adequate to get you started:

https://github.com/bcgov/BC-Policy-Framework-For-GitHub/blob/master/BC-Gov-Org-HowTo/Cheatsheet.md

In a nutshell:
1. Create a repository in github
1. Clone the repository
1. Add your smk files to the repo
1. stage/commit/push your changes to the remote

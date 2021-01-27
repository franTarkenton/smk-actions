# Add Build Deploy Files

<img src="https://lh3.googleusercontent.com/pw/ACtC-3d9oiZBEHAhC5itlp0r42IEk1qm2bAvIlnGCj7oBHOJOGt_rBaTn66XELEqb3T1fhLgZe7Shsjkv0Zt-zvzJ42gb_zJYqr-eiIvz_Fwo3-_GdXP_ETGGfJPybWmFO8yuNQrltOOvPy3j4Je68CLx0HDew=w999-h562-no?authuser=0" width="500">

## Overview

In order to enable automated build / deployment of your SMK application you will
need to add some files to your repository.

All the files that need to be added exist in this repository in 
the directory **smk-publish-app**. 
(https://github.com/bcgov/smk-actions/tree/main/smk-publish-app)



# Details

To add the required files to your repository basically copy everything 
from the directory **smk-publish-app** in this repository, to your smk
app repository.

After this is complete your repository should look similar to this:

```
drwxr-xr-x 8 kjnether kjnether  4096 Jan 25 19:22 .git
drwxr-xr-x 3 kjnether kjnether  4096 Jan 22 11:51 .github
-rw-r--r-- 1 kjnether kjnether   160 Jan 25 17:54 .gitignore
drwxr-xr-x 2 kjnether kjnether  4096 Jan 22 11:49 .vscode
-rw-r--r-- 1 kjnether kjnether  1132 Jan 22 11:49 Dockerfile
-rw-r--r-- 1 kjnether kjnether 11324 Jan 22 11:49 LICENSE
drwxr-xr-x 2 kjnether kjnether  4096 Jan 22 11:49 assets
-rw-r--r-- 1 kjnether kjnether  2400 Jan 22 11:49 code_of_conduct.md
-rw-r--r-- 1 kjnether kjnether  1876 Jan 22 11:49 index.html
drwxr-xr-x 2 kjnether kjnether  4096 Jan 22 11:49 layers
-rw-r--r-- 1 kjnether kjnether   849 Jan 25 16:07 package-lock.json
-rw-r--r-- 1 kjnether kjnether   247 Jan 25 16:07 package.json
-rw-r--r-- 1 kjnether kjnether   111 Jan 22 11:49 readme.md
-rw-r--r-- 1 kjnether kjnether 78109 Jan 22 11:49 smk-config.json
-rw-r--r-- 1 kjnether kjnether   146 Jan 22 11:49 smk-init.js
```

**Files copied:**
* .github/workflows/build-deploy-dev.yaml
* .github/workflows/deploy_prod.yaml
* Dockerfile
* LICENSE
* code_of_conduct.md


<br>

***[Back to summary](./summary.md)***

***[Next steps...  ...add Repository Secrets](./addSecrets.md)***

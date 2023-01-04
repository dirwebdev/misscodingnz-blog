# commands used

## Create 2 github repositories

1. misscodingnz-blog

    - will hold the blog configuration and blog files
    - basic settings
        - Public or Private
        - didnt use readme


2. misscodingnz-blog.github.io

    - will be for github pages, will hold all the static content
    - need to set up github.io pages
        1. click on repository settings
        2. click on pages on the left menu
        3. select source under build and deployment
            - either select:
                - github actions (Beta)
                - Deploy from a branch
                - (I used Deploy from a branch)
        4. select the branch and folder to use to use
            - I used:
                - main branch
                - root folder
        5. add custom domain if needed,(I did not use domain in this example)
        6. select whether or not you want https enforced
        7. **MAKE SURE SETTINGS ARE SAVED AS YOU GO**
        8. After few minutes you will see a link where the site will be live
            - The live link for this example:
                - https://dirwebdev.github.io/misscodingnz-blog.github.io/


1. Create new site

```bash
hugo new site misscodingnz-blog
```
2. Initiliaze a git repository

```bash
git init
```
3. Add files to staging
4. Commit the staged files to the repository
5. Add remote origin

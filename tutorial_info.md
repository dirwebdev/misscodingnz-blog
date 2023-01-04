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
    ```bash
    git add .
    ```

4. Commit the staged files to the repository
    - committed initial files
    ```bash
    git commit -m "new hugo site, with tutorial commands"
    ```

5. Make sure you are on Main branch, add remote origin and push repository to github
    - make sure you are on the main branch
        ```bash
        git branch -M main
        ```
    - add remote origin
        ```bash
        git remote add origin https://github.com/dirwebdev/misscodingnz-blog.git
        ```
    - push repository to github
        ```bash
        git push -U origin main
        ```
6. Create .git ignore
    - site used to create .gitignore
        - https://www.toptal.com/developers/gitignore
            - added flags:
                - VisualStudioCode
                - Hugo
                - macOS
    - add node_modules to .gitignore
        - in this tutorial node_modules/* to this section...
        ```bash
        # Icon must end with two \r
        Icon
        node_modules/*
        ```
    - add .gitignore to repository
        - (make sure you are in site root directory in terminal)
         ```bash
         touch .gitignore
         ```
        - copy and paste generated .gitignore text into new .gitignore file and save.
    - commit new .gitignore to repository.
        ```bash
        git add .
        git commit -m "added .gitignore updated tutorial_info"
        ```
7. Add hugo theme:
    - Link for hugo themes
        - https://themes.gohugo.io/
    - Theme used in tutorial
        - https://themes.gohugo.io/themes/blist-hugo-theme/
    - Add theme submodule to site:
        ```bash
        git submodule add https://github.com/apvarun/blist-hugo-theme.git themes/blist
        ```
    - install necessary modules
        - postcss-cli
            - to use PostCss with Hugo build
                ```bash
                npm i -g postcss-cli
                ```  
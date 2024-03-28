# Caramba.clinic Web Source Repository


The Static ([Hugo](https://gohugo.io)) website for [caramba.clinic](https://caramba.clinic).

## Local development
```bash
hugo server
``` 

## Automated publishing

When making changes please follow these steps:

 1. Clone this repo
 
    ```bash
    git clone git@github.com:caramba-uu/website.git
    ```
    or if you already have a clone of this repo
    ```bash
    git checkout master
    git pull
    ```
 2. Create a new branch with your name and what you are changing `name/topic-of-change`
 
    ```bash
    git checkout -b name/update-my-profile
    ```
 3. Make your edits
    Add and edit the MD file in "content/people"
    Add a profile picture in "static/img/people"
 4. Push your edits to a new branch *in this repo* (Important! otherwise it will not work)
 
    ```bash
    git add .
    git commit -m "profile update"
    git push -u origin name/update-my-profile
    ```
 5. Create a Pull Request (PR) on GitHub and select `base:master <- compare:name/update-my-profile`
 6. Check that the PR build status is passed (green)
    If not, go to step 3 and repeat
 7. Ask for it to be merged
 8. Done!

Note that you are supposed to work with this repository only. Don't fork the repo.

## Notes

Github Actions is used to generate the HTML pages by HUGO from this web template, and Github Actions pushes the HTML to the branch gh_pages. The HTML pages in branch gh_pages are served by Github on the domain caramba.clinic (configured in the settings of this repo)

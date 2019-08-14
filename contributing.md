# How to Contribute

We use the [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) workflow to make our lives easier. This means all new lessons, practices, and edits should be made in separate branches -- not the `master` branch.

If you have questions or run into problems at any point, contact [Kelly](mailto:sovacool@umich.edu).

## Setup

If you haven't already:

1. Configure git on your local machine

    Use the same email that is associated with your GitHub account.
    ```
    git config --global user.name "Firstname Lastname"
    git config --global user.email "you@email.com"
    ```

1. Clone this repo
    ```
    git clone https://github.com/GWC-DCMB/ClubCurriculum
    ```

If you need a refresher, Software Carpentry has a lesson on [Version Control with Git](http://swcarpentry.github.io/git-novice/).

## Creating or editing

1. Create a new branch for your feature
    
    Be sure to give it a short, descriptive name.
    ```
    git checkout -b new-branch-name
    ```

1. Make your edits
    ```
    jupyter lab notebook-name.ipynb
    ```
    Be sure to save them from jupyter!
    If you're creating a new lesson or practice, it's easiest to edit the lesson key, then copy the key to the lesson folder and remove any blanks that you want to be filled in during the live coding demo.

1. Commit & push your changes
    ```
    git add notebook-name.ipynb
    git commit -m "Edit lesson XX"
    ```
    (Take a look at this [style guide](https://chris.beams.io/posts/git-commit/) for writing good commit messages.)
    
    If you're pushing your branch for the first time, you'll have to set the upstream:
    ```
    git push --set-upstream origin new-branch-name
    ```

    Otherwise, just push like usual:
    ```
    git push origin new-branch-name
    ```

1. Open a pull request
    1. Open the [repo page in your web browser](https://github.com/GWC-DCMB/ClubCurriculum) and click `new pull request`.
    1. Select your branch name to compare to master.
    1. Create the pull request.
    1. Assign a reviewer.
    The reviewer will then take a look at the changes, make any edits as needed, and merge the branch into master

## Reviewing

1. Make sure your local copy of the repo is up-to-date
    ```
    git pull
    ```
1. Checkout the branch corresponding to the pull request you're reviewing
    ```
    git checkout branch-name
    ```
1. Review and edit the contents
    ```
    jupyter lab notebook-name.ipynb
    ```
1. Commit & push changes if needed
    ```
    git add notebook-name.ipynb
    git commit -m "Revise lesson XX"
    git push
    ```

1. Merge the pull request when you're happy with it

    Either press the `merge` button on Github in your web browser,
    or do it from the command line:
    ```
    git checkout master
    git merge branch-name master
    ```
    In the merge commit message, be sure to reference any issues that the pull request resolves (e.g. `Resolves #10`) so the issue is closed automatically.
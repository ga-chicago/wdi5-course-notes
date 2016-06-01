# Submitting Homework

> A guide to submitting homework

We use GitHub to submit homework. You'll be creating "pull requests" from our official GitHub repository. This will allow us to pull in your work and merge it with ours for review. Do not try to follow these instructions until we've covered our lessons on Git and GitHub.

## How to Submit Homework

The rest of this guide will walk you through how to submit homework. See also: the diagram on this page.

### 1. Fork The Homework Repo

First, [fork the original repository found here](https://github.com/ga-chicago/wdi5-homework). Once on the page, click the "Fork" button that appears just below the main navigation bar.

Once you've done this you'll have your own personal copy (AKA "Fork") of the homework repository.

### 2. Clone your fork

You should now clone your new fork. After you clicked on the "Fork" button you'll be taken to the copy of the homework repository that lives in your GitHub account. To clone your fork, run the following in a terminal window:

1. Locate the green "Clone or Download" button on your forked repository's page and click it.
2. A small popup/modal window will appear. Be sure to click the "Use SSH" link that appears
3. Copy the URL that appears in the text box on this small modal popup
4. In your terminal, run this command: `cd Sites && git clone <PASTE THE URL YOU COPIED IN STEP 3 HERE>`
5. You'll now need to enter the directory by running `cd wdi5-homework`
6. You need to keep track of changes that we make to our upstream repo. To do this, run `git remote add upstream git@github.com:ga-chicago/wdi5-homework.git`. This will add a remote to your repository so you can pull down changes we make to the original repository.

You now have successfully copied the repository to your own account, cloned it, and entered the directory in your Terminal window. With that taken care of, you'll need to start submitting homework.

## How each assignment works

The homework repository will be updated week by week, assignment by assignment. For each week of the course there will be a `weekX` folder. Within each week's folder there will be an assignment folder numbered and named after the homework assignment given.

To submit your homework you should enter the proper week and assignment folder and create a folder named after yourself. So, for example, if I wanted to set up a folder to submit my week 1 homework I would run the following commands in a new terminal window after I had cloned down my fork:

```
# Enter the homework assignment's folder within the homework repo
cd ~/Sites/wdi5-homework/week1/01_star_wars_cli

# Make a folder to submit my work
mkdir my_firstname_my_lastname

# Enter into my new folder
cd my_firstname_my_lastname

# Now I would do the assignment...
```

### 3. Submitting completed assignments

To submit your assignment you just need to go through the normal Git add, commit, and push flow. This will upload the file to your fork of the original homework repository. In step 4 you'll submit a "Pull Request" which will allow us to see the homework you've completed.

### 3a. Retrieving new assignments

When we add new assignments and/or new weeks you'll need to download the changes to the repository. To do this you must run the following command from within the Git repository for homework.

```
# This will download changes from *our* (original) version of the homework repo
git pull upstream master
```

### 4. Submit your homework

At this point you've got a copy of the homework repository, you know how to pull down updates and new assignments, and you know how to push up your homework to your own repository. Now it's time to make a "Pull Request" so that we can merge those changes into our repository and view your assignments for grading.

1. Visit your copy (fork) or the `wdi5-homework` repository on GitHub. Again, go to __*your*__ copy on GitHub, do not go to ours.
2. Press the little green (sometimes it's just plain gray) "New Pull Request" button
3. You'll be taken to a page where you can enter a title and description of your changes. In the title, be sure to add the name of the assignment. In the description field tell us about any issues or questions you have. This is your chance to let us know what you need additional help with. We use this information to make sure we cover the topics that you want additional help with.

The GitHub documentation explains this process as well. [See the official pull request docs](https://help.github.com/articles/using-pull-requests/#initiating-the-pull-request) for more information on how to create a new pull request

## Grading and Feedback

Once you've completed these steps we'll get a notification that you want to merge your changes with our repository. We'll review your code and provide feedback in the form of comments on your code which you'll receive as email notifications and/or GitHub notifications.

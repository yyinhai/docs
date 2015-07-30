---
deprecated: false
author:
  name: Linode
  email: docs@linode.com
description: 'The Linode Library GitHub guide.'
keywords: 'GitHub guide, write for us, linode library, article submissions'
license: '[CC BY-ND 3.0](http://creativecommons.org/licenses/by-nd/3.0/us/)'
modified: Tuesday, July 28th, 2015
modified_by:
  name: James Stewart
published: 'Tuesday, July 28th, 2015'
title: GitHub Beginners Guide
---

As part of our open-sourcing of our documentation library, we've moved to Github for management of our guides.  This tutorial will walk you through submitting a new guide on our public GitHub

#Before You Begin

This guide assumes that you've signed up for a [Github Account](https://www.github.com), and that you've followed the sections for installing and configuring Git on your local machine contained within our [Git Source Control Management](https://www.linode.com/docs/applications/development/git-source-control-management) guide.

#Submitting new guides or changes with Git

##Placing your SSH key on Github

1.  If you have not done so already, generate an SSH key on your local system

		ssh-keygen

2.  View the contents of the newly created public key file.

		cat ~/.ssh/id_rsa.pub

3.  In a browser window, select your user account icon in the upper right hand corner of the screen, then click Settings.

	[![Github Settings](/docs/assets/github-settings.png)](/docs/assets/github-settings.png)

4.  Select the 'SSH keys' option from the Personal Settings menu, and then click the 'Add SSH key' button.

	[![SSH key settings](/docs/assets/github-ssh-key.png)](/docs/assets/github-ssh-key.png)

5.  Copy the contents of your public key file from your terminal window, and paste them into the 'Key' text box.  Add a descriptive title for your key in the 'Title' text box.

	[![Add Key](/docs/assets/github-load-key.png)](/docs/assets/github-load-key.png)


##Setting up your repository

In order to edit or create documents for the Linode library, you will need to fork your own version of the Linode Docs repository on Github

1.  Navigate to the [Linode Docs](www.github.com/linode/docs) GitHub repository.

	[![Linode Docs Github Repo](/docs/assets/github-your-repository.png)](/docs/assets/github-your-repository.png)

2.  Click 'Fork' in the uppper right hand corner of your screen to create your own version of the repository

3.  Once the fork process has completed, visit the 'docs' repository under your repository list on the Github homepage.

	[![Your repository on Github](/docs/assets/github-your-repository.png)](/docs/assets/github-your-repository.png)

4.  Clone your forked branch to your local machine by copying the clone URL, and appending it to the following command.  We recommend cloning via SSH for this particular step.  This command will create a local copy of your cloned repository that you can work with directly, in the directory where the command is being run.

	[![Github Clone URL](/docs/assets/github-clone-url.png)](/docs/assets/github-clone-url.png)

		git clone <insert clone URL>

##Creating your branch

Once you've cloned a local copy of your repository, you will need to make a branch to store your new guide in.  Branches allow you to work on multiple guide changes without creating a mess within your pull requests.

1.  Move to the cloned directory that was created in the previous step.

		cd docs

2.  Verify that you are in the master branch by running the following command.

		git status

	You should receive output similar to that show below

		On branch master
		Your branch is up-to-date with 'origin/master'.

		nothing to commit, working directory clean

3.  Check out a new branch with a descriptive title matching the guide that you are editing or creating.

		git checkout -b guide-title

4.  Rerun the 'git status' command to confirm that you have been moved to the new branch.  You should receive output maching the following.

		On branch guide-title
		nothing to commit, working directory clean

##Submitting your first pull request (PR)

##Commenting and editing your PR

##Managing multiple branches

#Reporting issues with existing guides
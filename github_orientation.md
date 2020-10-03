# Github Orientation
## Introduction to Github and Git

This is the introduction to Github for the Johns Hopkins Nanoenergy Lab. Github is a remote, cloud-based platform for the development and management of what is primarily code, but other files and data may also be stored here. All content is stored in a **repository**, which is essentially a folder which contains all the data and files in one project. Each repository may be public or private (for instance, this repository, [github.com/jhu-nanoenergy/documentation](https://www.github.com/jhu-nanoenergy/documentation) is public). Github is based on the **Git** Version Control System (VCS), which allows you to track incremental progress through a sequence of **commits**, each of which represents an update from the previous commit (whether you're adding lines, changing lines, or removing lines of code).

In practice, you'll be making several commits as you code, each containing some changes you make, and the frequency of which is up to you to decide. However, it is advised to commit your changes often, as you can revert to a previous commit if you break your code, or otherwise want to undo different changes. After a certain amount of commits, or whenever you wish to publish your code to the **remote** repository, you will **push** all the commits to the Github server, and it will then be accessible by all who have access to it. Only collaborators of the repository may have push access, and anybody can see the code in a public repository, but only collaborators may see the code in a private repository.

However, Git will not refresh the **local** copy of the remote repository that you **clone** to your computer when other people commit new changes to the remote repository. Therefore, you must manually **pull** changes from the remote repository to keep your version as up to date as possible.

In essence, Git is like a backup system for incremental development of your code.


## Using Github

The Git VCS was originally designed as a command line tool to use in the terminal, the Command-Line Interface shell (the Terminal app on macOS, Windows Powershell on Windows, or the Linux terminal on Linux). For people who do not write software often, it may be more intuitive to rely on the [Github Desktop app](https://desktop.github.com/) (available for macOS and Windows) & the Github website, unless they have experience with Unix commands and the Command Line Interface. This guide will be updated to include information about that, but until then, it will focus on the Graphical User Interface of Github Desktop.
<!-- This is a comment, and just a reminder to remove this part once you introduce the CLI commands
-->

First, decide whether you wish to use the group account, [github.com/jhu-nanoenergy](https://www.github.com/jhu-nanoenergy), or to [create your own](https://www.github.com). It is generally preferable to use your own Github account so you can keep track of who has done what for easy accountability, and to use Github easily with your non-lab-related projects (it is a pain to sign off and on again). Just make sure to add your own account as a collaborator on the repositories you wish to work on and contribute to. To do so, click on the repository on the Github website, select the **Settings** tab as follows, select **Manage access** in the menu on the left, and select **Invite a collaborator** to add your personal account. Don't forget to accept the invitation in your email.

![View of the repository jhu-nanoenergy/documentation on github.com](/figures/repo_view.png)

Next, download the [Github Desktop app](https://desktop.github.com) and sign into your account. You will see something like the following, except you likely will not have repositories showing on the left-hand tab. To download a copy of an existing remote repository to your local computer, select **Clone Repository**.

![View of the Github Desktop app](/figures/github_desktop_clone.png)

Next, select which repository you wish to clone, and choose a local path on your computer where you want the repository to be located.

![View of the clone popup on the Desktop app](/figures/github_desktop_clone2.png)

After cloning, you will see that the repository is selected, and any changes to the contents therein will be reflected (it should be a blank list immediately after cloning, however). Once you create changes, they will reflect here - for instance, green text means you added lines since the last commit, and red means that line was removed since the last commit. For the files, a green square represents a newly added file, a yellow square represents a file with changes since the last commit, and a red square represents a file which was removed.

![View of the repository](/figures/github_desktop_deltas.png)

Also note the **Fetch origin** button in the top bar, which checks if the remote server has any changes that your local computer doesn't reflect. You should click this before you start making changes. If there are changes, it will show you the option to **Pull origin**, to pull the changes from the remote repository, alongside the number of new commits available (in this case 1).

![View of the Pull origin option](/figures/github_desktop_pull_origin.png)

Sometimes, there may be issues when pulling from the remote repository, if other changes conflict with changes you made. For example, if the remote commit changed line 1, but you also changed line 1 locally without having committed it, you will run into a merge conflict. You will get a popup that instructs you to stash your local changes and conform to the remote repository.

![View of the popup to stash your changes](/figures/github_desktop_stash.png)

Try to avoid this by coordinating with collaborators on what you will each be working on, and in particular which lines you may be Stash your changes, 

To change the repository, select the **Current Repository** dropdown and select the other one. Only then can you pull/push.

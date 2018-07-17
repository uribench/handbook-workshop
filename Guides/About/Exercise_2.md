# Exercise 2 - Preparing a Local Handbook Repository for the Workshop

***Duration: 10 min***

A *minimalist version* of the [software-engineering-handbook][1] GitHub repository was created for 
this hands-on workshop and is available on GitHub as [handbook-workshop][2] repository.

In this exercise we will create a local clone of the remote handbook-workshop repository on GitHub,
and then we will create a working branch from the local clone.

We will use [Git][3] locally, and also connect to a remote repository on [GitHub][4]. The deployed 
Linux development environment for this workshop has already been set and configured for using Git 
and GitHub for all the needs of this workshop.

During this workshop, all the participants will share the same **GitHub account** with the following 
credentials:

- Username: `handbookworkshop`
- Password: *(will be provided in the workshop)*
- Email: `handbookworkshop@gmail.com`

Perform the following steps in order to get familiar with the handbook-workshop repository and to
prepare it for the next exercises of this workshop:


## Step 1: Verify Prerequisites

Make sure you have completed [Exercise 1][5] and your current directory is the one you have created 
for yourself as instructed.


## Step 2: Visit the handbook-workshop Repository on GitHub

Use a new tab of your Chrome Browser to visit the [handbook-workshop][2] repository on 
GitHub and sign-in using the credentials of the shared `handbookworkshop` account.

Troubleshooting: If GitHub is under heavy load you may not be able to access it. You can check if it
is down for everyone or just you using the [isup.me][6] service.


## Step 3: Copy the GitHub Link for Cloning

Copy the GitHub link for cloning the repository using SSH protocol. To do that, make sure you are on
the 'Code' page of the repository on GitHub:

!['Code' page][8]

and click on the !['Clone or download' button][7] button on the right side of the page.

The copied link should be: `git@github.com:uribench/handbook-workshop.git`


## Step 4: Clone the handbook-workshop Repository

Clone the handbook-workshop repository using the following command locally from your
personal working directory on the Linux deployment for the workshop:

```bash
$ git clone git@github.com:uribench/handbook-workshop.git
```

Note: You can paste into the Linux bash terminal using the common `Ctrl-v` key combination. To copy
from the Linux bash terminal, just highlight the text you would like to copy and it will be copied
into the clipboard (as a queue for a successful copy, a scissors icon will be displayed for a short 
time in the center of the window).

This command will clone the remote repository into a newly created directory called:
`handbook-workshop`.
 
It also creates remote-tracking of branches, for each branch that you will create locally in the 
cloned repository (more on that in the next steps).

Note: We use in this workshop 'git clone' and not 'GitHub fork' because we are using a shared GitHub
account. Outside of the workshop you will use your personal GitHub account if you wish to contribute
to the handbook. In that case you will fork the repository to create a clone on your GitHub account, 
and only then clone the forked repository into your local machine.


## Step 5: Enter the Directory of the Cloned Repository

Change directory into the directory of the cloned repository: `$ cd handbook-workshop`


## Step 6: Create a Development Branch

Create a local branch for use during this workshop. 

The following annotated commands will get you familiar with some basic Git usage. Execute them all
in order to complete this step.

List the current local branches: `$ git branch`

Output:

```bash
* master
```

'master' is the only available branch currently. The current branch is highlighted with an asterisk.

Create a new branch: `$ git checkout -b <new-branch>`

Fot this workshop, it will help later if you pick a unique name for the branch. You can use the same 
name that you chose for your personal directory that you have created during Exercise 1.

This command will create a new branch and set it as the current branch. 

This can be verified by listing the current local branches using again: `$ git branch`

Output: 

```bash
  master
* <new-branch>
```


Now we are ready to proceed and make changes to the local repository, push them to the remote 
repository on GitHub, and create a pull request to propose our changes. All these steps will be 
explained in the next exercise.

---

[1]: https://github.com/uribench/software-engineering-handbook
[2]: https://github.com/uribench/handbook-workshop
[3]: http://software-engineering-handbook.com/Handbook/Development/Code%20Development%20Lifecycle/Version%20Control/Git/
[4]: http://software-engineering-handbook.com/Guides/Git/Working%20with%20a%20Remote%20Git%20Repository
[5]: /Guides/About/Exercise_1
[6]: https://downforeveryoneorjustme.com/github.com
[7]: /images/exercise-2/github-clone-or-download-button.png
[8]: /images/exercise-2/github-code-page.png
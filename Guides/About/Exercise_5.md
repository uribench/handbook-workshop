# Exercise 5 - Creating a Pull Request and Reviewing the Changes

***Duration: 10 min***

In the previous exercises we have created new content and connected it to the handbook navigation 
tree. Now we are ready to proceed and push the changes to the remote repository on GitHub, and 
create a pull request to propose our changes.

Perform the following steps in order to push the changes to the remote repository on GitHub, 
create a pull request, review the changes, merge them with the main branch, and delete the redundant 
branch:


## Step 1: Verify that all Changes are Committed

Make sure that all the changes you have made in the previous exercises are committed to the 
development branch using: `$git status`

If needed, commit the changes using the following commands:

```bash
$ git add . --all
$ git commit -m <commit-message>
```

## Step 2: Push the Changes to GitHub

Push the changes to the GitHub repository that we have cloned on Exercise 2.

Note that the current branch `<dev-branch-name>` has no upstream branch.
To push the current branch and set the remote as upstream, use:

```bash
git push --set-upstream origin <dev-branch-name>
```

## Step 3: Create Pull Request

Visit the [handbook-workshop][1] repository on GitHub. We have done that on an earlier exercise, 
so you are supposed to have an open tab on your Chrome browser that is already there. If not, then 
repeat [Exercise 2: Step 2][2].

Refresh the 'Code' page of the repository on GitHub:

!['Code' page][3]

and click on the !['Compare & pull request' button][4] button on the right side of the page.

You will be taken to the 'Open a pull request' page where you can see the changes highlighted at the 
bottom of the page if you scroll down.

Click on the !['Create pull request' button][5] button on the higher part of the page.


## Step 4: Wait for Completion of Integrated Checks

A special Linux deployment with an instant Markdown preview server, called 'madness' was integrated 
with this repository. It is triggered when a pull request is created.

Watch the progress of the integrated checks status. At first you will see something similar to the 
following status message in gold color:

![Deployment/now pending status][6]

Wait until the checks complete and the status message turns green as follows:

![All checks have passed status][7]


## Step 5: Review the Changes using a Preview Server

Click the `Show all checks` link next to the 'All checks have passed' status message:

![Show all checks link][8]

The next detail will be unfolded to show the message 'deployment/now — Deployment has completed'.
Click on the 'Details' link to its right:

![Check details link][9]

You will be transferred to the Linux deployment with an instant Markdown preview server. It will
look something like:

![madness preview][10]

Review the handbook with the changes that you have made. When you finish reviewing, move back to the 
GitHub repository.


## Step 6: Merge Pull Request

Refresh the 'Code' page of the repository on GitHub and click on the 
![Merge pull request button][11] button to start merging the pull request.

Now confirm the merge by pressing the ![Confirm merge button][12] button.


## Step 7: Delete the Redundant Branch on GitHub

We have approved and closed the pull request successfully. Consequently, the changes were merged 
into the 'master' branch and we can delete the redundant branch on GitHub.

Click on the ![Delete branch button][13] button next to the 'Pull request successfully merged and 
closed' message.


## Step 8: Visit the Workshop Site

Now we are able to see the handbook with the approve changes on the [workshop site][14].
It will look something like:

![workshop site][15]


We have completed all the steps needed to introduce new content up to airing the resulting handbook. 
It is time now to clean up the local repository. This will be done in the next exercise.

---

[1]: https://github.com/uribench/handbook-workshop
[2]: /Guides/About/Exercise_2#step-2-visit-the-handbook-workshop-repository-on-github
[3]: /images/exercise-2/github-code-page.png
[4]: /images/exercise-5/github-compare-and-pull-request-button.png
[5]: /images/exercise-5/github-create-pull-request-button.png
[6]: /images/exercise-5/github-pending-check-deployment-now-status.png
[7]: /images/exercise-5/github-all-checks-have-passed-status.png
[8]: /images/exercise-5/github-show-all-checks-link.png
[9]: /images/exercise-5/github-check-details-link.png
[10]: /images/exercise-5/madness-handbook-workshop-preview.png
[11]: /images/exercise-5/github-merge-pull-request-button.png
[12]: /images/exercise-5/github-confirm-merge-button.png
[13]: /images/exercise-5/github-delete-branch-button.png
[14]: http://workshop.software-engineering-handbook.com/
[15]: /images/exercise-5/workshop-site.png
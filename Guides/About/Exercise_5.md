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



---

[1]: https://github.com/uribench/handbook-workshop
[2]: /Guides/About/Exercise_2#step-2-visit-the-handbook-workshop-repository-on-github
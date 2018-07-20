# Exercise 6 - Cleaning the Local Repository

***Duration: 10 min***


In the previous exercises we performed all the steps needed to introduce new content, review it, and
air the modified handbook with the new content. It is time now to clean up the local repository.

Perform the following steps in order to clean up the local repository:


## Step 1: Verify that all Changes are Committed

Just as a precaution, make sure that all the changes you have made locally prior to the pull request
are committed to the development branch using: `$git status`

If this is not the case for some reason, then repeat all the steps of the previous exercise. 

Otherwise, continue with the next steps.


## Step 2: Clean Up the Local Repository

You can execute all the following commands in sequence and watch the intermediate output to see
the initial state, how the current branch is changing, and the final state:

```bash
git status
git branch
git checkout master
git branch
git pull --prune
git branch -d <dev-branch-name>
git branch
```

Alternatively, execute only the following minimal sequence of commands:

```bash
git checkout master
git pull --prune
git branch -d <dev-branch-name>
```


Congratulations!!! You have completed all the workshop exercises successfully and now you know how 
to contribute content to the [Software Engineering Handbook][1]. Your contributions are welcome!

---

[Previous Exercise](Exercise_5)

---

[1]: http://software-engineering-handbook.com/
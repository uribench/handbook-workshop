# Exercise 1 - Getting Familiar with the Workshop Development Environment

***Duration: 10 min***

For this hands-on workshop we will use a Cloud based deployment of Linux that was prepared 
especially for this workshop. Although, learning how this deployment was made is not part of this 
workshop, you may visit the [`handbook-workshop-docker-gotty`][1] GitHub repository for details.

Perform the following steps in order to get familiar with the workshop development environment:

**Step 1**: Visit the Linux bash terminal deployment using the following URL from a Chrome Browser:
[`https://handbook.now.sh/`][2]


**Step 2**: When asked, enter the passphrase for the SSH private key that will be provided in the
workshop.

If you decide to dismiss the request and start using the system immediately, you can always enter
the passphrase using the following command: `$ ssh-add`

After entering the passphrase or after dismissing the request, you will see a prompt similar to: 
`handbook app $ `

As indicated by the prompt, the default working directory upon entry is: `/app`


**Step 3**: The environment is shared by all participants of this workshop. Therefore, you are asked 
to create a directory with a unique name under `/app` and enter it using the following commands:

```bash
$ mkdir <unique-directory-name>
$ cd <unique-directory-name>
```

It is suggested to use your first or last name or a combination of the two as the 
`<unique-directory-name>`.


**Step 4**: For text editing we will use either `nano` or `vi` or in-browser Markdown editor.

If you have experience using any of these two text editors, skip the next sections if this step.

## nano

If you do not have experience with any of them, try `nano` first. It is a very simple text 
editor. To experiment with it use the following command: 

```bash
$ nano <text-file-name>
```

Get help about `nano` using `Ctrl-G` (marked as `^G` at the bottom).

## StackEdit

If you don't feel comfortable with any of these two text editors, you can use an in-browser Markdown 
editor, such as [`StackEdit`][3]. It will serve you well for most of the editing tasks in this 
workshop.

If you intend to use this tool, you will only have to learn how to copy content from this tool and 
insert it into a text file being edited by `nano` or `vi` and then save it.

To experiment with `StackEdit`, open a new tab in your Chrome Browser and use the following URL:
[`https://stackedit.io/`][3]

After clicking the 'Start Writing' at the top of the `StackEdit` page, you will see a split-screen 
with Markdown input on the left and live Markdown preview on the right.

On the top-right you will see an icon with `#` sign. Click on it to toggle the side-bar and expose
a menu with a 'Markdown cheat sheet' entry. Use it to get familiar with Markdown.

Experiment copying text from `StackEdit` and pasting it into a Markdown file (ending with `*.md`)
that is open using `nano`. Save the edited Markdown file using `nano`.

---

[1]: https://github.com/uribench/handbook-workshop-docker-gotty
[2]: https://handbook.now.sh/
[3]: https://stackedit.io/

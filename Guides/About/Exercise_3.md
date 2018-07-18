# Exercise 3 - Creating Simple Guides and Topics

***Duration: 20 min***

In this exercise we will create simple contents in the form of guides and topics related to one 
subject. We will also embed different types of links referencing internal and external targets.

Perform the following steps in order to create simple guides and topics:


## Step 1: Learn About the Directory Structure of the Handbook Repository

The contents of this repository is used to dynamically build the [Workshop Handbook site][1]. 

The main two data elements in this repository are:

- **Authored content** that is accessible to the end user from the handbook navigation tree 
- **Configuration data files** to construct the handbook navigation tree

Following is the structure of the main directories of the repository:
```
handbook-workshop/          root of the repository
├──config/                  main directory for the configuration files
├──Guides/                  root of the authored contents for guides
├──Topics/                  root of the authored contents for topics
└──Handbook/                handbook navigation tree. created automatically
```

All the authored content is placed under the `Guides` and `Topics` directories.

All the configuration files are placed under the `config` directory. In this exercise we will not 
deal with the `config` directory, and focus on creating new contents under the `Guides` and `Topics` 
directories. 

The resulting handbook navigation tree, which is created dynamically using the authored content and 
configuration files, is placed under the `Handbook` directory.

On the differences between the contents of `Guides` and `Topics` see the next step.


## Step 2: Learn About the Differences between Guides and Topics

Read the respective README files of the [`Guides`][2] and [`Topics`][3] in order to learn about the
differences between them in the context of the Handbook.


## Step 3: Create a Directory for Your Guides

Select a unique name for the directory that will host your guides. Use 'Title Case' with spaces 
("Humanized"). For instance, `Guides by <unique-name>`.

Create a directory with the selected unique name under:

`/app/<your-personal-directory>/handbook-workshop/Guides/`


## Step 4: Create Simple Guides

Use the following guidelines to create two simple Markdown files (ending with `*.md`) with arbitrary 
contents and place them under the newly created directory for your guides.

Guidelines for the Guide Markdown Files:

1. Filename - Use 'Title Case' with spaces ("Humanized"), such as `Getting Started with Vagrant.md`
2. Title - Same as the filename (without the `*.md` extension). Use H1 header.
3. Introduction - Short section immediately below the Title to introduce the guide
4. Additional Sections - One or more additional sections with sub-titles. Use H2 or higher headers.
5. Headers - Do not skip levels, Use H1, H2, H3, etc...

Use other existing guides under the `Guides` directory as examples.

Preview each Markdown file separately using a tool such as the [`StackEdit`][4].

At this stage we do not add cross references or links to external targets.


## Step 5: Create a Directory for Your Topic

Select a unique name for the directory that will host your topic. Use 'Title Case' with spaces 
("Humanized"). For instance, `Topic by <unique-name>`.

Create a directory with the selected unique name under:

`/app/<your-personal-directory>/handbook-workshop/Topics/`


## Step 6: Create a Simple Topic

Use the following guidelines to create one simple Markdown file (`index.md`) with arbitrary 
contents and place it under the newly created directory for your guides.

Guidelines for the Topic Markdown Files:

1. Filename - The main file of the topic has to be called `index.md`. It will serve as the entry
    point when referencing the parent directory. Any addition secondary file under the same 
    directory should have a name using 'Title Case' with spaces. The secondary files, if exist, may
    be referred by the main file, but cannot be referred directly by any guide or other topic.
2. Title - The title of the main file should be the same as the hosting directory. Use H1 header.
3. Introduction - Short section immediately below the Title to introduce the topic
4. Additional Sections - One or more additional sections with sub-titles. Use H2 or higher headers.
5. Headers - Do not skip levels, Use H1, H2, H3, etc...

Use other existing topics under the `Topics` directory as examples.

Preview each Markdown file separately using a tool such as the [`StackEdit`][4].

At this stage we do not add cross references or links to external targets.


## Step 7: Embed Links in the Guides

For an introduction on Markdown links see the [Markdown Cheatsheet][5]. Also, see examples in the
guides under the `Guides` directory.

Add links in the two guide files to refer to each other and to refer to the topic file. Also add at
least one reference to an external source.

Add at least one internal link to a header inside the same file and to a header in other file. See 
examples in the guides under the `Guides` directory.

Note that guides may include references to topics, but topics cannot reference guides.



Now we are ready to proceed and connect the new guides and topics to the Handbook. This will be done 
in the next exercise.

---

[1]: http://workshop.software-engineering-handbook.com/
[2]: /Guides/README
[3]: /Topics/README
[4]: https://stackedit.io/
[5]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links


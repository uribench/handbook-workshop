# Key Concepts

The contents of this repository is used to dynamically build the Handbook site. 

The main two data elements in this repository are:

- **Authored content** that is accessible to the end user from the handbook navigation tree 
- **Configuration data files** to construct the handbook navigation tree

The following sections describe the three main phases leading to the resulting Handbook site:

- Authoring Contents
- Configuration
- Building the Handbook

## Authoring Contents

All the authored content is placed under the `Guides` and `Topics` directories as depicted in the 
following diagram.

![Guides and Topics directories][1]

In general, `Guides` are opinionated in a way that they may include recommendations, while `Topics` 
are attempting to always be clean of opinion and focus on facts. Read the respective README files of 
the [`Guides`][2] and [`Topics`][3] in order to learn more about the differences between them in the 
context of the Handbook.

The `Guides` and `Topics` directories are including exactly one level of directories to group 
the underlying files under well-defined subjects.

Note that the files under the `Guides` directory will be refereed directly by their path and 
filename. The files under `Topics` are arranged differently. A file called `index.md` serves as the 
entry point. It is accessed by referring its parent folder. If this file becomes too large, some 
parts may be externalized to neighboring secondary files. Consider these files as containing 
sections or chapters of the main `index.md` file. The secondary files should not be referred from 
any party expect their neighboring main file.

The links in the bottom part of the next diagram illustrate the rules of what is allowed and what is 
forbidden regarding cross-references. 

![Guides and Topics links rules][4]

`Guides` may freely refer to other `Guides`. `Guides` may refer to `Topics` via their parent 
directory. External parties, including `Guides` are not allowed to refer secondary `Topics` files, 
as their existence is internal implementation details of the `Topics`. To keep `Topics` clean of 
opinions, references from `Topics` to `Guides` are not allowed.

## Configuration

As illustrated by the following diagram, all the configuration files are placed under the `config` 
directory of the handbook repository.

![Configuration files][5]

The `config` directory includes three sub-directories:

- [`navigation`][6]
- [`metadata`][7]
- [`templates`][8]

### `navigation` Directory

The `/config/navigation/root.yml` file and its optionally included external files, define the 
handbook navigation tree using YAML.

The names of the tree nodes in the `/config/navigation/root.yml` file are given in 'Title Case' with 
spaces ('Humanized' style). They are associated with optional metadata files having names that are
the "slagified" version. For instance, A tree node called 'Vagrant and VirtualBox' is matched with
a metadata file called `vagrant-and-virtualBox.yml`. Note that this default scheme can be overridden
using [optional `@id` tag][6]. 

The [`README`][6] file in the `config/navigation` directory has more details.

### `metadata` Directory

For details on the metadata files under the `config/metadata` directory see the respective 
[`README`][7] file.

### `templates` Directory

For details on the template under the `config/metadata` directory see the respective [`README`][8] 
file.

## Handbook Building

The below diagram depicts the process of building the handbook dynamically from the authored 
contents and the configuration files.

![handbook building][9]

The top left side of the above diagram shows the three groups of the configuration files. These
files are used to build the handbook directory tree that includes only directories and `index.md`
files. The handbook content is referred by some of the `index.md` of the handbook directory tree. 
Note that the handbook content itself remains under their `Guide` and `Topics` directories and is 
not copied into the handbook directory tree.

The handbook directory tree on the right side of the above diagram spans the handbook navigation 
configuration as defined by the `config/navigation/root.yml` file and its optionally included 
external files. 

The diagram shows the generated `index.md` files that are injected into all the tree nodes 
directories. When an optional corresponding metadata file does not exist, then a default `index.md` 
file is created. Default `index.md` files include only references to the neighboring directories 
(i.e., sharing the same parent directory with the `index.md` file).

However, when an optional corresponding metadata file does exist, the Jinja2 template engine is used 
with the [template file][10] in order to build a custom `index.md` file based on the metadata from 
the respective file. A custom `index.md` file may include several [optional sections][7], depending 
on their availability on the respective metadata file. In the above diagram, the custom `index.md` 
of the 'GitHub' subject, as an example, is built using the `github.yml` metadata file and the 
`index-template.j2` template.

Notes about the handbook-tools:

- It is a dispatcher for commands to build and maintain the Software Engineering Handbook.
- The source code of these tools are maintained on the [`software-engineering-handbook-tools`][11]
  GitHub repository.
- The handbook tools are implemented in Python 3 as a command line and are available as a Pip 
  package from [PyPI][12].
- To get help on the usage of the handbook command type: `$ handbook -h`

---

[1]: /images/key-concepts/guides-and-topics.png
[2]: /Guides/README
[3]: /Topics/README

[4]: /images/key-concepts/guides-and-topics-links-rules.png

[5]: /images/key-concepts/configuration-files.png
[6]: /config/navigation/README
[7]: /config/metdata/README
[8]: /config/templates/README
[9]: /images/key-concepts/handbook-building.png
[10]: /config/templates/index-template.j2
[11]: https://github.com/uribench/software-engineering-handbook-tools
[12]: https://pypi.org/project/handbook-tools/
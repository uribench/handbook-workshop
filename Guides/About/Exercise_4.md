# Exercise 4 - Connecting the new Guides and Topics to the Handbook

***Duration: 10 min***

In the previous exercise we have create content for guides and topics related to one 
subject. In this exercise we will connect that contents to the handbook navigation tree.


Perform the following steps in order to connect the new guides and topics to the handbook navigation 
tree:


## Step 1: Learn How to Configure the Handbook

All the configuration files are placed under the `config` directory of the handbook repository.

The resulting handbook navigation tree is placed under the `Handbook` directory. It is created 
dynamically using the authored content and the configuration files.

<details>
  <summary><b>Optional Reading:</b> Key Concepts and Principles:</summary>
    &ensp;&ensp;&ensp;&ensp;Read the  
        <a href="https://github.com/uribench/software-engineering-handbook/blob/master/README.md#key-concepts-and-principles">
            Key Concepts and Principles
        </a> to learn more about the subject.
</details>


## Step 2: Create Metadata for the Entry Point for Navigating to the New Subject

Now you have a general idea about the key concepts and principles of the handbook configuration. 
Read the [Metadata Configuration Files][2] to get specific details about the metadata configuration 
files. This include, their purpose, where they are located, file naming convention, their structure, 
examples, and also some technical background about how they are being used with a template. 

Create a new YAML file (ending with `*.yml`) under the `/config/metadata/` directory with three 
key-value pairs based on the following guidelines:

|   key    | guidelines for the value                                |
|:--------:|:--------------------------------------------------------|
| `intro`  | An introduction to the new subject                      |
| `guides` | YAML sequence of the filenames of the guides we created |
| `topics` | Place the filename of the single topic we created       |

The optional metadata configuration files, including the one you are creating here, are used to 
compose the `index.md` files for each directory in the navigation tree.

As an example see the metadata configuration file [`/config/metadata/vagrant-and-virtualbox.yml`][3]
and the resulting [`/Handbook/Development/Vagrant and VirtualBox/index.md`][4] navigation file.


## Step 3: Modify the Navigation Tree to Include a Node for the New Subject

To make the new subject visible in the handbook navigation tree, we need to modify the navigation
configuration file `root.yml` and add a new node representing the new subject.

Each key and value indicators in the the navigation configuration file `root.yml` will have a 
corresponding directory under the `Handbook` directory. 

The optional metadata configuration files, similar to the one created in the previous step, are used 
to compose the `index.md` files for each directory in the navigation tree.

Perform the following actions in order to complete this step:

- Open the `/config/navigation/root.yml` file for editing using your preferred text editor. 
- Identify the `- Made in the Workshop:` line.
- The `- Made in the Workshop:` line represents a key of a key-value pair having a value which is a 
  YAML sequence (array of items indicated with `-`). Currently, the sequence has at least one 
  `Dummy` place holder string item.
- Add a new line below `Dummy` including the name of directory that will represent the new subject
  in the directory hierarchy under the `Handbook` directory. To select the right name you need to
  consider the following points:
  - The new directory will be placed under `Handbook/About the Workshop` directory.
  - An `index.md` file will be created automatically under this new directory, using the 
    corresponding metadata file that was created under the `/config/metadata/` directory in the 
    previous step.
  - Unless otherwise specified (not covered in this workshop), the name has to be the in 
    'Title Case' with spaces ("Humanized") and its "slagified" (all lower case with spaces converted 
    to hyphens) version is used locate the corresponding metadata file.
  - The `index.md` file that will be created will have a title that is equal to the name of the
    new directory.

## Step 4: Build the Handbook

Now that we have all the pieces of the new content in place, we have to build the handbook 
navigation tree under the `Handbook` directory. This will be created dynamically using the 
`handbook-tools`, which will consume the authored content and configuration files and generate the 
`Handbook` directory structure. 

Run the following commands to build the handbook:

```bash
$ cd /app/handbook-workshop
$ handbook build -f
```

<details>
  <summary><b>Optional Reading:</b> Notes about the handbook command:</summary>
    &ensp;&ensp;&ensp;&ensp;- It is a dispatcher for commands to build and maintain the Software 
        Engineering Handbook.<br>
    &ensp;&ensp;&ensp;&ensp;- The source code of this command is maintained on the
        <a href="https://github.com/uribench/software-engineering-handbook-tools">
            software-engineering-handbook-tools
        </a> GitHub repository.<br>
    &ensp;&ensp;&ensp;&ensp;- To get help on the usage of the handbook command type: 
        $ handbook -h<br>
</details><br>

Now we are ready to proceed and push the changes to the remote repository on GitHub, and create a 
pull request to propose our changes. This will be done in the next exercise.

---

[1]: https://github.com/uribench/software-engineering-handbook/blob/master/README.md#key-concepts-and-principles
[2]: /config/metadata/README
[3]: /config/metadata/vagrant-and-virtualbox.yml
[4]: /Handbook/Development/Vagrant%20and%20VirtualBox

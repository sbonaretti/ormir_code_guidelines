# Contributing to the ORMIR documentation

In the ORMIR community, we create and support community documentation, such as the [ORMIR Code Guidelines]() that you are reading or the [ORMIR Data Sharing Guidelines](https://www.ormir.org/data_sharing_guidelines/), as well as documentation of Python packages like [ORMIR-MIDS](https://ormir-mids.github.io/) and [ORMIR-XCT](https://ormir-xct.github.io/).
All our documentation websites are built using [Jupyter Book](https://jupyterbook.org/) and managed through [GitHub](https://github.com/).

Did you spot a typo, find outdated information, or notice something missing in the ORMIR documentation? 
Here you will find a step-by-step guide designed to make contributing as straightforward as possible.
If you are unsure about any part of the process, are looking for something to contribute, or simply have a question, don't hesitate to contact the project coordinators or email us at ormircommunity@gmail.com. 

:::{hint} Why follow this workflow?
At first, this workflow may seem more involved than simply editing a document. However, following it ensures that **your contributions are properly tracked and attributed** through GitHub, making **your work visible to the community** while **helping maintainers review, discuss, and integrate your changes efficiently**. 
Like any new workflow, it quickly becomes familiar and each contribution gets faster and easier!
:::


---

## The contributing process

Contributing to the ORMIR documentation involves three steps: 

```mermaid
flowchart LR
    direction LR
    
    clone[1.Setting up<br>the website locally]
    installJB[2.Making <br>your changes]
    contribute[3.Submitting your<br>changes for review]

    clone --> installJB --> contribute

    
    classDef yellow fill:#ffd42aff,stroke:#d6b656,stroke-width:2px // yellow    
      class clone,installJB,contribute yellow
```
The following sections walk you through each step. 

---

### 1. Setting up the website locally
Before you can edit the documentation, you need to set up the project on your computer so 
you can **make and preview your changes locally** before submitting them for review. 
This setup consists of four steps. 


#### 1.1 GitHub: Create an account
Make sure you have a **GitHub account** and have installed and signed in to either **GitHub Desktop** or **Git**. If you have not, follow the instructions [here](#gh-before-start).
If you already have a GitHub account and GitHub Desktop (or Git), you can proceed directly to the next step.


#### 1.2 GitHub: Fork and clone the repository
First, **fork** (create your own copy of) the documentation repository to your own GitHub account. If you are unfamiliar with forking, find instructions [here](#fork).

These are the current ORMIR documentation projects and their GitHub repositories: 

| Project                       | GitHub repository                                         |
|:----------------------------- |:--------------------------------------------------------- |
| ORMIR Code Guidelines         | https://github.com/ORMIRcommunity/code_guidelines         |
| ORMIR Data Sharing Guidelines | https://github.com/ORMIRcommunity/data_sharing_guidelines |
| ORMIR-MIDS                    | https://github.com/ormir-mids/ormir-mids.github.io        |
| ORMIR-XCT                     | https://github.com/ORMIR-XCT/ormir-xct.github.io          |


Next, **clone** (i.e. download) your fork to your computer. If you are unfamiliar with cloning repositories, follow the instructions [here](#clone).


#### 1.3. Jupyter Book: Install
The easiest way to install Jupyter Book is with `pip install`. Open a terminal (it can also be the terminal inside JupyterLab) and run: 

```bash
pip install "jupyter-book>=2.0.0"
```

If you prefer another installation method, go to the official [Jupyter book installation documentation](https://jupyterbook.org/stable/get-started/install/).


#### 1.4. Jupyter Book: Build the website locally
Open a terminal and run the following commands to navigate to your local copy of the documentation repository and start the website locally:

```bash
cd <path-to-your-folder>
jupyter book start
```

Replace `<path-to-your-folder>` with the path to your local copy of the ORMIR documentation project.


You will see output similar to this:

```{figure} figures/jb_localhost.png
:label: jb_localhost
:alt: jb_localhost 
:width: 50%
:align: center
:figclass: with-border
```

Click on `https://localhost:3000`. A new browser tab will open with the documentation site rendered locally. You are now ready to make your changes. 

---

### 2. Making your changes

#### 2.1 Repository content

An ORMIR documentation repository contains at least the following files:
- `myst.yml`: the main configuration file for the documentation website. It defines the structure of the website, including the table of contents (ToC), which determines the hierarchy and order of the pages, as well as project metadata and build settings. If you would like to learn more about this file, see the [Jupyter Book documentation](https://jupyterbook.org/stable/authoring/table-of-contents/).
- Markdown (`.md`) and/or Jupyter Notebooks (`.ipynb`) files: these contain the content of the documentation. Each file typically corresponds to a page of the website. The homepage is always `index.md`.

#### 2.2 Markdown and MyST markdown
ORMIR documentation uses **MyST (Markedly Structured Text)**, an extension of **Markdown** developed for scientific and technical writing.
In addition to standard Markdown (you can find the syntax rules [here](https://www.markdownguide.org/cheat-sheet/)), MyST adds
[admonitions](https://mystmd.org/guide/admonitions) (notes, warnings, tips), 
[cross-references](https://mystmd.org/guide/cross-references), 
[citations](https://mystmd.org/guide/citations), 
[equations](https://mystmd.org/guide/math), 
[code-cell integration](https://mystmd.org/guide/code), 
[figures](https://mystmd.org/guide/figures), 
and other directives that make it possible to create rich and interactive documentation.
A complete reference to MyST syntax can be found [here](https://mystmd.org/guide/typography).

#### 2.3 Start contributing!

First, create a **branch** (a copy of the project edicated to a specific contribution, topic, or fix). 
If you are unfamiliar with creating a branch, find instructions [here](#branch).  

Then, open the file(s) you would like to edit (or create a new one) using your preferred editor, such as [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/) or [Visual Studio Code](https://code.visualstudio.com/). As you save your changes, Jupyter Book automatically rebuilds the affected pages.

---

### 3. Submitting your changes for review

Once you are done with your changes, [commit](#commit) (save your work), [push](#push) (send the changes to your repository), and [open a pull request](#pr) (propose your changes). A maintainer will review your pull request asap!


<!-- Thank you card -->
<div style="
width:100%;
background:#ffd42aff;
border:1px solid #d6b656;
border-radius:px2;
padding:30px;
text-align:center;
font-size:1.4em;
">

🎉 <strong>Thank you for contributing to the ORMIR community!</strong> 🎉
<br> 
Your contribution helps make musculoskeletal imaging research
more open, reproducible, and accessible for everyone.

</div>

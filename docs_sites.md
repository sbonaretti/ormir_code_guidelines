# Documentation websites

Documentation websites provide a central place where **users and contributors can learn how to install, use, and contribute to your project**. They can include user guides, tutorials, API documentation, and developer guidelines.

Several frameworks are available for building documentation websites. Among the most popular in the Python ecosystem are [Jupyter Book](#jupyter-book), [Sphinx](#sphinx), and [Read the Docs](#read-the-docs). The first two are useful to generate documentation websites, while latter is also a platform for hosting and automatically publishing them.

---

(jupyter-book)=
## Jupyter Book

[Jupyter Book](https://jupyterbook.org/) is the documentation framework most commonly used within the ORMIR community. 
It is built on [MyST Markdown](https://mystmd.org/). 
You can find comprehensive guidelines on the [Jupyter Book](https://jupyterbook.org/stable) website. 
We use Jupyter Book both for writing community documentation, such as these [Code Guidelines]() and the [Data Sharing Guidelines](https://www.ormir.org/data_sharing_guidelines/), and for publishing the documentation of some Python packages, such as [ORMIR-MIDS](https://ormir-mids.github.io/) and [ORMIR-XCT](https://ormir-xct.github.io/).


<!-- In a nutshell:

1. For each website page, create one .md or .ipynb file and write the content using markdown
2. Create a _toc.yml and a _config.yml files (see examples here)
3. Install Jupyter Book with the command pip install jupyter-book
4. Create your book with the command jupyter-book build book_name
5. The created .html files will be in the folder _build/html -->

---

(sphinx)=
## Sphinx 
[Sphinx](https://www.sphinx-doc.org/en) is a tool to write and generate documentation from docstrings.
You can find guidelines on how to use Sphynx [here](documents/ORMIR_Sphinx_SOP.pdf).

---

(read-the-docs)=
## Read the Docs
[Read the Docs](https://docs.readthedocs.io/en/stable/)is a tool to generate code from docstrings and to host and publish documentation on the web. To learn how to use Read the Docs follow their [step-by-step tutorial](https://docs.readthedocs.com/platform/stable/tutorial/index.html). An excellent example of Read the Docs is the [documentation of Ciclope](https://ciclope.readthedocs.io/en/).

---


<!-- ## How do I deploy my Jupyter Book website on GitHub using CI?
[To be updated for jupyter book 2
On GitHub: Setting -> Pages -> Under Build and deployment, Source-> GitHub Actions; Enforce HTTPS

]
CI (Continuous Integration) is a tool that allows you to automate procedures, and in GitHub it is called Actions. Deploying a Jupyter Book website using Actions is very convenient because it automates the building process, ensuring that your site is continuously and seamlessly updated with every change pushed to the repository. You can find detailed information on how to deploy a Jupyter Book website using Actions here. Briefly:
1. Make sure that your repository contains all the website content files, (that is, .md and/or .ipynb files, together with figures, etc.), _config.yml and _toc.yml. Note: You do not need to push the _built folder because GitHub Action will create the .html files of your website
2. In the same repository, add the following files from this ORMIR template folder: requirements.txt, .nojekyll, and .github/workflows/ci.yml (note that .nojekyll and .github/workflows/ci.yml are hidden files)
3. Go to your GitHub repository on GitHub.com. In the top bar, click on Settings, and in the appearing left panel, click on Pages. Under Build and deployment, Source, select GitHub Actions
4. Every time you push new content to the repository, the book will be automatically created and the new .html files will be automatically deployed to your website. You can follow the progress by clicking Actions on the top bar of the GitHub repository -->

## Installation
- With a package manager, just search for "MkDocs"


- Manual installation, for this you need to have Python and pip installed. After having these, just run this two commands to install it and verify it was installed correctly.
  
    `pip install mkdocs`  
    `mkdocs --version` 

For more info and troubleshooting, refer to the main [site](https://www.mkdocs.org/#installation)

## Create a new project

To create a new MkDocs project inside your code repository, all you have to do is follow the next commands

    mkdocs new my-project

Where **my-project** is either your project's folder or, if you are starting with documentation and there is no repository yet, a new folder name that will contain everything.

The command above will create for us our config file `mkdocs.yml` and a docs folder where we will specify our source files for all documentation. 

## Structure

The structure and contents you want to apply will always depend on what your project's code contains, but here are some good standards to follow (in case it applies)

    docs/
         index.md 
         about.md
         setup.md (Steps to run the project)
         configuration-options.md
         license.md
         img/

You can add any other important feature or component regarding your specific project.

## Serve project
The following command will be used to preview our documentation locally.

    mkdocs serve

> You will be able to preview it at **127.0.0.1:8000** or where the terminal indicates.
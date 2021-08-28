# Template repository for creating new Python libraries

This GitHub [template repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/creating-a-repository-from-a-template) can be used to create a new repository with the skeleton of a Python library, based on the [python-lib](https://github.com/simonw/python-lib) cookiecutter.

Start here: https://github.com/simonw/python-lib-template-repository/generate

The name of your repository will be the name of the Python package that you publish to [PyPI](https://pypi.org/), so make sure that name is not taken already!

Add a one-line description of your repository, then click "Create repository from template".

![Screenshot of the create repository interface](https://user-images.githubusercontent.com/9599/131230293-7ed5760e-b385-407e-bbf1-c6fc7540d3fe.png)

Once created, your new repository will execute a GitHub Actions workflow that uses cookiecutter to rewrite the repository to the desired state. This make take 30 seconds or so.

You can see an example of a repository generated using this template here:

- https://github.com/simonw/python-lib-template-repository-demo

## Enabling workflows in your new repository

GitHub Actions like this are not allowed to create new workflows themselves.

Your new repository will have a folder in it called `.github/rename-this-to-workflows` - rename that folder to `.github/workflows` to enable the `test.yml` and `publish.yml` workflows, which can then run tests for your plugin and publish new GitHub releases to PyPI, as [described here](https://github.com/simonw/python-lib#publishing-your-library-as-a-package-to-pypi).

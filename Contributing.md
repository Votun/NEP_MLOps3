# Contributing to the Project

Please read these guidelines before starting your work.


## Working with the Code

Before submitting a Pull Request, make sure your code adheres to the quality standards and coding style guidelines.

### Setting Up the Dev Environment

#### PDM

We use `PDM` for managing our project's dependencies. If you haven't installed `PDM` yet, follow these steps:

1. Install `PDM` globally using pip:
    ```bash
    pip install pdm
    ```
2. Verify the installation by executing:
    ```bash
    pdm --version
    ```

#### Creating and Activating a Virtual Environment


`PDM` automatically creates and manages a virtual environment for your project. To activate the virtual environment for the current project, simply use `PDM` in the project's root directory.

#### Adding New Dependencies

To add a new library as a regular dependency to your project, use the `pdm add` command. For example, to add the requests library, execute the following command:
```bash
pdm add requests
```
This will automatically update the `pyproject.toml` file and the lock file of dependencies, adding the new library and its dependencies.

To add development dependencies, use the `--dev` flag with the pdm add command.

```bash
pdm add --dev pytest
```

After adding new dependencies, it is recommended to run `pdm install` to ensure that all dependencies are correctly installed in your local environment.

##### Exporting Dependencies to a `requirements.txt` File

After adding new dependencies to your project, export the list of all dependencies to a `requirements.txt` file:

```bash
pdm export -f requirements > requirements.txt
```


### Wemake-python-styleguide

В качестве эксперимента используем надстройку над flake8 Wemake.
https://github.com/wemake-services/wemake-python-styleguide

Возм. позже переключимся на связку black+Ruff.

Wemake Docs: https://wemake-python-styleguide.readthedocs.io/en/latest/index.html

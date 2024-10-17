# Developer Guide

## Setting up your work environment

Run these instructions immediately after creating your project with cookiecutter.

1. Navigate to the directory you created:

        cd projetoClassificador

2. Create a virtual environment for your development:

        conda create -n projetoClassificador python=True
        conda activate projetoClassificador

3. (optional) Install the `gh` app to automatically create your repository on GitHub:

        conda install gh --channel conda-forge
        gh auth login

4. Install your module in editable mode:

        pip install -e .

5. Verify that the command-line tool is working:

        projetoClassificador-cli --help

## Syncing with GitHub

### With the `gh` app

In the root folder of your newly created project:

    git init
    git add *
    git commit -m "Initial commit"
    gh repo create projetoClassificador --public --push --source .

### Without the `gh` app

1. In your browser, go to [GitHub](https://www.github.com) and log in as isavrodrigues.
1. Create a new repository (empty, without an initial README, gitignore, etc.) called projetoClassificador (be mindful of capitalization, etc.).
1. Run the commands below in the root folder of your newly created project:

        git init
        git add *
        git commit -m "Initial commit"
        git remote add origin https://github.com/isavrodrigues/projetoClassificador.git
        git push --set-upstream origin main

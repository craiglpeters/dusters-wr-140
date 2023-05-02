[![Codespaces Prebuilds](https://github.com/craiglpeters/dusters-wr-140/actions/workflows/codespaces/create_codespaces_prebuilds/badge.svg)](https://github.com/craiglpeters/dusters-wr-140/actions/workflows/codespaces/create_codespaces_prebuilds)

## Using JupyterLab in GitHub Codespaces

The [Jupyter Project](https://jupyter.org/) creates powerful open source tools for interactive computing. Jupyter tools power many of the most important discoveries and learning experiences in computing.

[GitHub Codespaces](https://github.com/features/codespaces) makes exploration, development, and experimentation using notebooks in Jupyter simpler by automating the set up and management of development environments so you don't have to configure anything on your computer, and you can take advantage of powerful cloud computing environments. This repository provides a straightforward, yet impactful, way to explore the power of using JupyterLab in Codespaces.

## The example - image generation from the James Webb Space Telescope MIRI instrument for WR-140

**Credit for the data and notebook:** WR-DustERS, [ERS 1349](https://www.stsci.edu/jwst/science-execution/approved-programs/dd-ers/program-1349), PI - R. Lau, personal communication, April 2023

This repository contains a Jupyter notebook that converts processed data from the JWST MIRI instrument and uses `astropy.visualization` to render an image of the WR-140 binary star system showing the dynamically generated dust rings. For more details about the research see:

 - DustERS team site https://www.ir.isas.jaxa.jp/~ryanlau/WRDustERS/index.html
 - Nature publication https://www.nature.com/natastron/volumes/6/issues/11

## Working with the Jupyter Notebook in Codespaces

If you are reading these words from the github.com hosted site, simply click on the [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/craiglpeters/dusters-wr-140?quickstart=1) button and you'll quickly be up and running in a codespace. You won't have to install anything on your computer to run the notebook! (If you are already in a codespace, you don't need to click the button again - nothing bad will happen, but, you know :stuck_out_tongue_winking_eye:, [Inception](https://en.wikipedia.org/wiki/Inception).)

> Note: GitHub provides you 120 core-hours of Codespaces for free each month. The Jupyter kernel requires some resources, so it is recommended to use at least a 4 core Codespaces machine for this repository, which means you'll get 30 hours free a month. See [About Billing for GitHub Codespaces](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces) for more details.

The steps that follow illustrate how to work with the notebook in Codespaces using the [VS Code for the Web](https://code.visualstudio.com/docs/editor/vscode-web) default client with the [Jupyter VS Code Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter). There are many ways to run Jupyter in Codespaces described in [Other ways to use Jupyter in Codespaces](0#other-ways-to-use-jupyter-in-codespaces), but the flow is roughly the same. 

1. If you haven't already done so, start a codespace by clicking the "Open in GitHub Codespaces" badge, or using the Code dropdown from the GitHub repository. Codespaces will launch in less than a minute with all the tools you need pre-installed and configured.
2. Once you are in the codespace, open the WR140_MIRI_Image.ipynb notebook from the file explorer. VS Code will load the notebook and automatically activate the Jupyter extension. 
3. Click the "Run All" button in the top bar of the notebook document editor

![Run All](/assets/vscode-jupyter-run-all.png)

4. The Jupyter extension will prompt you for which Jupyter envionrment to use. First select a Python Kernel

![Select Python Kernel](/assets/vscode-jupyter-select-kernel.png)

Then select the recommended Python Environment

![Selct Recommended Python Environment](/assets/vscode-jupyter-select-python.png)

> Note: this Jupyter Python kernel was created by the VS Code Jupyter extension using the codespace user's python environment. This environment includes the packages required by the notebook by using the Codespaces configuration file `.devcontainer/devcontainer.json` to evaluate the `requirements.txt` file in the repository.

5. Scroll down the notebook document to see the processing of each cell. (You can igore the warnings from the astropy.fits processing)

6. Observe the output of the final cell with the `plt.show()` output to see the image of the dust rings spun out by the binary star system observed by the JWST MIRI instrument

## Find the Community and Learn More

You can then explore more about [GitHub Codespaces in the documentation](https://docs.github.com/en/codespaces), and find others in the [Codespaces Community Discussions](https://github.com/orgs/community/discussions/categories/codespaces?discussions_q=is%3Aopen+sync+category%3ACodespaces). 

This repository is configured with a Dev Container to install all the tools and settings you need for your Codespaces environment so you don't have to worry about them. For more information about how this repository is configured, and how you can do this for your own projects, see the [Codespaces: Introduction to Dev Containers](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers) documentation.

### Other ways to use Jupyter in Codespaces

There are many other ways you can use JupyterLab in Codespaces:
1. Start a Codespace from the Code dropdown menu in the repository. Then open the WR140_MIRI_Image.ipynb document by clicking on it in the file Explorer in VS Code. That will prompt the Jupyter VS Code extension to activate, and then you can select the Jupyter Kernel that already has the packages installed because they were setup in the `onCreateCommand` in the `devcontainer.json` file
2. Run a Jupyter server manually in a Codespace by typing `jupyter lab` in the terminal, then CMD+Click one of the published URLs
3. Select the `Open in...` option for the already running codespace listed on the https://github.com/codespaces page, and choose Jupyter
4. Start a codespace from the Code dropdown menu in a GitHub Pull Request
5. Start a codespace from a new branch created from the Issues developmet brach dialog
6. Start a codespace from the VS Code client
7. Use the `gh cs jupyter` cli 


### Codespaces and VS Code Jupyter Extension Documentation

- [Codespaces Documentation: Getting Started with GitHub Codespaces for Machine Learning](https://docs.github.com/en/codespaces/developing-in-codespaces/getting-started-with-github-codespaces-for-machine-learning)
- [VS Code Marketplace: Jupyter Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- [VS Code: Jupyter Notebooks](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)
- [Dev Containers Specification](https://containers.dev)
  - Default image which contains JupyterLab https://github.com/devcontainers/images/tree/main/src/universal
- This repository is configured to start quickly by using Codespaces Prebuilds. A prebuild is used to install the python packages required for the notebook ahead of time, so that when you start a codespace you don't have to wait for the package installation to complete. To learn more see [About GitHub Codespaces Prebuilds](https://docs.github.com/en/codespaces/prebuilding-your-codespaces/about-github-codespaces-prebuilds).
- GitHub CLI https://docs.github.com/en/codespaces/developing-in-codespaces/using-github-codespaces-with-github-cli#open-a-codespace-in-jupyterlab
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/craiglpeters/dusters-wr-140?quickstart=1)
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

If you are reading these words from the github.com hosted site, simply click on the ["Open in GitHub Codespaces"](https://codespaces.new/craiglpeters/dusters-wr-140?quickstart=1) badge at the top of this page and you'll quickly be up and running in a codespace. You won't have to install anything on your computer to run the notebook! (If you are already in a codespace, you don't need to click the button again - nothing bad will happen, but, you know :stuck_out_tongue_winking_eye:, [Inception](https://en.wikipedia.org/wiki/Inception).)

> Note: GitHub provides you 120 core-hours of Codespaces for free each month. The Jupyter kernel requires some resources, so it is recommended to use at least a 4 core Codespaces machine for this repository, which means you'll get 30 hours free a month. See [About Billing for GitHub Codespaces](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces) for more details.

The steps below illustrate using Jupyter Lab as a server running in Codespaces, and connecting via the browser. There are many other ways to use Jupyter, and [some are listed below](#other-ways-to-use-jupyter-in-codespaces).

1. Run
```bash
jupyter lab
``` 
in the terminal

![Run Jupyter Lab in the terminal](/assets/terminal-juptyter-lab.png)

2. Find the URL for the Jupyter server at the end of the terminal output

![Jupyter Server URL in the Terminal](/assets/terminal-jupyter-lab-url.png)

3. Open the URL in another browser window/tab - on Mac use the cmd+click

![Click on the URL to open another tab](/assets/terminal-jupyter-lab-url-click.png)

4. Your JupyterLab session is running!

![JupyterLab in the browser](/assets/jupyter-lab.png)

5. Open the WR140_MIRI_Image.ipynb notebook from the file explorer

![Open the notebook](/assets/jupyter-notebook-pre-run.png)

Note that JupyterLab deteced the kernel running automatically

6. Select 'Run -> Run All Cells` from the JupyterLab menu bar

![Select Run All Cells](/assets/jupyter-run-all.png)

Note that you do not need to worry about installing the required Python packages - those are taken care of for you by Codespaces thanks to the configuration in `/.devcontainer/devcontainer.json`.

7. Scroll down to observe the output of the final cell with the `plt.show()` output to see the image of the spiral of dust rings spun out by the binary star system observed by the JWST MIRI instrument

![Spirals of dust showin in an image from the JWST](/assets/jupyter-plot.png)

## Find the Community and Learn More

You can then explore more about [GitHub Codespaces in the documentation](https://docs.github.com/en/codespaces), and find others in the [Codespaces Community Discussions](https://github.com/orgs/community/discussions/categories/codespaces?discussions_q=is%3Aopen+sync+category%3ACodespaces). 

This repository is configured with a Dev Container to install all the tools and settings you need for your Codespaces environment so you don't have to worry about them. For more information about how this repository is configured, and how you can do this for your own projects, see the [Codespaces: Introduction to Dev Containers](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers) documentation.

### Other ways to use Jupyter in Codespaces

There are many other ways you can use JupyterLab in Codespaces:
1. [Open the WR140_MIRI_Image.ipynb document by clicking on it in the file Explorer in VS Code for the Web.](/jupyter-vscode-extension.md)
1. Run a Jupyter server manually in a Codespace by typing `jupyter lab` in the terminal, then CMD+Click one of the published URLs
1. Select the `Open in...` option for the already running codespace listed on the https://github.com/codespaces page, and choose Jupyter
1. Start a codespace from the Code dropdown menu in a GitHub Pull Request
1. Start a codespace from a new branch created from the Issues developmet brach dialog
1. Start a codespace from the VS Code client
1. Use the `gh cs jupyter` cli 


### Codespaces and VS Code Jupyter Extension Documentation

- [Codespaces Documentation: Getting Started with GitHub Codespaces for Machine Learning](https://docs.github.com/en/codespaces/developing-in-codespaces/getting-started-with-github-codespaces-for-machine-learning)
- [VS Code Marketplace: Jupyter Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- [VS Code: Jupyter Notebooks](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)
- [Dev Containers Specification](https://containers.dev)
  - Default image which contains JupyterLab https://github.com/devcontainers/images/tree/main/src/universal
- This repository is configured to start quickly by using Codespaces Prebuilds. A prebuild is used to install the python packages required for the notebook ahead of time, so that when you start a codespace you don't have to wait for the package installation to complete. To learn more see [About GitHub Codespaces Prebuilds](https://docs.github.com/en/codespaces/prebuilding-your-codespaces/about-github-codespaces-prebuilds).
- GitHub CLI https://docs.github.com/en/codespaces/developing-in-codespaces/using-github-codespaces-with-github-cli#open-a-codespace-in-jupyterlab
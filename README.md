## Using JupyterLab in GitHub Codespaces

The [Jupyter Project](https://jupyter.org/) creates powerful open source tools for interactive computing. These tools power many of the most important discoveries and learning experiences in computing.

[GitHub Codespaces](https://github.com/features/codespaces) makes exploration, discover, development, and experimentation using notebooks in Jupyter a joy. This repository provides a straightforward, yet impactly, way to explore the power of using JupyterLab in Codespaces.

To learn more https://docs.github.com/en/codespaces/developing-in-codespaces/getting-started-with-github-codespaces-for-machine-learning

## The example - image generation from the James Webb Space Telescope MIRI instrument for WR-140

Credit for the data and notebook: WR-DustERS, [ERS 1349](https://www.stsci.edu/jwst/science-execution/approved-programs/dd-ers/program-1349), PI - R. Lau 

This repository contains a Jupyter notebook that converts input from the JWST MIRI instrument and uses astropy.visualization to render an image of the WR-140 binary showing generated dust rings. For more details about the research see:

 - DustERS team site https://www.ir.isas.jaxa.jp/~ryanlau/WRDustERS/index.html
 - Nature publication https://www.nature.com/natastron/volumes/6/issues/11

## Working with the Jupyter Notebook in Codespaces

If you are reading this from the github.com repository code page, simply click on the [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/craiglpeters/dusters-wr-140?quickstart=1) button and you'll quickly be up and running with in a codespace. You won't have to install anything on your computer to run the notebook!

> Note: GitHub provides each of you up to 60 hours of monthly usage of Codespaces for free. See [About Billing for GitHub Codespaces](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces) for details.

The following steps illustrate using the notebook in the [VS Code for the Web](https://code.visualstudio.com/docs/editor/vscode-web) default client for Codespaces with the [Jupyter VS Code Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter). There are many ways to run Jupyter in Codespaces described in [Other ways to use Jupyter in Codespaces], but the flow is roughly the same. 

1. Start a Codespace by clicking the "Open in GitHub Codespaces" badge, or using the Code dropdown
2. Once you are in the codespace, if you are using the default VS Code client, simply open the WR140_MIRI_Image.ipynb notebook from the file explorer, and VS Code will load the notebook. 
3. Then click Run All in the top bar of the notebook document editor

![Run All](/assets/vscode-jupyter-run-all.png)

4. The Jupyter extension will prompt you for which Jupyter envionrment to use. First select a Python Kernel

![Select Python Kernel](/assets/vscode-jupyter-select-kernel.png)

Then select the recommended Python Environment

![Selct Recommended Python Environment](/assets/vscode-jupyter-select-python.png)

> Note: this Jupyter Python Kernel was configured automatically in Codespaces to include all the packages needed for the notebook in the `.devcontainer/devcontainer.json` configuration so that you don't need to install anything.

5. Scroll down the notebook to see the processing of each cell. (You can igore the warnings from the astropy.fits processing)

6. Observe the output of the final cell with the `plt.show()` output to see the image of the dust rings spun out by the binary star system observed by the JWST MIRI instrument

## Find the Community and Learn More

You can then explore more about [GitHub Codespaces in the documentation](https://docs.github.com/en/codespaces), and find others in the [Codespaces Community Discussions](https://github.com/orgs/community/discussions/categories/codespaces?discussions_q=is%3Aopen+sync+category%3ACodespaces). This repository is configured with a dev container to install all the tools and settings you need in the cloud so you don't have to worry about them. For more information about how this repository is configured to run Jupyter automatically, and how you can do this for your own projects, see the [Codespaces: Introduction to dev containers](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers) documentation.

### Other ways to use Jupyter in Codespaces
There are many ways you can use JupyterLab in Codespaces:
1. Start a Codespace from the Code dropdown menu in the repository. Then open the WR140_MIRI_Image.ipynb document by clicking on it in the file Explorer in VS Code. That will prompt the Jupyter VS Code extension to activate, and then you can select the Jupyter Kernel that already has the packages installed because they were setup in the `onCreateCommand` in the `devcontainer.json` file
2. Run a Jupyter server manually by typing `jupyter lab` in the terminal, then CMD+Click one of the published URLs
3. Open in... from the https://github.com/codespaces page and choose Jupyter
4. Start a Codespace from the Code dropdown menu in a GitHub Pull Request
5. Start a Codespace from a new branch created from the Issues developmet brach dialog
6. Use the `gh cs jupyter` cli 


### Documentation and References

https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter
https://code.visualstudio.com/docs/datascience/jupyter-notebooks
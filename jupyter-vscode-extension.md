## Using the VS Code Extension for Jupyter

The steps that follow illustrate how to work with the notebook in Codespaces using the [VS Code for the Web](https://code.visualstudio.com/docs/editor/vscode-web) default client with the [Jupyter VS Code Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter). There are many ways to run Jupyter in Codespaces described in [Other ways to use Jupyter in Codespaces](README.md#other-ways-to-use-jupyter-in-codespaces), but the flow is roughly the same. 

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

6. Observe the output of the final cell with the `plt.show()` output to see the image of the spiral of dust rings spun out by the binary star system observed by the JWST MIRI instrument
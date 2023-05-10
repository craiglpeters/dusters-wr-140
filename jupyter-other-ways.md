If you are reading these words from the github.com hosted site, simply click on the ["Open in GitHub Codespaces"](https://codespaces.new/craiglpeters/dusters-wr-140?quickstart=1) badge at the top of the [README.md](README.md) page and you'll quickly be up and running in a codespace. You won't have to install anything on your computer to run the notebook! (If you are already in a codespace, you don't need to click the button again - nothing bad will happen, but, you know :stuck_out_tongue_winking_eye:, [Inception](https://en.wikipedia.org/wiki/Inception).)

> Note: GitHub provides you 120 core-hours of Codespaces for free each month. The Jupyter kernel requires some resources, so it is recommended to use at least a 4 core Codespaces machine for this repository, which means you'll get 30 hours free a month. See [About Billing for GitHub Codespaces](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces) for more details.

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

## Running Jupyter Lab in the VS Code terminal

This method works either in VS Code for the web for the VS Code client.

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


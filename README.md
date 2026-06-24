# Land_Atmosphere_interactions_notes

Repository containing the practical material for the course of [Land-Atmosphere Interactions](https://studiekiezer.ugent.be/2025/studiefiche/en/I002451). This course materials is also hosted as a website at https://h-cel.github.io/land-atmosphere-interactions-public/.

The assignment (without solutions) can be found on a [public repository](https://github.com/h-cel/land-atmosphere-interactions-public). The solutions are in a [private repository](https://github.com/h-cel/land-atmosphere-interactions), access to which can be granted upon [contacting me](mailto:olivier.bonte@hotmail.com).

## Installation instructions (local setup)

First, make a local copy of this repository using

```
git clone https://github.com/h-cel/land-atmosphere-interactions-public.git
```

or download as zip file and unzip. In each case, make sure to navigate inside the `land-atmosphere-interactions-public` folder before executing any of the command line interface (CLI) instructions below.

Go to the [Quarto download page](https://quarto.org/docs/download/) and download Quarto for your operating system (OS). This repository was built using Quarto 1.9.38.

Next, make sure you have (Mini)Conda installed (download links found [here](https://docs.anaconda.com/miniconda/)). Next open your CLI (or Anaconda prompt) and type:

```
conda env create -f environment.yml
conda activate la_interactions_quarto
```

Next, it is recommended that following Quarto tools are installed:

- In this repository, a final output is rendered to pdf. Therefore, [a LaTeX distribution is needed](https://quarto.org/docs/output-formats/pdf-basics.html#prerequisites). Install the [TinyTex distribution](https://yihui.org/tinytex/), a lightweight version of [TeX Live](https://www.tug.org/texlive/), with following command in the CLI: `quarto install tinytex`. This should be more straightforward than managing your own [Tex distribution](https://www.latex-project.org/get/#tex-distributions).
- To render the diagrams, made with [Mermaid](https://mermaid.js.org/intro/), [quarto needs the Chrome or Edge browser](https://quarto.org/docs/authoring/diagrams.html#chrome-install). If you don't have Chrome or Edge in your local device and prefer to keep it that way, you can install a [Chrome Headless Shell](https://developer.chrome.com/blog/chrome-headless-shell) via quarto in the CLI with `quarto install chrome-headless-shell`. 


There are several ways to use Quarto, but here [VS Code](https://code.visualstudio.com/Download) is used as interface. With VS Code installed for your OS, perform the following:

1. Under extensions, install the [Quarto extension](https://marketplace.visualstudio.com/items?itemName=quarto.quarto).
2. Follow the instructions [here](https://code.visualstudio.com/docs/python/environments#_select-and-activate-an-environment) and select `la_interations_quarto` as your Python interpreter for VS Code.
3. To have a nice preview of your `.qmd` quarto document, use `Ctrl + Shift + k`. After modifying the `.qmd` document, use the same key combination to render the preview again. Alternatively, run `quarto preview --no-browser` in the CLI (this should normally eliminate the need to use `Ctrl + Shift + k` repeatedly).
4. To render the entire set of documents as one `.pdf`, type `quarto render` in the command line. Under the `_book` folder, you can then find the rendered `.pdf`.

For more details on how to use Quarto with VS Code, see the [Quarto documentation](https://quarto.org/docs/get-started/hello/vscode.html).

## Github Actions for automatic publishing

With [publish.yml](.github/workflows/publish.yml), the repository is automatically rendered and published as a website. For more information on how this works, see the [README of the Quarto template repository](https://github.com/olivierbonte/quarto_template_ugent/tree/main#hosting-as-a-website-with-github-actions-and-github-pages) or the [Quarto documentation on publishing](https://quarto.org/docs/publishing/quarto-pub.html).
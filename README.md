# Joyner Document Format

Welcome to the **2022 update** of the Joyner Document Format official LaTeX class.

## TeX Installation

If you already have Tex installed and configured for your OS than you can likely skip to Quick Start section

### MacOS

```sh
brew install text-live-utility
# Ensure required packages are installed
sudo tlmgr install collection-latexrecommended collection-latexextra collection-fontsrecommended collection-fontsextra collection-mathscience
```

### Linux

```sh
# For Ubuntu (From https://github.com/iamjakewarner/jdf/pull/15/files)
sudo apt-get install texlive-full
```

### Windows

#### WSL

Follow the Linux guide for WSL

#### Non-WSL

Install [Strawberry Perl](https://strawberryperl.com/) and [MikTex](https://miktex.org/howto/install-miktex) using these links or by running

```sh
choco install miktex strawberryperl -y
```

Next, follow the instructions for [Installing for VS Code](#vscode-quick-start) but use MikTeX instead of texlive

## CLI Quick start

You can clone this repo and try typesetting `jdf-starter.tex`
with the following commands:

```sh
biber jdf-starter
pdflatex jdf-starter
```

The result should look like `jdf-starter.pdf`.
* `biber` command generates used references from `references.bib` 
* `pdflatex` command generates the final pdf 

## Adding jdf.cls to Global TeX

The `jdf.cls` file can be referenced by updating the `TEXINPUTS` with the path to the git checkout

```sh
export TEXINPUTS=/path/to/the/checkout/jdf/
```

## VSCode Quick Start

1. Add the [Latex Workshop](https://github.com/James-Yu/LaTeX-Workshop) Extension
    - Ensure that `texlive` for your OS is installed. See additional instructions in the extensions' README
2. Use the preview icon (top left) or use the keyboard shortcut (Ctrl + Alt + V). This will open up a live preview.
3. Once done, use the green play button, or use keyboard shortcut (Ctrl + Alt + B) to build the project and generate PDF.
4. You can now view the PDF in visual studio code by clicking the book with magnifying glass icon on the top right (🔍)

## License

Copyright 2019 by Jake Warner.

You have my permission to use JDF in whatever projects you wish,
whether commercial, personal, or otherwise, in whatever way you like.
Official license information can be found in [LICENSE](LICENSE)
(spoiler: it's the MIT License 🙀).

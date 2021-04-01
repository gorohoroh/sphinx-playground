# sphinx-playground
A standard Sphinx setup with Markdown to evaluate for Alemira

## How to use this repository on Windows

### Prerequisites

1. Create a GitHub account and log into GitHub in your browser.
1. Install [Git](https://git-scm.com/download/win) (use defaults in the installer if in doubt).
1. Install the latest [Python](https://www.python.org/downloads/) - in the installer, select "Add Python 3.9 to PATH".
1. Install [VS Code](https://code.visualstudio.com/docs/?dv=win).
1. In VS Code, press *F1*, type "terminal default", select *Terminal: Select Default Profile*, and change the default terminal type from PowerShell to Command Prompt (cmd).
1. Clone this repository from VS Code: click "Source Control" in the left sidebar, then select to clone repository; optionally configure GitHub integration along the way).
1. Open a new terminal in VS Code (*Terminal | New Terminal*). Make sure you're in the root of the cloned repository (*C:\some-path\sphinx-playground*).
1. In the terminal, run `py -m venv .`
1. In the terminal, run `Scripts\activate`.
1. In the terminal, run `pip install -r requirements.txt`.
1. In the terminal, run `Scripts\deactivate`.

### Editing documentation
1. Open a terminal in VS Code. Make sure you're in the root of the cloned repository (*C:\some-path\sphinx-playground*).
1. In the terminal, run `Scripts\activate`.
1. In the terminal, run `sphinx-autobuild source build/html`. From now on, when you make changes to documentation and save them, they will be automatically built to HTML.
1. Open http://127.0.0.1:8000 in the browser: this is where you can see the generated HTML documentation.
1. Edit Markdown (.md) files in the `source` directory or its subdirectories.
1. If necessary, create new Markdown files in the `source` directory or its subdirectories. When you create a new file, add it to the `{toctree}` block in `build/html/index.html` - this will add the file to the table of contents.
1. When ready, commit and push your changes to Git.
1. When you're done working with the documentation:
  1. Press `Ctrl+C` in the terminal to stop watching your source files for changes.
  1. Run `Scripts\deactivate` in the terminal.

## TODO

* [x] Boostrap a Sphinx project
* [x] Enable Markdown authoring
* [ ] Understand and document how to use Sphinx directives
* [x] Provide required packages as requirements.txt (Ekaterina shouldn't need to run each pip command separately):
  ```
  pip install sphinx
  pip install sphinx-rtd-theme
  pip install myst-parser
  ```
* [x] Document how to use this repository.
* [ ] Provide syntax samples and links to syntax references and tutorials
* [x] Enable auto-build on changes.

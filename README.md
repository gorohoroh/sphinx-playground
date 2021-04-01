# sphinx-playground
A standard Sphinx setup with Markdown to evaluate for Alemira

## How to use this repository on Windows

1. Install [Git](https://git-scm.com/download/win) (use defaults in the installer if in doubt).
1. Install the latest [Python](https://www.python.org/downloads/) - in the installer, select "Add Python 3.9 to PATH".
1. Install [VS Code](https://code.visualstudio.com/docs/?dv=win).
1. Clone this repository from VS Code: click "Source Control" in the left sidebar, then select to clone repository; optionally configure GitHub integration along the way).
1. Open a new terminal in VS Code (*Terminal | New Terminal*). Make sure you're in the root of the cloned repository (*C:\some-path\sphinx-playground*).
1. In the terminal, run `py -m venv .`
1. In the terminal, run `.\Scripts\activate.bat`. (If you're seeing an error about disabled scripts, open the PowerShell console and run `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`. After doing so, restart VS Code, open terminal, and try running `.\Scripts\activate.bat` again.)
1. Run `pip install -r requirements.txt`.
1. `make html` (or, if PowerShell refuses to run scripts this way, try `.\make html` instead.)
1. Open `build/html/index.html` in the browser: this is the entry file of your documentation.
1. Edit Markdown files in the `source` directory or its subdirectories. To re-generate HTML documentation after changing Markdown files, run `make html` or `.\make html` in the terminal.
1. If necessary, create new Markdown files in the `source` directory or its subdirectories. When you create a new file, add it to the `{toctree}` block in `build/html/index.html` - this will add the file to the table of contents.
1. When ready, commit and push your changes to Git.
1. When you're done working with the documentation, run `.\Scripts\activate.bat` in the terminal.

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
* [ ] Enable auto-build on changes.

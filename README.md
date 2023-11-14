# MasterDSB-TimeSeries


1. Install poetry : [Introduction | Documentation | Poetry - Python dependency management and packaging made easy (python-poetry.org)](https://python-poetry.org/docs/) (*via* `curl`).
   Note: there can be an [issue](https://github.com/python-poetry/install.python-poetry.org/issues/52) with the official installer on MacOS. Recommended way is to use `brew`:
   ```shell
   brew install poetry
   ```
2. Clone and `cd` into the repo and initialize your virtual environment using:
   ```shell
   poetry install
   ```
3. When using VSCode, you can add your Poetry `virtualenvs` folder to the list of folders VSCode should check:
   1. get Poetry `virtualenvs` location:

      ```shell
      poetry config virtualenvs.path
      ```

      Which should give you something like `/Users/<username>/Library/Caches/pypoetry/virtualenvs`
   2. Add this path to VSCode settings.json:

      ```json
      "python.venvFolders": [
          "/Users/<username>/Library/Caches/pypoetry/virtualenvs"
      ]
      ```
   3. You can now select the Poetry `llm-chatbot-project--<uid>` Python environment and run the notebook.

Other useful `poetry` commands:

* To add other python dependencies, use `poetry add <my-package>`.
* To activate the environment within a nested shell: `poetry shel`l

[![Documentation Status](https://readthedocs.org/projects/mv-tool/badge/?version=latest)](https://mv-tool.readthedocs.io/de/latest/?badge=latest)

# German User Manual for the MV-Tool

This repository contains the German user manual for the MV-Tool, a tool designed to track measures in information security. The MV-Tool supports projects and organizations implementing information security measures according to the [BSI IT Grundschutz](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html) or any other similar procedure or standard.

The MV-Tool allows users to define concrete steps (measures) to implement each information security requirement. These steps can then be tracked in an issue tracker. Currently, only JIRA from [Atlassian](https://www.atlassian.com/software/jira) is supported as an issue tracker.

The MV-Tool itself is made up of two components: the [web API](https://github.com/hutschen/mv-tool-api) and the [web client](https://github.com/hutschen/mv-tool-ng).

## Installation and Preview

This user manual was created with [Sphinx](https://www.sphinx-doc.org/).

To generate and view a local preview of this user manual, you first need to install the necessary dependencies. To do this, install [Python](https://www.python.org) and [Pipenv](https://pipenv.pypa.io/) first. Then, in your terminal, navigate to the root directory of this repository and run the following commands:

```sh
pipenv install --dev && pipenv shell
```

Once the dependencies have been successfully installed, run the following commands to generate the HTML files for the documentation using [sphinx-autobuild](https://github.com/executablebooks/sphinx-autobuild) and to display them in your browser:

```sh
sphinx-autobuild . _build/html --port 9000
```

Alternatively, you can generate the HTML files for the user manual with the following command. The HTML files will then be placed in the `_build/html` directory. You can view the user manual by opening the `index.html` file in your browser.

```sh
make html
```

## License

This user manual is published under the [CC-BY-SA 4.0 License](LICENSE).

Instead, the source code of the [web API](https://github.com/hutschen/mv-tool-api) and [web client](https://github.com/hutschen/mv-tool-ng) of the MV-Tool is open source and is published under [another license](https://github.com/hutschen/mv-tool-api/blob/main/LICENSE).

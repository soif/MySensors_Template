This project aims to serve as a base template for publishing your [MySensors](https://www.mysensors.org/) project on GitHub and get it automatically grabbed and published on [OpenHardware.io](https://www.openhardware.io/)


## Quick Start

1. Use this project as a directory skeleton and include your arduino sketch, images and/or pcb files.

2.  Carefully fill the mysensors.json file to fully describe your project.

3. push it to your github repo.

4. submit your Github repo to [OpenHardware.io](https://www.openhardware.io/)

5. Once approved, your project is automatically published on the OpenHardware.io website, and you just need to push any future update to your GitHub repo.


## Files structure
Your repo should contains at least the following files.

- **MyProject.ino** : the arduino IDE sketch file *named exactly as your repo name*
- **mysensors**.json : a (JSON formatted) file describing your project
- **description.md** : a (Markdown formatted) file containing the full description/story/instructions for your project 

Optionally you can add:
- **images/** to hold your projects photos, shematics, pcb view etc...
- **hardware/** to hold your PCB gerber files, Fritzing files, etc...


## mysensors.json file
Formatted with the [JSON syntax](http://www.w3schools.com/json/json_syntax.asp), It is basically based on the [composer format](https://getcomposer.org/doc/04-schema.md) and server to fully describe your project. It should hold at least the following fields :

- **gh_id** *(required)* 	: your unique Github repo id, made from the end of your GH project repo URL, ie this one is "soif/mysensors_template"
- **type** *(required)* 	: set it to "project"
- **name** *(required)* 	: name of your project
- **baseline** *(required)* : a short description of your project
- **version** *(required)* 	: the version of the project
- **time** *(required)* 	: the latest release date formatted as YYYY-MM-DD
- **keywords** 				: a list of keywords, separated by a comma
- **homepage** 				: the project's site URL
- **license** *(required)* 	: the project's license type and version
- **authors** *(required)* 	:  an array of at least one author, formatted like this:
 - **name** *(required)* 		: Author's FullName
 - **email** *(required)*		: Author's email address
 - **homepage**					: Author's site URL
 - **gh_user** *(required)* 	: Author's username @GitHub
 - **mys_user** *(required)* 	: Author's username @Mysensors
- **images** 				:  an array describing images located in the *images/* directory, each with two fields
 - **type**						:  main | shematic | wiring | pcb_front | pcb_back | misc
 - **file**						:  the file's name
- **hardware** 				:  an array describing files located in the *hardware/* directory, each with two fields
 - **type**						:  fritzing | gerber_tl | gerber_bl | gerber_ts | gerber_bs | gerber_to | gerber_bo | gerber_ml | gerber_dr
 - **file**						:  the file's name

You can check if your JSON syntax is valid by using [this tool](http://jsonlint.com/).


## description.md

Formatted with the [Markdown syntax](https://help.github.com/articles/markdown-basics/) , it should contain the full description of your project, starting first with an introduction text, optionally followed by some (at least second or more level) Markdown headings and texts.
This page will be published asis on hardware.io. 

You can easily preview your document by using a Margown preview site, ie [MarkdownLivePreview](http://markdownlivepreview.com/) or [Dillinger](http://dillinger.io/).
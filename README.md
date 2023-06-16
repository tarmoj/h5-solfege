H5P Solfege - Libraries for ear-training exercises
==========

## About

These H5P libraries have been created to be used in https://sisuloome.e-koolikott.ee/ or similar H5P content systems. 

The software is developed at Georg Ots Tallinna Music School, now Tallinn College of Music and Ballet for project "Digitaalse muusikateooria ja solfedžo õppevara täiustamine ja arendamine"   with the support of European Social Fund (Euroopa Sotsiaalfond).

<img src="./eu.jpg" alt="Euroopa Sotsiaalfond" width="250"/>


The aim of these libraries is to provide H5P content types for creating new solfege (musical ear training)  exercises in following categories:

- degree dictations (in Estonian: *astmediktaadid*)
- harmonic dictations (in Estonian: funktsiooniharjutused)
- musical dictations, one voiced (in Estonian: ühehäälsed meloodilised diktaadid )


See video instructions demonstrating exercises using these content types on e-koolikott (in Estonian):


[Astmediktaatide loomine](https://www.youtube.com/watch?v=WWGh_v6EX9Q&ab_channel=MUBA) <br />
[Diktaatide loomine](https://www.youtube.com/watch?v=SIb7oxUOw2c&ab_channel=MUBA)

Similar exercises, but limited in number,  are realized on: https://otsakool.edu.ee/digisolf



## License

The MIT License -  see LICENSE enclosed in this folder for details.


## Author

Tarmo Johannes tarmo.johannes@otsakool.edu.ee / tarmo.johannes@muba.edu.ee



## Source code of the libraries

The libraries are included here as git submodules. Run `git clone --recursive` or  `git submodule update --init --recursive` to pull or renew them.

The included repositories are:

https://github.com/tarmoj/h5p-harmonic-functions

https://github.com/tarmoj/h5p-degree-dictations

https://github.com/tarmoj/h5p-editor-degree-input

https://github.com/tarmoj/h5p-musical-dictations


Have look to according README.md files to find out more about the libraries.

<br>

## Translating

I suggest h5p tool (see below for creating the translations).

To create a new translation, move to the folder of selected library, create subfolder _language_ (if not existing) and run similar command to:

    h5p create-language-file ./ et

In case of h5p-editor-degree-input just copy the launguage/en.json to <your_laguage>.json and translate the strings.

When the translation is done, upload your the translation files to your testing enivironment (like Drupal7), set the langugage there and test your translation.


See https://h5p.org/h5p-cli-guide#createlanguagecmd and https://h5p.org/documentation/for-developers/translate-h5p-libraries for more info 


<br>

## For Developers

Anyone is free to extend, debug or improve these libraries. Here are some guidelines and hints about the development.

### Setting up H5P development environment

At the moment of writing, it is most convenient and recommended to develop and test these libraries on Drupal 7 content management system (Drupal 8 or 9 do not support H5P development folder that makes work easier).

About setting up Drupal 7: https://www.drupal.org/docs/7/install

Setting up H5P on Drupal 7: https://h5p.org/documentation/setup/drupal7 

*NB! Make sure that you download H5P module meant for Drupal 7, not 2.0.0-alpha or other later version:* https://www.drupal.org/project/h5p/releases/7.x-1.50

Set up development environment, see https://h5p.org/development-environment

It is most convenient to work with the libraries in the development folder `sites/default/files/h5p/development` on the server -  you can copy the folders of your libraries there, they don't need to be packaged and installed as h5p files.

It is wise to install h5p development tools yo your computer (makes translation and packaging easier). Make sure you have nodejs installed in your computer and run

	npm -g install h5p

More info about the h5p tool: https://h5p.org/h5p-cli-guide

*NB! h5p server command (for starting local server) does not work. You need to test your libraries on a web server with Drupal 7 installed.*



### Structure of the libraries, working with the code

**H5P.HarmonicFunctions** is based on a simple, "old style" template similar to https://h5p.org/tutorial-greeting-card,  the library is pure javascript (using H5P.jQuery though), no external libraries are used. All the functionality is in `harmonicFunctions.js` that you can edit and change directly on the server in *development* folder -  if your operating system and software enables it.

**H5P.DegreeDictations** is based on h5p-boilerplate template https://github.com/h5p/h5p-boilerplate, it uses **nodejs** and **babel** for its development, also **Tone.js** library for sound production. After cloning or downloading the library source code you need to do navigate to its rootdirectory and run (this also installs Tone.js node module):

	npm install

And for building:

	npm run build

The build result will be placed into folder `dist`. You need to copy the `dist` folder, `semantics.json, library.json, package-lock.json` to you H5P library, the rest is only for development.

`src/entries/h5p-degree-dictations.js` is the entry point for H5P and declaration of the class, the main code resides in `src/scripts//h5p-degree-dictations.js` 

Folder `src/instruments` contains the sound samples for playing the dictations and `src/styles` obviously the css definitions.

To make building and deploying easier, there is `deploy.sh` script in the root folder of the library. Edit the (sftp) server address, username and port according to your setup.

The semantics file requires a special custom H5P editor widget for conveniently entering and validating the degrees. The source code of the widget resides here: https://github.com/tarmoj/h5p-editor-degree-input

It has to be placed next to H5P.Degreedictations to the development folder of Drupal 7. For making final h5p file, package it with running this command in the parent directory of the libraries:  
  
	h5p pack h5p-degree-dictations h5p-editor-degree-input  DegreeDictations.h5p  


**H5P.MusicalDictations** is similar to H5P.DegreeDictations -  it uses **babel** and **nodejs** for developmnent, next to that it is based on **React**. It uses Lilypond as its notation language + graphical UI, VexFlow for rendering notation.

The library depends on these React components that are used both in editor and library: https://github.com/tarmoj/vexflow-react-components (pulled as submodule).

Building and deploying is similar to H5P.DegreeDictations.


<br>

### Packaging, preparing h5p files


To make the final h5p file, it is recommended to use the h5p tool, run from the root folder (h5p-solfege):

	h5p pack h5p-harmonic-functions HarmonicFunctions-<version>>.h5p
    h5p pack h5p-degree-dictations h5p-editor-degree-input  DegreeDictations-<version>.h5p
    h5p pack h5p-musical-dictations h5p-editor-notation-input  MusicalDictations-version.h5p


<br>


### Sending libraries to https://sisuloome.e-koolikott.ee

Please contact HTM (*to be extended*).

 
<br> 

### Maintenance and risks


These H5P libraries do not depend on external libraries -  everything necessary is bundled in, in the state it was tested and reported to work. Unless there are major changes on the browser side, they should stay functional.

In case of problems, the source code is sufficiently commented and written in comprehensive way, it should be understandable and editable for any person with sufficient skills.

The developers have done its best to make the software as stable and user friendly as possible but do not forget,  according to the MIT license, the software is issued under:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
 
 







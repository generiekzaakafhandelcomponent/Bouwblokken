# Building blocks

![en](https://img.shields.io/badge/lang-en-red.svg)

Building blocks are a collection of files, that can be used to supplement a process or other parts of an implementation.
These can consist of forms, form flows, plugins, custom front-end, and back-end code. Unlike [process blueprints](blueprints.md),
building blocks do not contain a process definition. For example, a plugin that allows sending messages via Slack could be a building block.

## How to import a building block

Importing a building block and customizing it for a specific use case can be done by following the instructions on
this page. Additionally, specific instructions for a building block can be found on GitHub for that particular building 
block. These always take precedent over these general instructions.

### Copying files

Almost all files in `backend` can be copied into the back-end of an implementation project. The exceptions are:

* `application.yml`. This only includes the configurations required by the building block. These should be merged
  with the `application.yml` you already have.
* `build.gradle` or `pom.xml`. This only includes the dependencies required by the building block. These should be
  merged with the `build.gradle` or `pom.xml` you already have.

Almost all files in `frontend` can be copied into the front-end of an implementation project. The exception is
`package.json`. This only includes the dependencies required by the building block. These should be merged with
the `package.json` you already have.

### Configuring and customizing the building block

A building block will not always work out of the box (e.g. plugins need to be configured).
Each building block comes with a README that explains the specifics that should be configured in order for the
building block to be used. In addition to this, consider the following checklist:

* Does this building block rely on or contain plugins? If so, these will have to be configured.
* Are there dependencies or application properties that have to be configured?
* If there are form flows, are all the forms it references present?

> Be sure to follow the specific instructions that are included in the README of the building block.

Instructions on how to contribute to this repository can be found [here](https://github.com/generiekzaakafhandelcomponent/Bouwblokken/blob/main/CONTRIBUTING.md).

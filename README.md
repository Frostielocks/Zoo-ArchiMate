# Zoo-ArchiMate
An ArchiMate model for Zoo, a conceptual custom IT service provider.

This model is used to:
1) Maintain an architecture of my personal IT initiatives for documentation purposes.
2) Practice ArchiMate modeling to develop and maintain my modeling skills.
3) Educate and spread awareness on the importance of enterprise architecture and how to use the ArchiMate framework.

![](capability-map-cover.jpg)


## Getting Started
If you're an ArchiMate veteran directly using the [source model](#source) will provide the best experience.

We recommend newcomers to the ArchiMate language to instead download or fork the repository and use the [HTML documentation site](#html-documentation-site) which is usable even without having any modeling tools installed.

If you just want to consult the diagram without even downloading or forking the repository you can check out the [PDF jasper report](#jasper-reports) which will render in a browser.


## Using the Model
We provide several different ways to consult the ArchiMate model.

### Source
The model is developed using .archi format.
An xml file is also included in ```/exports/``` if you would like to 

### HTML Documentation Site
The diagram is exported as an interactive HTML documentation website.
this can be found in

### Jasper Reports

## Contributing
Currently [FrostTusk](https://github.com/FrostTusk) is the sole contributor for the project.

### Submitting Changes
Suggested changes can be submitted by creating a pull request.
Make sure to export to all file formats before submitting exports/html/ exports/zoo-archimate.csv exports/zoo-archimate.xml and exports/reports)
Before submitting any change
Make sure to read the [namespaces section](#Namespaces) when adding new views or folders.

### Namespaces
This archimate project is structured using namespaces.
Namespaces help keep view filenames descriptive and ensures views are ordered correctly in reports.
They work by prepending [\<namespace id\>] (with namespace code being a unique 2 letter (or 1 if it's the first namespace) code that describes the namespace).
Example: [ABCD] defined by [AB] Artilley Basics and [ABCD] Artilley Basics Collateral Damage.
An important file is denoted by adding an exclamation mark "!" at the end of the namespace id.
This ensure that important view is rendered before any other views within the namespace.
For example: [AB!] denotes an important view in the Artilley Basics namespace.


There are two exceptions to this rule: library views are prepended with "__" and deprecated views are prepended with "_".
Outdated architectural views and drafts.

## Acknowledgements
* [ArchiMate® ](https://prod.opengroup.org/archimate-forum/archimate-overview): Enterprise Architecture Modeling Language by the Open Group
* [Archi](https://www.archimatetool.com/): Open Source modelling toolkit for creating ArchiMate models and sketches
# Zoo-ArchiMate
An ArchiMate model for Zoo, a conceptual custom IT service provider.

This model is used to:
1) Maintain an architecture of my personal IT initiatives for documentation purposes.
2) Practice ArchiMate modeling to develop and maintain my modeling skills.
3) Educate and spread awareness on the importance of enterprise architecture and how to use the ArchiMate framework.

![](capability-map-cover.jpg)


## Getting Started
If you're an ArchiMate veteran directly using the [source model](#source) will provide the best experience.

We recommend newcomers to the ArchiMate language to instead download or fork the repository and use the [HTML documentation website](#html-documentation-website) which is usable even without having any modeling tools installed.

If you just want to consult the diagram without even downloading or forking the repository you can check out the [PDF jasper report](#jasper-reports) which will render in a browser.


## Using the Model
We provide several different ways to consult the ArchiMate model.

### Source Model
The model is developed in the ```Zoo.archimate``` source file which can be opened with the [Archi](https://www.archimatetool.com/) modeling tool.
The repository also includes an alternative *Open Exchange File* in ```exports/Zoo.xml``` if you would like to use your own prefered modeling tool.

### HTML Documentation Website
We regularly export the diagram as an interactive HTML documentation website.
You can consult it by opening ```exports/html/index.html``` in your browser of choice.

### Jasper Reports
We regularly export the model as *Jasper Report* in different file formats which can be found under ```exports/reports/```.
A *Jasper Report* is a documented digest of the ArchiMate model which can be read as a business report.

### CSV
We regularly export the model as *CSV File* in ```exports/Zoo.csv``` which can be used to process data conveyed within the model.


## Contributing
Currently [FrostTusk](https://github.com/FrostTusk) is the sole contributor for the project.

### Submitting Changes
Suggested changes can be submitted by submitting a pull request.
Make sure ```exports/``` is updated before submitting!
Check out the [Using the Model](#using-the-model) section to ensure your exports are complete.
Also consult the [namespaces](nNamespaces) section when adding new views or folders to the source model.

### Namespaces
This archimate project is structured using namespaces.
Namespaces help keep view folder and view names descriptive and ensures views are ordered correctly in exported reports.

Namespaces work by prepending ```[<namespace IDs>]``` to a view or folder.
A namespace ID is a unique one or two letter alphanumeric code that describes the namespace.
You should only use one letter codes on hierarchical top level namespaces.
Folders define a namespace.

*Example*: ```[ABCD] Application Usage``` is a view stored under the ```[ABCD] Collateral Damage``` folder which is itself stored under the ```[AB] Artilley Basics``` folder. The namespace ```[AB] Artilley Basics``` could also be shortened to ```[A] Artilley``` because it is a hierarchical top level namespace.

Use an exclamation mark ```"!"``` at the end of a namespace ID to denote an important view.
This ensures that the rendering software displays that important view before any other views within the namespace.
Good targets for important views are views that provide a helicopter look at the system under design.

*Example*: ```[AB!] Capability Map``` denotes an important view, "Capability Map", in the Artilley Basics namespace.

The root folder is the empty namespace and views stored under this folder must still prepend ```[]``` in front of their name. Typically you will only include important files in the root folder.

*Example*: ```[!] Organization Diagram``` denotes an important view, "Capability Map", in the root folder.


There are two more special namespaces defined by the ```__libraries``` and ```_deprecated``` folders. Any view in one of those folders should prepend ```__``` or ```_``` to its name respectively and will always be rendered last.
Library views denote views that define concepts not intrinsic to the system under design but are still useful for illustrative purposes.
Deprecated views are views that are in the process of being removed from the model but might still reference concepts defined in some other view.

*Example*: ```_Weird Test Diagram``` denotes an old testing view that is in the process of being removed. The rendering software will always render this view last with other deprecated views.


## Acknowledgements
* [ArchiMate® ](https://prod.opengroup.org/archimate-forum/archimate-overview): Enterprise Architecture Modeling Language by the Open Group
* [Archi](https://www.archimatetool.com/): Open Source modelling toolkit for creating ArchiMate models and sketches

# PlantUML Styles
This repository contains the style definitions we typically use in combination with [PlantUML](http://plantuml.com/). To use these styles in a diagram,
include the snippet below in your plantuml file.


    !includeurl https://raw.githubusercontent.com/inthepocket/plantuml-styles/master/styles.plantuml!0
 
## Running the examples

This repository contains a number of [examples](https://github.com/inthepocket/plantuml-styles/tree/master/examples) that are meant to test
the stylesheet in different scenarios. The recommended way to test these examples, is to use **Visual Studio Code** with the PlantUML plugin.

## PlantUML server

This repository contains a modified version of the `plantuml-server`, released under the GPL3 license, that demonstrates how a stylesheet
can be applied server-side. In this scenario, it is no longer necessary to use `!include` or `!includeurl` directives. To test it, run:

    docker run -p 8080:8080 inthepocket/styled-plantuml-server


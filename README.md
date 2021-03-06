# Virtual Barcodes

R/Shiny app to display virtual barcodes for [DPO Mass Digitization](https://dpo.si.edu/mass-digitization-program) projects.

The app allows to search a local database of objects and displays a QR code with the ID of the object. In addition, any other data fields present in the database are displayed for the object row selected. 

This app uses a field already in the collection database to link the images taken with the collection record. 

It is assumed that:

 * The objects do not have barcodes 
 * No printed barcodes will be used
 * The connection will be direct between the filename and the specified field from the database
   * There is the option for a prefix or suffix to the field

In the case the object has an image in EDAN, this image will be displayed.

## Screenshots

This example is from the CHSDM collection and displays the QC code as well as the image of the object from EDAN:

![ch_example](https://user-images.githubusercontent.com/2302171/111470935-be73b000-86fe-11eb-9c01-67bc5c3c8ce1.png)

## Requirements

 * R and the packages:
   * [shiny](https://cran.r-project.org/package=shiny)
   * [DT](https://cran.r-project.org/package=DT)
   * [RSQLite](https://cran.r-project.org/package=RSQLite)
   * [dplyr](https://cran.r-project.org/package=dplyr)
   * [shinyWidgets](https://cran.r-project.org/package=shinyWidgets)
   * [qrcode](https://cran.r-project.org/package=qrcode)
   * [EDANr](https://github.com/Smithsonian/EDANr) (If querying EDAN)
 * [Shiny](https://shiny.rstudio.com/)

## Future enhancements

 * An option to print the barcodes on demand, when these will be applied to objects in a collection
 * Save other data fields

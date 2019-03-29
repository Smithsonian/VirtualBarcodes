# Virtual Barcodes

R/Shiny app to display virtual barcodes for [DPO Mass Digitization](https://dpo.si.edu/mass-digitization-program) projects.

The app allows to search a local database of objects and displays a data matrix barcode with the ID of the object. In addition, any other data fields present in the database are displayed for the object row selected. 

This app uses a field already in the collection database to link the images taken with the collection record. 

It is assumed that:

 * the objects do not have barcodes 
 * no printed barcodes will be applied
 * the connection will be direct between the filename and the specified field from the database

In the case there is already an object that has an image in EDAN, this image will be displayed.

## Requirements

 * R and the packages:
   * [shiny](https://cran.r-project.org/package=shiny)
   * [DT](https://cran.r-project.org/package=DT)
   * [RSQLite](https://cran.r-project.org/package=RSQLite)
   * [dplyr](https://cran.r-project.org/package=dplyr)
   * [futile.logger](https://cran.r-project.org/package=futile.logger)
   * [shinyWidgets](https://cran.r-project.org/package=shinyWidgets)
   * [EDANr](https://github.com/Smithsonian/EDANr) (If querying EDAN)
 * [Shiny](https://shiny.rstudio.com/)
 * Python3 and the modules:
   * PIL
   * [pylibdmtx](https://github.com/NaturalHistoryMuseum/pylibdmtx)

## Future enhancements

 * An option to print the barcodes on demand, when these will be applied to objects in a collection
 * Update the record in the database to indicate that the object has been digitized
 
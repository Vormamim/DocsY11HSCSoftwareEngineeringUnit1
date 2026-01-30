---
icon: book-open
---

# Maintenance

Maintenance is an ongoing process of correction and refinement. Software products have a life span and over this time will require maintenance to meet the expectations of their users. This process involves ongoing communication with the product’s users. Once a decision has been made to modify the product, the software development cycle is commenced and on completion a method of distributing the modification is devised. For example, small bug fixes may be distributed as a patch, whereas new features may require a complete upgrade.

## Modification of Code to meet Changed Requirements

Software solutions are not static entities - they evolve over time. Most applications mature as new versions are introduced. These new versions will correct bugs and introduce new functionality not present in the original product. Changes made to subsequent releases of applications are often the result of user requests. Many software companies provide facilities for users to make suggestions in regard to new functionality or changes to existing functionality. Remember, fulfilling the requirements of end users is a central aim for most software products.

## Identification of the Reasons for Change in Source Code

Reasons for change common to all applications include bug fixes, new hardware and upgrading to take advantage of features available in new operating systems.

A software company whose products have a large customer base may receive many thousands of requests for modification of their products. The company must then prioritise these requests and make decisions on which modifications will be included and which will not. Often registered users are surveyed to obtain their views on possible modifications. Support departments provide a valuable source of data: the number of support issues about specific functions highlights useability problems. This information can be used as the basis for selecting appropriate modifications for inclusion in an upgrade.

## Determining the Scope of the Change

Documentation of the original product’s development will prove invaluable to maintenance programmers. Maintainability is a measure of how easily a solution can be maintained and is closely linked to the quality of the original documentation. Often the maintenance programmer will not be the same as the original programmers. Many software development companies have a separate team of maintenance programmers.

Once a decision has been made to modify a particular aspect of a product, the location of the section to be altered needs to be determined. Models of the system are used to assist in this process. Structure charts and data flow diagrams will assist in the location of the module or modules requiring modification. Once a module has been identified, the programmer can analyse the original algorithms and models, and the actual source code. A thorough understanding of the original source code is required before any modifications are undertaken.

## Determining the Changes

After the section of code to be modified has been located, we need to determine the changes to be made. Depending on the nature of the modification, changes may be required to data structures, files, and the user interface, as well as to the source code.&#x20;

The consequences of changes made to one module must be considered. If a record data structure is altered then what effect will this have on other modules that access this data? For example, if a field within a record that once contained Boolean data is changed to hold integer data then there will be consequences for all modules that access these records. We don’t want to solve one problem only to cause a number of new ones. Analysis of the original documentation should alert programmers to the possible consequences of changes.

## Implementing and Testing the Change

Once the changes to be made have been determined, these changes must be implemented within the existing application. In many cases, changes will be made to the source code and the application will be recompiled, tested, and distributed. In other cases, a small application or patch may be written to implement the changes on end users’ systems. Custom systems can often be changed directly on the site or over an internet link. This is particularly the case with script and macro modifications.

The implementation of modifications can have a ripple effect to other aspects of the application. These problems are minimised if the original product was designed using a structured modular approach. When each procedure or function has been designed independently then the effect of changes will be easier to identify and correct. Modules that are used in several places throughout the application should be modified in such a way that they retain their original processing, including input and output parameters. Changes to modules that alter parameters will require modifications to each higher-level calling module.

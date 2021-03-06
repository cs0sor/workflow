---
slug: importing-opportunities-into-act
redirect_from: "/article/142-importing-opportunities-into-act"
title: Importing Opportunities into ACT!
---
This task will create new Opportunities in ACT!. See the [ACT! Opportunity XML](act-opportunity-xml) page for more information.

This task requires a Connection to ACT!, for more information on setting up and managing ACT! connections, see [Connecting to ACT!](connecting-to-act).

## Connection Settings  
### ACT! Connection
_Required_  
The ACT! connection to import Opportunities into. See the [Connecting to ACT!](connecting-to-act) page if you require more information on how to create/manage Zynk Connections to ACT!.  
Defaulted to the connection marked as the default for ACT!. For more information on managing default connections within Zynk, see the [Connection Manager](connection-manager) page.

## File Settings
### Fail File
_Required_  
An absolute or relative file path on the local computer or network to save any Opportunities which failed to import into ACT! to. See the [Zynk Objects](zynk-objects) page if you require more information on how the Zynk Object file value works.  
Defaulted to `act_import_opportunities_fail.xml` in the current working directory.  

### Input File
_Required_  
The absolute or relative file path to the XML file containing the ACT! Opportunities to import. This can also be inline XML, e.g. by generating the data using a razor script or by providing a URI to a script generating the data and specifying 'Read contents of file'. See the [Zynk Objects](zynk-objects) page if you require more information on how the Zynk Object file value works.  
Defaulted to use the `Output from the previous task`.

### Success File
_Required_  
An absolute or relative file path on the local computer or network to save all Opportunities which were successfully imported into ACT! to. See the [Zynk Objects](zynk-objects) page if you require more information on how the Zynk Object file value works.  
Defaulted to `act_import_opportunities_success.xml` in the current working directory.

## Import Settings  
### Auto Create Products  
_Required_  
Set to `true` to automatically create any Products on imported Opportunities that don't exist in ACT!. If this setting is not enabled then any Opportunities containing Products that don't exist in ACT! will fail to import.  
Defaulted to `true`.

### Prevent Duplicates 
_Required_  
Set to `true` to prevent Opportunities with the same `Id` from being imported more than once. This feature will only work for Opportunities that are imported with a `Id`, see the [ACT! Opportunity XML](act-opportunity-xml) page for more information.  
Defaulted to `true`.

## Zynk Settings
See [Common Task Settings](common-task-settings).

## Articles and Sample Files
For full documentation and samples, see [ACT! Opportunity XML](act-opportunity-xml).

## Links
- [Introduction to the ACT! Connector](act)
- [Connecting to ACT!](connecting-to-act)
- [Importing Companies into ACT!](importing-companies-into-act)
- [Exporting Companies from ACT!](exporting-companies-from-act)
- [Importing Contacts into ACT!](importing-contacts-into-act)
- [Exporting Contacts from ACT!](exporting-contacts-from-act)
- [Importing Opportunities into ACT!](importing-opportunities-into-act)
- [Exporting Opportunities from ACT!](exporting-opportunities-from-act)
- [Importing Products into ACT!](importing-products-into-act)
- [Exporting Products from ACT!](exporting-products-from-act)


---
slug: import-items-to-my-mobile-workers
title: Import Items to My Mobile Workers
---
The My Mobile Workers platform will allow you to import items via the API. For example, if you have product records that are maintained in an external system that you want to keep up to date in My Mobile Workers you would use this task as part of your process to import them.

The API documentation provided by My Mobile Workers is available [here](https://docs.mymobileworkers.com/index.php?title=Create_Items).

This task will import items to My Mobile Workers in an XML format.

## Settings
### Connection
_Required_
The My Mobile Workers connection to use. See the [Connecting to My Mobile Workers](connecting-to-my-mobile-workers) article for more information.

### Fail File
_Required_
The file to write failed records to.

### Input File
_Required_
The file containing the records you wish to process.

### Success File
_Required_
The file to write successful records to.
---
slug: sugar-crm-to-sage-50-integration
redirect_from: "/article/468-sugar-crm-to-sage-50-integration"
title: Sugar CRM to Sage 50 Integration
---
 This tutorial details the basic principles when dealing with an integration between Sugar CRM and Sage 50. This workflowwill perform two basic tasks, which is the downloading opportunities from Sugar CRM to Sage (as sales orders), and uploadthe sales order number generated by Sage back to Sugar CRM.        

You can download a copy of the workflow from our             [GitHub samples](https://github.com/zynksoftware/samples/tree/master/Integration%20Samples/Sugar%20CRM%20to%20Sage%2050%20Integration).

## Assumptions
We make the following assumptions about how the integration should work:

 * A single S1 product will be used on the sales orders in Sage for the total amount of the opportunity.
 * A custom field named 'sales_order_no_c' has been added to the opportunities module in Sugar, and will be used                by the integration to store the Sage sales order number that corresponds with each opportunity in Sugar.
 * A custom field named 'sales_account_ref_c' has been added to the accounts module in Sugar, and will store the                Sage customer account reference that corresponds with each account in Sugar.
 * The customers will already exist in Sage, so the workflow will not create them if they don't, and will log an                error.

## Download Opportunities from Sugar - Phase 1
This part of the process will download new 'Closed Won' opportunities from Sugar CRM and import them in to Sage as sales            orders. The process consists of the following tasks:

1. [Querying Records in SugarCRM](querying-records-in-sugarcrm) - This task will query Sugar CRM                for all opportunities and their related account where the 'sales_stage' field is set to 'Closed Won', and                the 'sales_order_no_c' field is blank. The results will be saved to the 'sugar_opportunities.xml' file.
2. [XSLT Transform](xslt-transform) - This task will transform the output file from                the previous task to sales orders in the Zynk XML format, ready to be imported into Sage. Refer to our                 [API Documentation](zynk-xml-overview) for detailed XML schema information.
3. [Importing Sales Orders into Sage 50 UK](importing-sales-orders-into-sage-50-uk) - This task will import                the sales order XML generated by the previous task into Sage. It will write out any failed and successful                imports to separate success and fail files.

## Upload Sales Order Numbers to Sugar - Phase 2
This part of the process will upload the sales order number of successfully imported sales orders to the corresponding opportunity            in Sugar CRM. As we only download opportunities in phase 1 where the 'sales\_order\_number\_c' field has not been,            this will prevent opportunities that have already been processed from being downloaded again. The process consists            of the following tasks:

1. [XSLT Transform](xslt-transform) - This task will transform the success                file from the import sales orders task to opportunity updates in the Sugar XML format. It sets the 'sales_order_no_c'                field on each opportunity to the sales order number from Sage.
2. [Inserting Records to SugarCRM](inserting-records-to-sugarcrm) - This task will upload the                opportunity updates contained in the output file from the previous task to the 'Opportunities' module in                Sugar. The opportunities are matched based on the 'id' field, which was downloaded by the first task in the                workflow.

## Archive - Phase 3
This is the final task in the process, and will archive off all data that was used by the workflow process. This allows for            traceability and will assist when debugging the workflow.

1. [Archive Workflow Data](archive-workflow-data) - This task will archive off all data that was                used by the workflow process.

If you have any queries on any of the above, feel free to contact our support team via email at support@zynk.com            or via telephone on 0191 303 7279. Please note, as stated on the Auto Mapper task we do not support any changes            to XSLT.
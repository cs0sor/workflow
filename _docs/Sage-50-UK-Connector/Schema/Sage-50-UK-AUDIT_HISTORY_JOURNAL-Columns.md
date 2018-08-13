---
slug: sage-50-uk-audit_history_journal-columns
title: Sage 50 UK AUDIT_HISTORY_JOURNAL Columns
---
# AUDIT_HISTORY_JOURNAL Columns

| Name | Type  |  Length | Precision  |  Notes  | Example |
| --- | --- | --- | --- | --- | --- |
| TRAN_NUMBER | INTEGER | 4 | 10 | Transaction number |  |
| TYPE | VARCHAR | 2 | 2 | Transaction type |  |
| DATE | DATE | 2 | 10 | Transaction date |  |
| NOMINAL_CODE | VARCHAR | 8 | 8 | Nominal Code |  |
| USER_NAME | VARCHAR | 32 | 32 | User name |  |
| DETAILS | VARCHAR | 60 | 60 | Details |  |
| EXTRA_REF | VARCHAR | 60 | 60 | Extra Reference |  |
| DISPUTED | SMALLINT | 2 | 5 | Disputed flag |  |
| VAT_FLAG | VARCHAR | 1 | 1 | VAT reconciled flag - y/n/- |  |
| PAID_FLAG | VARCHAR | 1 | 1 | Transaction paid flag - y/n |  |
| PAID_STATUS | VARCHAR | 2 | 2 | Transaction disputed/paid status - */p/d*/dp/ |  |
| DEPT_NUMBER | SMALLINT | 2 | 5 | Department number |  |
| DEPT_NAME | VARCHAR | 60 | 60 | Department name |  |
| TAX_CODE | VARCHAR | 3 | 3 | Tax code (T0 to T99) |  |
| DELETED_FLAG | SMALLINT | 2 | 5 | Transaction deleted flag |  |
| AMOUNT | DOUBLE | 8 | 15 | Signed amount (credits negative) |  |
| FOREIGN_AMOUNT | DOUBLE | 8 | 15 | Signed amount (foreign currency, credits negative) |  |
| SPLIT_NUMBER | INTEGER | 4 | 10 | Split number |  |
| HEADER_NUMBER | INTEGER | 4 | 10 | Header number |  |
| VAT_FLAG_CODE | TINYINT | 1 | 3 | VAT reconciled flag - 0/1 |  |
| DATE_ENTERED | DATE | 2 | 10 |  |  |
| VAT_RECONCILED_DATE | DATE | 2 | 10 | VAT Reconciled Date |  |
| RECORD_CREATE_DATE |  | 16 | 0 | Date and time when the record was created. |  |
| RECORD_MODIFY_DATE |  | 16 | 0 | Date and time when the record was modified. |  |
| RECORD_DELETED | TINYINT | 2 | 3 | Flag denoting if the record has been deleted or not. |  |
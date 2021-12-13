{
  "date" : "2019-10-11",
  "keywords" : [ "aba file", "aba file format", "what is an aba file", "file", "aba example", "aba file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ABA - CemText File Format",
  "description":"Learn about ABA file format and APIs that can create and open ABA files.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
    }
  },
  "lastmod" : "2121-03-24"
}

## What is an ABA file?

A file with .aba extension is an Australian Bankers Association (ABA) or the [Cemtext](https://www.cemtexaba.com/) file format that is used by banks for batch transactions. It is used by most of the Banks for financial record keeping. Also known as a Direct Entry file, the ABA file format has been adopted by most of the Australian banks as default format for batch transactions. It has still not beed recognized as Standard format despite the fact that it has been in use by Bank of Queensland, NAB and Westpac. ABA files can be opened with any text editor such as Notepad++.


## ABA File Format

An ABA file uses the ASCII format to store data for forwarding or loading in to banking systems. The format has been kept simple to make it easy for integration into companies own financial system to process batches of transactions. For example, in a payroll system, a batch of transactions can be uploaded to be processed in one hit. The ABA file format specifications are available as full transcript on the [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) website and can be referred to for developers reference.

An ABA file consists of multiple lines where each line is known as a `record`. There are three main records in an ABA file:

 * Descriptive Record
 * Detail Record
 * File Total Record

### Descriptive Record

A `Descriptive Record` contains information such as Reel Sequence Number, Name of User's Financial Institution, Name of Use supplying file, and other information.

### Detail Record

The `Detail Record` type includes information such as Bank/State/Branch Number, Account number to be credited/debited, Indicator, Transaction Code, Amount, and other information.

### File Total Record

The "File Total Record" type includes Record Type 7, BSB Format Filler, File (User) Net Total Amount, File (User) Credit Total Amount, File (User) Debit Total Amount, and other information.

### Transaction Codes

A list of valid transaction codes is as follow. Most of the time, the code "53 - Pay" is used in ABA files. These transaction codes span debits, credits, and withholding taxes.

|Code|Transaction Description|
---|---|
|13|Externally initiated debit items|
|50|Externally initiated credit items with the exception of those bearing Transaction Codes|
|51|Australian Government Security Interest|
|52|Family Allowance|
|53|Pay|
|54|Pension|
|55|Allotment|
|56|Dividend|
|57|Debenture/Note Interest|

## ABA File Example

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## References

* [Cemtext ABA](https://www.cemtexaba.com/)

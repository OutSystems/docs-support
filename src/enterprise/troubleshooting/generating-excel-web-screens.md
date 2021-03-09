---
summary: 
---

# Generating Excel files from web screens by renaming the file

## Introduction

Generating complex Excel files (with styles) is not natively possible using OutSystems Platform primitives. The only primitive available out of the box is [RecordListToExcel](http://www.outsystems.com/help/ServiceStudio/9.1/index.htm#t=Designing_Actions%2FExport_to_MS-Excel_a_Record_List.htm), which generates files with plain formatting (default styles, no colors, etc).

An alternative widely promoted through the internet is "hacking Excel" by serving it an HTML page. Excel has been able to open HTML files for a while, and it tries to convert the HTML page to Excel. Additionally, by saving an Excel file with .XLS extension, Excel is forced to open it by the operating system. This is usually considered a [*quick and dirty*](http://www.glump.net/howto/web/serve-html-as-an-excel-file-from-a-web-application) way to implement an Excel export, easily.

As with any *quick and dirty* approach, problems may (and will) arise. 

## The problem

Problems related to the use of this pattern may come in (at least) two flavors:

1. Evolution of Excel

2. Evolution of the OutSystems Platform

### 1. Evolution of Excel

Since the file is not exactly an Excel file, Excel may choose to treat it differently from a proper Excel file. With evolution, Excel may treat such files differently (e.g. for security purposes).

This may lead (and has lead in the past) to files no longer opening in newer versions of Excel, opening with security or corruption warnings, or simply displaying wrong content.

### 2. Evolution of the OutSystems Platform

The OutSystems Platform itself evolves, and with it evolve the way the platform generates HTML files. If your Excel is being generated from a web screen, changes to the HTML in it may occur with every upgrade or even update / revision patch. This may lead, again, to the same problems in the previous section: files that no longer open, with security or corruption warnings, or that display wrong content.

Additionally, the behavior of Excel itself may not be consistent throughout the experiences. For example, embedded file opening in Internet Explorer may show different behaviors than when the file is opened directly in Excel; may depend on the security settings of Internet Explorer, any group policies, etc.

## Solving it

To properly solve this problem, one must steer away from generating Excel by using HTML files. If the built-in primitive is not sufficient for the business needs, the alternative is building an Extension to integrate with a proper API to build Excel files.

An obvious suggestion would be using Microsoft's API ([https://msdn.microsoft.com/en-us/lib.../bb448854.aspx](https://msdn.microsoft.com/en-us/library/office/bb448854.aspx)). Also, a number of commercial or free libraries exist for the same purpose; the [OfficeUtils](https://www.outsystems.com/forge/component-details/687/OfficeUtils/) component in the Forge can be used as a starting point for implementing such an integration - it was built using NPOI 2.2.1 (.NET stack) and Apache POI 3.7 (Java stack).

Using this quick & dirty approach may be legitimate if you have a controlled environment, or for a quick proof of concept.

Tactical solutions between the quick & dirty and the proper solution can involve "fixing the symptom" (e.g. find specific patterns in the page's HTML that cause a problem and fix them before exporting the file), but should be seen as temporary.


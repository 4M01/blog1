---
title: "Types of An API"
date: 2020-12-26
tags: ["API","Types of an api","Rest API","API Testing"]
draft: false
author: "Amol Chavan"
socialshare: true
---
# Types of an API

   In the last [post](https://amolchavan.space/post/api/what-is-an-api/), we covered [what is an API](https://amolchavan.space/post/api/what-is-an-api/) and why we need an API. 
   
   In this post, we will cover how API generally get classified based on their usage and release policies.

## Types of API based on Usage:
<br>
### 1. Libraries and frameworks as APIs

API for an object-oriented language, such as Java, would provide a specification of classes and its class methods. Java SDK also provides lot of API that one can use to build the applications. Selenium Library provides an API for browser automation. The API describes and prescribes the "expected behavior" (a specification) while the library is an "actual implementation" of this set of rules. A single API can have multiple implementations (or none, being abstract) in the form of different libraries that share the same programming interface.

We can import the `java.time` package to work with the date and time API. The package includes many date and time classes.

```visual-basic
import java.time.LocalDate; // import the LocalDate class

public class Main {
  public static void main(String[] args) {
    LocalDate myObj = LocalDate.now(); // Create a date object
    System.out.println(myObj); // Display the current date
  }
}
```

### 2. Operating systems APIs
An API can specify the interface between an application and the operating system. Windows OS provides COM API for WMI and for VBScript

```visual-basic
' List Physical Memory Properties

On Error Resume Next

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colItems = objWMIService.ExecQuery _
    ("Select * from Win32_PhysicalMemoryArray")

For Each objItem in colItems
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection
Next
```

Output:

>Microsoft (R) Windows Script Host Version 5.812

>Copyright (C) Microsoft Corporation. All rights reserved.

>Description: Physical Memory Array

>Maximum Capacity: 33554432

>Memory Devices: 2

>Memory Error Correction: 3

>***** script completed - exit code: 0 *****

<center>![Windows native OS - COM-API Example](/Types-of-An-API/Windows native OS COM-API Example.png)_Windows native OS - COM-API Example_</center>

### 3. Remote APIs

Remote APIs allow developers to manipulate remote resources through protocols, specific standards for communication that allow different technologies to work together, regardless of language or platform.

For example, the Java Database Connectivity API allows developers to query many different types of databases with the same set of functions.

<center>![Java Database Connectivity API](/Types-of-An-API/Java Database Connectivity API.png)_Java Database Connectivity API. Source: javaguides.com_</center>

### 4. Web APIs

A Web API is an application programming interface for either a web server or a web browser. It is a web development concept. <span style="background-color:yellow">**In a generic sense, an webservice IS a API over HTTP. They often utilize JSON or XML, but there are some other approaches as well.**</span>

<center>![Example of Web API/Untitled%202.png](/Types-of-An-API/Example of Web API.png)_Example of Web API. Source: tutorialsteacher.com_</center>

## Types of API based on release policies:

#### Private:
The API is for internal company use only.


#### Partner:
 Only specific business partners can use the API. 
 
 **For example**, vehicle for hire companies such as Uber and Lyft allow approved third-party developers to directly order rides from within their apps. This allows the companies to exercise quality control by curating which apps have access to the API, and provides them with an additional revenue stream.

#### Public: 
The API is available for use by the public. 

**For example**, Microsoft makes the Windows API public, and Apple releases its API Cocoa, so that software can be written for their platforms. Not all public APIs are generally accessible by everybody. For example, Internet service providers like Cloudflare or Voxility, use RESTful APIs to allow customers and resellers access to their infrastructure information, DDoS stats, network performance or dashboard controls. Access to such APIs is granted either by “API tokens”, or customer status validations.

<hr>

Now, that we have covered basics of APIs, we will dig deeper in next post about Web APIs and REST APIs.

Cheers!
---
title: "What is An API"
date: 2020-12-11
tags: ["API","What is an api","Rest API","API Testing"]
draft: false
author: "Amol Chavan"
socialshare: true
---
# What is an API?

In this post, we will cover what an API is with simple everyday examples that will help you to relate and recall this concept anytime. 

You will also understand:

1. What is the use of an API? 
2. What are the examples of an API?

    

This post focuses on the general term API and not on webservices or REST API . Here is the outline of the article.
### Table of Contents
1. [An Application](#Application)
2. [An Interface](#Interface)
3. [Application Interface](#ApplicationInterface)
4. [API: Context about Programming](#APIcontext)

## API - Application Programming Interface

You may already know the acronym of API, but do you understand all those terms?  I'll explain each term, not in the same order.

## An Application <a name="Application"></a>
- What does an application mean to you?
- What kind of picture comes to your mind while using this word?

Application is nothing but any program running [or you can run] on a computer. In turn, a program is nothing but a set of instruction given to a computer in a language that computer understand to perform some task. This is almost true and you can imagine <span style="background-color:yellow">**task manger and each processes running on a computer as an applications.**</span>

You are reading this post in a browser running on the computer or mobile [also small pc], the browser is an application.

You can divide applications into various categories depending upon the criteria. Simple classification criteria we can use whether the application is a desktop-based app [aka native app] like a browser, Microsoft paint, excel or browser-based apps like YouTube, Twitter or CITI  bank application that you use to transfer the fund.  

- In case of **Web Application**, though you are using it in a browser, you are just accessing it through the browser, the application runs on some another machine[called as a server]
- The **Desktop application** runs on your machine and you can close at any point of a time [most of] unlike a web-application which you stop using for yourself but it keeps running on the server.

<center>![Examples of Desktop Applications & Web Applications](/What-is-an-API/ExamplesOfDesktopApplicationsWebApplications.png)_Examples of Desktop Applications & Web Applications_</center>

***Examples of Desktop Applications & Web Applications***

Applications can also be divided into other categories depending on their intend and use.

1. **Efficiency**:

    <ins>Example:</ins>  Phone banking app.

2. **Communication/Collaboration:**

     <ins>Example:</ins> Whatsapp

3. **Information Distribution:**

     <ins>Example:</ins> New York post website

4. **Fun:**

     <ins>Example:</ins> Games

You can group most of the apps in one or more categories mentioned above. An application can belong to multiple groups.

<center>![Applications categories depending on their intend and use](/What-is-an-API/ApplicationsCcategoriesDependingOnTheirIntendUse.png)_Applications categories depending on their intend and use_</center>


I hope this gives you context about the term application, we will also try to group application using one more criteria in the latter part.

## An Interface <a name="Interface"></a>

let's try to understand interface as a general term, afterwards we will use it from the context of computing.

<center>![Bing Search results for term Interface](/What-is-an-API/BingSearchresultsfortermInterface.png)_Bing Search results for term Interface_</center>



<p>An interface is something with which we interact as a user.</p>


<center>![Interface Example - Electric Switch](/What-is-an-API/InterfaceExampleElectricSwitch.png)_Interface Example - Electric Switch_</center>



Everyday, we interact with electric switches which are great examples of an interface.

Essentially,  using electric switch you just close the circuit.

<center>![Example Open and Close Circuit](/What-is-an-API/ExampleOpenANDCloseCircuit.png)_Example Open and Close Circuit_</center>


1. In case of electric switch, you know how to use it.  But you don't need to understand how it works - it just gets your work done - light up the bulb.
2. Also how it is designed and implemented is up to the vendor, you have been provided with the common understanding of how to use it.
3. It can have different form and do the exact same thing or have a different form for a different objectives. In Example, image above of electric switch, You can have it for electric socket

## Application Interface <a name="ApplicationInterface"></a>

Now, let's try to understand the interface from the computing perspective. 

Earlier, we categorized applications using criteria as kind of applications(web/native) and purpose of an application.  Now, let's categorized application from perspective how end-user consumes application, how one interacts with the application:

<center>![How end user interacts with applications using GUI & CLI](/What-is-an-API/HowEndUserInteractsWithApplicationsUsingGUI&CLI.png)_How end user interacts with applications using GUI & CLI_</center>



In computing, the <span style="background-color:yellow">**Interface is something we use to exchange the information with an application**</span> or in some case libraries which may not be running until you run it. 

1. **Graphical User Interface (GUI):**

    A GUI is a system of interactive visual components for computer software. According to [wiki](https://en.wikipedia.org/wiki/Graphical_user_interface) -

    > The graphical user interface is a form of user interface that allows users to interact with electronic devices through graphical icons and audio indicator such as primary notation, instead of text-based user interfaces, typed command labels or text navigation.

    Example : Google Search. You are provided with Text Box were you type-in your query and hit on Search Button or hit/tap on Enter/Search Key. Everything is intuitive for end user and using GUI you exchange information with Application. More than 99.9% of applications are created for end user are GUI application

2. **Command Line Interface:**

    Terminal or Command prompt like applications where user exchange information through series of text command provided by application. According to [wiki](https://en.wikipedia.org/wiki/Command-line_interface) - 

    > A command-line interface (CLI) processes commands to a computer program in the form of lines of text. The program which handles the interface is called a command-line interpreter or command-line processor

    Example : [curl](https://curl.se/) - exchange of information over multiple protocol.

Application like git client does provide both GUI and CLI so that user can use any kind of exchange he/she  prefers. 

## API: Context about Programming <a name="APIcontext"></a>

All the applications created to do information exchange because they are created with the one of the intent mentioned earlier.  In a way, it is required to have at least one kind of interface available so information exchange happens. We went through the two kind of interfaces in previous section. Let's discuss about API.  **APIs are developed so they will get consumed in some of the program(s) as per the need. APIs, almost all the time, are never meant for end user interaction.**

From [MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction)

> Application Programming Interfaces (APIs) are constructs made available in programming languages to allow developers to create complex functionality more easily. They abstract more complex code away from you, providing some easier syntax to use in its place.
As a real-world example, think about the electricity supply in your house, apartment, or other dwellings. If you want to use an appliance in your house, you simply plug it into a plug socket and it works. You don't try to wire it directly into the power supply — to do so would be really inefficient and, if you are not an electrician, difficult and dangerous to attempt.

<center>![Electric Plug as an example of the API](/What-is-an-API/ElectricPlugAsAnExampleOfTheAPI.png)_Electric Plug as an example of the API_</center>

Let's go through the examples -

**1. Java Time API** 

We can import the `java.time` package to work with the date and time API. The package includes many date and time classes.

```java
import java.time.LocalDate; // import the LocalDate class

public class Main {
  public static void main(String[] args) {
    LocalDate myObj = LocalDate.now(); // Create a date object
    System.out.println(myObj); // Display the current date
  }
}
```

**2. Simple VBScript**

Open Notepad, copy and paste one line mentioned, save it as `vbs` file and click on it.

```visual-basic
MsgBox "Hello World"
```

**3. Browser Extensions**

FireFox Browser is native app and it does supports extensions ecosystem through [JavaScript API](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API).

With just two files and few lines of code, you can [create the working extension](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension) and it is possible because browser as native app provides API which anyone who knows JavaScript can use to consume in his/her program and can extend the functionality of the browsers.

Developer can extends browser features in multiple different way and that is reason for so many different extensions to exist but as standard API Browser decide what information exchange can happen with browser application through this API and developer who are using this API don't need to understand underlying working of the browser. Browser also don't need to understand how this APIs are going to use in other programs.

Example: [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) is one of my favorite extension but there are [tons of an extensions](https://addons.mozilla.org/en-US/firefox/) which extends functionality of the browsers.  

JIRA Plugins system also uses API - to create extensions like [zephyr](https://www.getzephyr.com/) & [X-Ray](https://www.getxray.app/)

4**[. IFTTT](https://ifttt.com/)**

API provides way to integrate applications together. 

Example: One can save every email received on GMail to Dropbox because both of this applications provided the API or one can revive text message if he gets an email by using GMail API and Twilio API. It is easy to integrate the apps if required APIs are provided and then there are service providers like [IFTTT](https://ifttt.com/) and [Zapier](https://zapier.com/) who can also help to create workflows on this API.

It's apparent from above examples, what API's can be used for

1. As building block while creating applications.
2. Using Existing application as a block.
3. Extend the functionality of an application by building on top of it.
4. Integrating  multiple applications together.
5. Hiding information and allowing to interact with limited application for information exchange.

Hope this helps.

Cheers!

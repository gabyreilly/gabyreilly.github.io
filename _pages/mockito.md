---
title: "Mockito in Java - Workshop"
layout: single
permalink: /mockito
author_profile: true
toc: true
toc_icon: laptop-code
---
## Intro

Unit testing is an important step of software development, especially when a program will evolve and change over time. In this hands-on workshop, we will write unit tests for a small Java program using JUnit and Mockito. We will discuss how to make a program "testable", how to use mocks and assertions, and share tips for debugging. This workshop is appropriate for any developer interested in unit testing, and especially those comfortable with Java concepts.

## Sign up

* Jan 22nd 2020, 2pm-4pm - Airship employees only, join #mockito-workshop in slack
* Date TBD, February 2020 - [WWCode Portland](https://www.womenwhocode.com/portland/events), full link TBD

## Setting up your computer for the workshop

Our main setup steps are:
* Install Java
* Install IntelliJ
* Install Git
* Open sample code from [https://github.com/gabyreilly/mockito-workshop](https://github.com/gabyreilly/mockito-workshop)

Screenshots will be taken from my Mac, but check for links to Windows and Linux instructions.



## Install Java

Start by opening a terminal (on Mac, open the Terminal app)

Copy or type the command:

```
java -version
```

If your version is 8 or higher, you can skip these steps.

{: .notice--info}
Note: If you have a higher version of java on your machine but want to change to Java 8 for the workshop,
you can set the explicit version with this line in your ~/.bash_profile or ~/.zshrc : 
 `export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)`


### Download Java 8 JDK

[Oracle JDK Download Link](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

Accept the license agreement and choose the appropriate download for your system:

![Accept License from oracle before downloading](/assets/images/workshop-install/accept-oracle.jpg)


You will need to make an Oracle account in order for the download to start.
[Create Oracle account](https://profile.oracle.com/myprofile/account/create-account.jspx)

### Install Java 8 from the bundle you downloaded

Open the bundle and install Java using the provided wizard.

### Set `JAVA_HOME` environment variable

Setting this environment variable depends on which version of the shell your system uses. 

#### Mac OS
Newer versions of Mac OS use zsh shell, while older versions use bash.

To figure out which shell you are using run this command:

    echo $SHELL


**If your shell is `/bin/zsh`**, run this command:

    touch ~/.zshrc & open ~/.zshrc

Then paste in this on its own line:

    export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)

and save the file.  After saving, close your terminal window and open a new one.

**If your shell is `/bin/bash`**, run this command:

    touch ~/.bash_profile & open ~/.bash_profile

Then paste in this on its own line:

    export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)

and save the file.  After saving, close your terminal window and open a new one.

#### Confirm JAVA_HOME is saved

In the new terminal window, run the command:

    echo $JAVA_HOME
	
It should output the path like:

![/Library/Java/JavaVirtualMachines/jdk1.8.0_231.jdk/Contents/Home](/assets/images/workshop-install/echo-java-home.jpg)

#### Other systems
Follow the directions from this link: [Tutorial from Baeldung](https://www.baeldung.com/java-home-on-windows-7-8-10-mac-os-x-linux)

### Confirm Java version

In a terminal window, type the command:

```
java -version
```

Sample output:

![Successful response of java -version](/assets/images/workshop-install/java-version-8.jpg)

----

## Install IntelliJ

Download IntelliJ Community Edition

[IntelliJ Download](https://www.jetbrains.com/idea/)

Install IntelliJ from the bundle you have downloaded.

Installation recommendations:
* You do not need to import settings, just start fresh
* In general, keep the defaults as recommended by IntelliJ
* If you do not want all the default plugins, you can turn them off, but our demo will require
 Build Tools -> Maven and Test Tools -> JUnit


![All plugins enabled](/assets/images/workshop-install/intellij-plugins.jpg)

----

## Install git

In a terminal window, check to see if you already have git installed. 

	git --version

Any version will work.

If you do not have git installed, follow instructions for your system on this [Git-SCM tutorial](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Download our workshop's sample code

In a terminal window, clone our sample repo:

    git clone https://github.com/gabyreilly/mockito-workshop.git

This will create a folder named mockito-workshop

Then, you can open the project in IntelliJ with the following steps:

On the Welcome to IntelliJ screen, click "Open".

![Click "Open" from the welcome screen](/assets/images/workshop-install/intellij-welcome.jpg)

Navigate to the mockito-workshop folder and click Open. (You don't have to click on any files inside the folder -- just open the folder itself)

![Open mockito-workshop folder](/assets/images/workshop-install/intellij-nav-finder.jpg)

It will take IntelliJ a few minutes to get everything set up, but once it's done, it should look like this:

![Project loaded in IntelliJ](/assets/images/workshop-install/intellij-loaded.jpg)


You can click the arrows to expand the various modules and explore:

![Module expanded in IntelliJ](/assets/images/workshop-install/intellij-expand.jpg)

## Workshop slides
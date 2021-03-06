<!--
title: "Running Contrast on an IntelliJ Application"
description: "Overview of the process for installation of Contrast on an application using IntelliJ"
tags: "java agent installation IntelliJ IDE"
-->


Use the following instructions to add the Contrast agent to an application using IntelliJ IDE's supported application servers.

## Before You Start

[Download and install the Java agent](installation-javastandard.html) from Contrast before proceeding with the **Configuration** instructions.

## Configuration

* Click on **Run** in the application toolbar, and then click on the **Edit Configuration** menu item from the dropdown.

<a href="assets/images/KB2-f04_1.png" rel="lightbox" title="Edit Configuration"><img class="thumbnail" src="assets/images/KB2-f04_1.png"/></a>

* Select the IntelliJ Server configuration instance.
* Select the **Server** tab, and enter the Contrast launcher string in **VM Options**: `-javaagent:${DOWNLOADS}/contrast.jar -noverify`.

<a href="assets/images/KB2-f04_2.png" rel="lightbox" title="VM Options"><img class="thumbnail" src="assets/images/KB2-f04_2.png"/></a>

* Click **Apply** and then **OK**.
* Start the **Server**. 
* A Contrast startup message should appear in the **Server** console. (Allow one to two extra minutes for server startup.) 

<a href="assets/images/KB2-f04_3.png" rel="lightbox" title="Startup Message"><img class="thumbnail" src="assets/images/KB2-f04_3.png"/></a>

* Navigate to your application and allow an extra minute for it to start up. 

## More Information

[Running Contrast on GlassFish with IntelliJ](installation-javaserver.html#glass)

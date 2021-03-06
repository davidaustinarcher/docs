<!--
title: "Contrast 3.6.10 - November 2019"
description: "Contrast 3.6.10 November 2019"
tags: "3.6.10 November Release Notes"
-->

## Bug Fixes

* The Flow Map interactive application view didn’t work in older IE11 browsers and had some minor formatting issues.

* Drilling down on an Assess rule to see all apps that use the rule would cut off results at the first screen.

* Protect suppressed incorrect attack events after creating an exclusion. (We fixed this by adding an option to suppress events in an improved Create Exclusion workflow.) XXE attack events showed incorrect and confusing details in the attack event overview.

* Libraries showed incorrect total vulnerabilities counts for CVEs. Users could not override a Library policy at the organization level.

## New and Improved Features

* Jira integrations have a new **application importance filtering option** that tells Contrast to only create tickets for vulnerabilities from applications that have a specific importance level.

* It’s now possible to **search for vulnerabilities by Application Tag**, both through the Contrast UI and the API. A new filter option in the Vulnerabilities view makes it easier to find vulnerabilities by topics that are relevant to your teams.

* We support **.NET Core applications deployed on Linux.** We’re expanding our coverage of .NET Core applications from Windows to include Linux deployments. You can now use the same .NET Core agent and gain accurate and detailed security coverage on your application.

* Integrations with **Azure Pipeline can now allow development teams to set vulnerability thresholds** that prevent builds from succeeding if applications exceed thresholds and are too vulnerable.

## Agent Updates

### Java summary

The Java team worked to **improve accuracy in Assess** for this release in these areas:

* Detecting XSS attacks on Java Servlet applications

* Detecting SSRF attacks

* When using Java 11

The team also made **improvements for reporting and troubleshooting,** as well as smaller bug fixes. These include:

* Clarified usage of the *max_stack_depth* property and improved reporting of the error that occurs when it is misconfigured.

* Added a heartbeat message to help administrators diagnose Contrast Protect syslog connectivity.

### .NET agent summaries

The team **improved sensitive data masking** for cookies and assured **higher accuracy for Path Traversal rules** in Protect. 

#### .NET Framework 

The team **improved route-based coverage** across the board to more accurately discover and observe routes for different routing configurations. They also fixed the following bugs:

* Error logging bug when the agent had a problem discovering applications hosted on IIS

* The agent could produce an invalid IL code for applications that were re-deployed dozens and dozens of times without a server restart.

#### .NET Core

The Contrast .NET Core agent now supports Linux (Ubuntu, Debian, openSUSE)! See https://docs.contrastsecurity.com/installation-netcoresupport.html 

The team also added a feature to capture and report the HTTP POST body for vulnerabilities and attacks.

### Node.js summary 

The Node team is pleased to announce **full support for NodeJS** version 12 LTS.

The team also implemented **route-based auto-verification** (RBAV) functionality for the agent. RBAV will be fully released and functional when our main products also complete server implementation for route-based auto-verification.

We fixed how Assess reports relevant findings from malicious cookies for the Koa framework.

### Ruby summary 

The Ruby team focused on **language compatibility** to ensure the agent adheres to best practices and works alongside common dependencies. In particular, the team addressed an incompatibility with FactoryBot, allowing the agent to run with the gem installed. The team also fixed an incompatibility with the 2.6 base image on Heroku, so the agent can once again be installed in that environment.

In addition, updates to Contrast Service runner assure startup in all supported installations, as well as improved interoperability for applications running in multiple processes.

The team also implemented route-based auto-verification (RBAV), slated for full release later this year.

### Python summary

The Python team released the Python Assess beta and continues to add features and stability improvements. 

The team also improved the agent’s SQLAlchemy support and request body handling. The agent now logs its configuration and log file locations to stdout on initialization. The team fixed several issues surrounding its communication with the Contrast Service, enabling the agent to use the latest version of the Service (2.3.0) by default.

Additional improvements include PyCassa support for SQL injection and updates to internal testing and packaging.

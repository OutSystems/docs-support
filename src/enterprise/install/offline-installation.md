---
summary:
locale: en-us
guid: 900d27aa-ee3c-496d-a216-229c64a4d604
---

# Offline Installation of the OutSystems Platform

## Overview

In some customers with stricter security policies it may happen that you wish to install the OutSystems Platform on a machine without Internet access. This is always possible to do, provided you are able to access the Internet in some other way to obtain the required files and transfer them to the target machine.

This article will provide detailed information on how to do this in all OutSystems Platform stacks.

I would like to note that this configuration is simpler in some application servers than others. Notably, it's considerably more complex when using JBoss EAP than most of the other application server options currently available.

## .NET / IIS

The usual way to install the OutSystems Platform on the .NET stack should already be applicable to an offline scenario, as you are required to download the Platform Server and Development Environment binaries and install them locally.

Regarding the prerequisites installation you'll need to be able to add or remove features from Windows in an offline manner. This can be done using the installation media, or by other standard means.

## Java / Generic

In Java / Linux installations the difficulty lies primarily in that the yum tool used for package management is a primarily online tool. Most organizations who employ offline installation of their machines will keep a mirror repository of their Operating System of choice and use that instead of the online ones.

The OutSystems Platform itself is also distributed through a standard [yum repository](http://yum.outsystems.net/9.1/), so you can mirror that one on your internal network.

The major difficulty lies with the third party libraries which are required by the OutSystems Platform but that we cannot distribute due to licensing. This affects specially the Java SDK and most of the application servers used by the OutSystems Platform.

You can obtain the libraries required by the platform in the following locations:

* [ant](http://ant.apache.org/bindownload.cgi)

* [java sdk](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

* [Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html)

In all application servers, if you're doing an offline installation, the step to add the OutSystems Platform yum repository is not required.

## Java / Wildfly

In order to do an offline installation of the OutSystems Platform using the Wildfly application  server:

* download Wildfly from [here](http://wildfly.org/downloads/)

* Install the following rpm packages from the OutSystems yum repository

    * wildfly8

    * platform

    * libs

Java / Weblogic

In order to do an offline installation of the OutSystems Platform using the Weblogic application server:

* download Weblogic from [here](http://www.oracle.com/technetwork/middleware/weblogic/downloads/wls-main-097127.html)

* Install the following rpm packages from the OutSystems yum repository

    * weblogic

    * platform

    * libs

## Java / JBoss EAP

The OutSystems Platform in JBoss EAP only supports the rpm mode of installation. This means that you'll need to be able to obtain the jboss package and its dependencies in order for the OutSystems Platform to be installed.

This complicates matters a bit more as JBoss and its dependencies can be over 100 packages. The OutSystems Platform, after installed, can  operate offline. One option is to enable internet temporarily just for the installation of the OutSystems Platform. If this is not possible, several other approaches are possible

* Set up a different machine with internet access to act as a proxy for the yum installation. This is probably the simplest way to achieve this.

* Set up a machine with the same configuration as your offline machine with internet connection. Install the platform there and either use a tool like [yumdownloader](https://access.redhat.com/solutions/10154) to just obtain the necessary files or install the platform normally and obtain the necessary files from the yum cache.

* You can download the files one by one from the JBoss repositories and then install them on the target machine. The OutSystems Platform defines the following dependencies, which you'll need to download all the dependencies of, and etc:

    * bash >= 3.2

    * iptables >= 1.3.5

    * zip >= 2.31

    * unzip >= 5.52

    * jbossas-product-eap >= 7.5.0

    * jbossas-standalone >= 7.5.0

    * jbossas-domain >= 7.5.0

    * jbossas-hornetq-native >= 2.3.25

    * jbossas-jbossweb-native >= 1.1.32

    * jbossas-bundles >= 7.5.0

    * jbossas-appclient >= 7.5.0

    * jbossas-core >= 7.5.0

    * jbossas-modules-eap >= 7.5.0

    * jbossas-welcome-content-eap >= 7.5.0

    * dos2unix >= 3.1-0

    * patch >= 2.5.4-0

    * java-1.8.0-oracle-devel

You'll also need the following files from the OutSystems Platform repository:

* platform

* libs

* jboss6-eap


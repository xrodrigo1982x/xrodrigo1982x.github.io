---
layout: post
title:  Preparing your development environment
summary: A short tutorial on how to prepare your Java development environment         
categories: java jdk sdkman maven
---

No doubt the most (maybe the only) annoying thing about Java development is doing the whole preparation before doing the development itself.

Why? Because there are different versions, different distributors such as Oracle, Amazon, RedHat etc, there are free and non-free for commercial use, and the many other features.

We are going to stick to two distributions, first Oracle's OpenJDK and later GraalVM (many good devs say amazing things about it!).

<br/>

# Sdkman
Some years ago it was really annoying to configure a machine to develop in Java. 
But thanks to [Sdkman](https://sdkman.io/){:target="_blank", :rel="noreferrer"} it's much easier now!

Sdkman is a tool that helps to install development tools and more things related to Java development. 

[To install Sdkman follow this link](https://sdkman.io/install){:target="_blank", :rel="noreferrer"}

<br/>

Let's install the JDK for Java 14, which is the current version.  
So, to install JDK 14 is as easy as: 
> **sdk install java 14.0.2-open**
  
<br/>
Usually Sdkman sets the newly installed version as current, but just to be sure, use the following command: 
> **sdk use java 14.0.2-open**

This command is specially useful when you use different versions of Java for different projects. 

<br/>
To be sure the current version running is the chosen one:
> **java -version** \
> openjdk version "14.0.2" 2020-07-14 \
> OpenJDK Runtime Environment (build 14.0.2+12-46) \
> OpenJDK 64-Bit Server VM (build 14.0.2+12-46, mixed mode, sharing)

<br/>

Ok! Now you have a Java development kit, you can write code, but depending on the number of files your program has it becomes annoying.
That's why we install [Maven](https://maven.apache.org/){:target="_blank", :rel="noreferrer"}.  
Maven helps you compile and build Java projects. It also manages external libraries and frameworks you're going to use in your projects.   
<br/>
With Sdkman it's easy as:
> sdk install maven 3.6.3

<br/>

Verify it's installed:
> **mvn -version**  
> Maven home: /home/.../.sdkman/candidates/maven/current \
  Java version: 14.0.2, vendor: Oracle Corporation, runtime: /home/.../.sdkman/candidates/java/14.0.2-open \
  Default locale: en_US, platform encoding: UTF-8 \
  OS name: "linux", version: "5.4.0-45-generic", arch: "amd64", family: "unix"

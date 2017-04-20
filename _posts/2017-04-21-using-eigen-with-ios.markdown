---
layout: post
title:  "Using Eigen on iOS"
date:   2017-04-20 06:27:27 +0900
categories: iOS programming
---
Eigen is a collection of platform independent libraries for mathematical computations. It is popular because of being open-source, too. Developing OS X apps that use Eigen is straightforward. Just include the correct headers, and you are done.

However, things are not that easy when it comes to iOS apps. Several compiler errors have been reported.

The good news is, doing two things can fix most of these problems:

1. put #include directives relating to Eigen at the top of the program file.
2. under the Build Settings of the project, look for "C++ Language Dialect" and "C++ Standard Library" settings. Instead of "Compiler Default", you can selecting different settings. I do not want to suggest a particular setting because that might clash with other libraries that you have included.

---
layout: post
title:  "The legacy inception"
date:   2016-01-20 10:19:30 +0000
categories: 
---


The most part of the projects dealing with software development become legacy just about from the start. It happens over and over again even nowadays when the majority of software developers are more or less familiar with the concept of "legacy code" and claim to fight it using all possible best practices they know.

Let’s take a look at the two noticeable parts of any software project: business logic and third party tools. Sure, projects sometimes include other things like tests, build scripts, deployment configurations etc. But things that affect the project’s structure (or architecture for those who prefer to name it that way) are still only the business logic and third party tools like frameworks and libraries.

The situation with third party tools is pretty clear: usually there are a lot of documentation on websites of framework vendors, books, tons of answered questions and code examples on the stackoverflow. The approach here is: learn the tool and follow the rules it provides. Though it is still possible to misuse frameworks or copypaste some code from the stackoverflow without understanding of how it works and break some parts of the application, the way how third party tools are used is not what normally the problem is.

The next and the most important part of any software project is the business logic. This is the thing, that brings value to the project. This is the thing that covers needs of the business and solves its problems. And this is really essential, because we, developers, create software that solves problems, right?

But how the hell a developer can know details of how the business works? How can one can convert knowledge about the problem domain into bits and bytes without having a deep understanding about the subject? And that is now it starts...

We, developers, tend to underestimate the business domain complexity and thus not to handle it in the software design. And that is for many reasons: 
   
 * It is not our responsibility, to deal with it.
 * No need to understand it, we have a business analyst (product owner, domain expert, you name it).
 * We can just start coding and understand the problem on the way. If even the product owner can understand it, it can not be as hard...
 * Sometimes we work in parallel on many different projects and it is hard to wrap the head around many different problem domains. Context switching is painful.
 * Gathering new knowledge about the domain does not expand our technical skills and does not increase our value as professionals.

But the funny thing is: understanding the business domain is that what really matters! Because without deep analysis and understanding of the domain, application logic can not be designed in the way that reflects it.

One can say: “the project I work on is very small and does not really have any logic. It just takes data from the database and shows it on the screen.” And then implements is in terms of chosen frameworks’ concepts and rules without any structure, because why bother, right? And here we are: the business logic, spreaded as a thin layer over the whole application, gives us those legacy code we do not like to deal with.

And then one say: “It is still not bad, because the project manager said, that the application will be released and never ever changed in the future”. But all software projects, every single one of them, have one common thing: changes! There will be changes for sure! And it makes always sense, to dig into the problem domain and come up with a model, that is inline with business needs, so that understanding and changing existing software is not as painful any more.

Here is a list of things, which can help to build more structured and maintainable software:

 * Take systematically time to understand and deal with the problem domain.
 * Line up your domain model accordingly to the rules of the business.
 * Do not allow concepts and rules of third party tools you use to leak into your domain model.

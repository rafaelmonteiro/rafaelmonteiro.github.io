---
layout: post
title: "Microservices"
description: Is the end of monolithic structures?
headline:
modified: 2016-06-01
category: development
tags: [SaaS, microservices, API]
image:
  feature:
comments: true
mathjax:
---

## Introduction
Since the explosion of SaaS applications there have been a lot of innovation
in the area of APIs which provide an important interaction between application
functionalities.  

The main idea around microservices is that, in general, applications tends to
become easier to develop when they are treated as modules. Considering that,
each piece is developed separately, being the application a composition of all
parts working together. It opposes the traditional development where the
application is considered a 'monolithic' entity.  

That way, developers can focus on their own core business while other
specialists provide the components needed, which will be accessed through APIs.  

<figure>
	<a href="https://dzone.com/storage/temp/570495-slide1.png"><img src="https://dzone.com/storage/temp/570495-slide1.png"></a>
	<figcaption><a href="http://rafaelmonteiro.github.io/" data-toggle="tooltip"
    title="Monolithic vs Microservice">Monolithic vs Microservice</a>.
    </figcaption>
</figure>

## How it works
In general, a microservice provide an API endpoint commonly (but not
exclusively) through a stateless REST API which can be accessed via HTTP as a
traditional webpage. So, consuming those services is easy, as they only require
tools and methods that developers are already familiar with.

## Benefits
When applications components are splitted, development time is optimized as they
are produced concurrently.  Besides that, modules created with this thought in
mind are easier to be reused in other contexts/applications.  

Resilience appears as an additional advantage as components can be spread into
multiple servers or even various data centers. In case of a component failure,
you can quickly replace it while the rest of application can continue to work as
expected.  

Scaling become more efficient too, because you can focus on most demanding parts
rather than simply duplicating the entire application.

## Examples
There are several players in various areas, as one can see in the image below:

<figure>
	<a href="https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAg6AAAAJDYxZmU0OTEyLWNmZWItNGVlNS1iYTRiLTRiNjExYjk4MGNiNA.jpg"><img src="https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAg6AAAAJDYxZmU0OTEyLWNmZWItNGVlNS1iYTRiLTRiNjExYjk4MGNiNA.jpg"></a>
	<figcaption><a href="http://rafaelmonteiro.github.io/" data-toggle="tooltip"
    title="Microservices players">Microservices players (image by Menlo Ventures)</a>.
    </figcaption>
</figure>

## Conclusion
Microservices demands a conceptual change in IT departments towards a DevOps
culture, in which development and operations teams work aligned to support an
application through its lifecycle, and go through a fast or even continuous
release cycle rather than a traditional long one.

Though they are not a silver bullet, microservices must be considered when
architecting a new application or refactoring an old one.

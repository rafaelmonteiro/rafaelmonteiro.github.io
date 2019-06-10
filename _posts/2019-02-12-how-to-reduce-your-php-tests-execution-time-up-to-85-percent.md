---
layout: post
title: "How to reduce your PHP tests execution time up to 85%"
description: >-
  The solution relies on the use of ParaTest, a library that supports parallel
  testing in PHPUnit.
date: '2019-02-12'
categories: development
comments: true
keywords: [Testing, PHP, Software Development, Software Engineering, Improvement]
---

![Speedometer image from [Wikimedia](https://upload.wikimedia.org/wikipedia/commons/6/65/Speedometer_%28kmh%29.JPG)](https://cdn-images-1.medium.com/max/1600/1*e94W7J-gYa9LywIJr0sOyQ.jpeg)

Speedometer image from [Wikimedia](https://upload.wikimedia.org/wikipedia/commons/6/65/Speedometer_%28kmh%29.JPG)

We all know that a good test suite — unit and integration — is important to any application. We also know that running all our tests can take some time (especially in large projects). What one may not know is that is possible to reduce this time up to 85% (or even more).

In this post, I will show how we did this. Results may vary, but certainly you will notice a great improvement.

#### The Problem

In my squad’s current project, we have (at this time) a test suite with 345 scenarios (865 assertions). It was taking almost **4 minutes** to finish the whole execution.

During [Brayan](https://medium.com/@brayan.dichtl)’s researches, he found a package that could help us by reducing the time on this task. He thought it could be a good idea for a [Pet Project Day](https://theiconic.tech/how-we-exercise-creativity-on-pet-project-days-decbe31e265f) and I decided to help him on it.

#### The Implementation

The solution relies on the use of [ParaTest](https://github.com/paratestphp/paratest), a library that supports parallel testing in PHPUnit. So, instead of running just only one process, the idea is to distribute your tests into several different threads.

Even if you try the default usage (no additional parameters) you will be able to see some improvements already.

However, the real magic comes if you configure the _runner_ parameter, as explained in the ParaTest documentation:

> The default Runner for PHPUnit spawns a new process for each testcase. This provides the highest compatibility but comes with the cost of many spawned processes and a bootstrapping for each process. Especially when you have a slow bootstrapping in your tests (like a database setup) you should try the WrapperRunner with `--runner WrapperRunner` or the SqliteRunner with `--runner SqliteRunner`. It spawns one "worker"-process for each parallel process (`-p`), executes the bootstrapping once and reuses these processes for each test executed. That way the overhead of process spawning and bootstrapping is reduced to the minimum.

Besides that, you can tweak even more by changing the amount of processes created. The default is the number of logical CPU cores of your machine. You should take into account that each process generates some overhead though. That’s why you need to resist to the temptation of creating a massive number of threads.

Therefore, in our scenario, the optimal configuration was:

#### Results

By doing this, we’ve managed to achieve the following:

**Before**

![](https://cdn-images-1.medium.com/max/1600/1*o73kWMBn12zIKAoYETumng.png)

**After**

![](https://cdn-images-1.medium.com/max/1600/1*-Z6j2mQQ0kseE9PMYqzykQ.png)

Basically, we are **7 times faster** than before, or using just **14% of the original time**!

Isn’t that amazing?

An additional improvement is the reduction of memory usage as well (from 66MB to 34MB).

#### Conclusion

Less time during the build process means more efficient use of resources and a faster deployment. And all of it was achieved by simply installing a new package.

Do you have any other ideas on how to improve the build process? Let us know in the comments!

---
*This post was originally published on [THE ICONIC Tech blog](https://theiconic.tech/how-to-reduce-your-php-tests-execution-time-up-to-85-690f70e28d41).*

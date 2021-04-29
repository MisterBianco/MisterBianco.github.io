+++
slug="complexity_1"
title = "Software Complexity Pt 1"
description = "What is software complexity"
date = 2021-04-29T00:00:00+00:00
+++

# Why is software development so complex?

I was asked a variation of this question by a coworker this week, and he wanted a 
one sentence answer. 

After pondering for a bit I said:

> Marrying experience and assumptions of engineers to reality is a non-trivial task.

I firmly believe this to be true. However, I can't boil down the problem to such a small
pithy value statement and pretend it addresses the entirety of the issue. I believe that
the question is really asking "why does software become so complex?" Because, if it was 
simple we wouldn't have problems deploying it.

I don't imagine myself any sort of expert on the matter of software complexity.
I also don't claim to be any form of expert in software deployment or maintenance.
However, the best part of the internet is that we can all adding our burning
commentary on whatever subject we want. After all I can claim to be an expert in
the field of virology after 30 minutes of googling /s.

### What is software complexity?

> "Complexity" seems to be a lot like "energy": you can transfer it from the end-user 
> to one/some of the other players, but the total amount seems to remain pretty much 
> constant for a given task. -- Ran

We have developed models to calculate complexity as some sort of mathematical
function, as if complexity can be determined by tokenizing a source file. Methods like 
McCabe's complexity model (AKA cyclomatic complexity), Halstead's metrics, and the 
Maintainability Index. An issue with these models is that the more complex the problem, 
the more complex the solution. We can choose to use languages, tools, frameworks that
are expressive and powerful but these models tackle an impossibly difficult problem with
many facets. Now I am not arguing that use of these models is futile.
We have to be vigilant in how we design systems, and I have
a few things I watch out for when implementing solutions which I wish to discuss here.

##### Technical debt

As requirements surrounding software increases developers must begin to think
more earnestly about how their application is architected and if concerted efforts
are not made to ensure software complexity is addressed we develop a form of complexity
commonly referred to as "technical debt." Ward Cunningham, who coined the term Technical Debt,
stated:

> "Shipping first-time code is like going into debt. A little debt speeds development so
> long as it is paid back promptly with a rewrite. Objects make the cost of this transaction 
> tolerable. The danger occurs when the debt is not repaid. Every minute spent on 
> not-quite-right code counts as interest on that debt. Entire engineering organizations can be 
> brought to a stand-still under the debt load of an unconsolidated implementation, object-oriented
> or otherwise."

Look no further than LinkedIn, in an effort to get to market quickly sacrifices in quality were made.
Shortcuts that were never revisited and soon they were at a point that no product could be made
by developers without a high degree of stress that business systems would collapse. New feature
development would be frozen, and an initiative by the name project InVersion (clever) was started.
This project was a two-month freeze on new features while portions of their stack were more or less
rebuilt. Two months to address technical debt is a serious problem for any organization especially
when competitors are on your heels. 

We have developed methods and practices over the years to control technical debt. Each organization
and by extension their subunits, should find what works for them. I have found that taking Fridays 
as a day to pay back debt is a hugely beneficial exercise for nearly all organizations I have worked 
with.

##### Readability

Beyond just technical debt there are other metrics that contribute to complexity. For example;
general readability which includes convention, formatting, and style. Every organization should
come to agreement on certain conventions possibly even leaving it up to a tool to do the formatting
and styling for them. In python, we have a style guide called pep-8 which can be automatically applied
by editors or IDEs and we can leverage opinionated tools like [black](https://github.com/psf/black). 
The programming language Go actually (mostly) enforces their conventions at compile time which 
eliminates any arguing amongst team members or the need for additional tooling.

Picking proper names for variables, functions, and the like are very important. No developer can
hope to recall what a poorly named `x` variable is for after not touching the codebase for a week.
Similarly, we need to be succinct and expressive which is an extremely difficult task. We often joke
that the hardest problem is naming our variables. Just as `x` is a bad name so too is `iterator_variable`
in place of the (customary) `i` we often find in for-loops. Naming is an art and counts very strongly
when we consider readability.

My note on convention, the purpose of mastering any convention or rule is to know when to violate it.

###### Engineering

Over-engineering, or its inverse, under-engineering is the issue of not applying the
appropriate amount or engineering to a solution. 

I firmly believe that every developer has come across code like the following:

```python
def add(x: int, y: int) -> int:
    """
    Adds two integers
    
    @param: x int
    @param: y int
    @return int
    """
    return x + y
```

Almost everyone would agree the "complexity" of this code is low. The readability is 
relatively high. However, the code is over-engineered for the problem it is trying to solve,
and the comment on the function is useless. Engineers, especially less experienced ones can easily
complicate a solution.

### Closing

I feel this article is waxing long. I will do a second post on the matter and let this end where it is.

+++
slug="docs"
title = "Docs as code"
description = "code as code about code"
date = 2020-09-03T02:00:00+00:00
+++

## Prologue

If you haven't read my previous article about wikis you can do so [here](/posts/wiki)

## Documentation as code

There is hopefully a fairly obvious pattern in my posts, I am a religious believer in everything
as code. This is just the next installation in that series. 

Documentation as code is the idea that documentation should be kept close to the code and highly
visible. If you want to generate documentation for a project you can use a documentation generation
tool provided by the language like [nim's](https://nim-lang.org) nimdoc tool, pythons mkdoc or sphinx,
and there are others or you can use a static site generator like [hugo](https://gohugo.io/) or 
[zola](https://www.getzola.org/).

> This site uses hugo but zola is an equally great project.

## Benefits

You can now create processes around documentation such as blocking merging if docs arent updated. 

> We have a github action that labels merge requests that contain changes to docs and assign people 
> who understand our docs best, like our team leads.

Another benefit is if you ever have a technical writer they have the benefit of docs being close to 
the code. Not hidden in some forsaken wiki.

And my final benefit is that docs are just another deployable. Ideally, there would be some mechanism 
that when a change is made to documentation, the documentation is rebuilt and deployed. An easy 
deployment mechanism may be to have a github action that deploys your docs to a gh-pages branch. 
Either way, it should be automated and have its own deployments.

## Documentation as an artifact

when the organization is at a point where it is able or when you are building documentation for api's
it becomes imperative that your docs be versioned. I would make the case that a mechanism exists so that 
when your code is deployed so to is your documentation in away that is versioned and immutable.

- You could for example do a tagged release from the gh-pages branch. 
- Or save these docs in a versioned s3 bucket.

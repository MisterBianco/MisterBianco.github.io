+++
slug="wiki"
title = "Wikis aren't for humans"
description = "Wikis, where knowledge goes to die"
date = 2020-09-03T01:00:00+00:00
+++

# Wiki's where knowledge goes to die

I work at a company that makes use of confluent for wiki articles and 
I get told a lot when I ask questions that I need to "go read the wiki."
Which causes a sense of dread because when I search for information in the 
wiki I get the following:

    Search: pipeline webhook token

Results:
- ngp pipelines
- ngp fargate pipelines
- ngp v2 pipelines
- ngp pipeline - other
- pipelines in aws
- monorepo pipelines
- pipelines for polyrepos
- sonarqube in a monorepo inside a polyrepo in a mini repo in space

Which of these could possibly be the correct article?

    The answer? None of the above because it was a private doc for one team.

## Problems with wikis

#### Seperation from code

Typically, I know where to find the code related to a project much more likely 
than I am to know where the wiki pages are located. Wouldn't it just be easier 
to keep the docs close to the code? 

Seperating knowledge or information from the source of that knowledge only creates
gaps and serves to waste time. Funny how something meant to make a team more productive 
only serves to make the SDL slower.

#### Private wikis

I struggle to imagine a better way to create technical silos and knowledge gaps 
in an organization than to say, Team X manages Y process so they are going to hide
everything from you.

This knowledge silo is a Anti-DevOps practice.

#### Misery

You tell an engineer to go read the wiki and they can't find the right page and now 
you have made someone feel dumb. One of my mentors tells me "we are emotional beings,"
we need to be aware of how we make people feel. 

    Out of Date docs are ACTIVELY HARMFUL

#### Writing good docs are hard

I like the LeadDev channel and there is a talk from Beth Aitman that I really enjoy on 
[docs](https://www.youtube.com/watch?v=R6zeikbTgVc)

TL;DR

Tips:

- Start with what the reader needs to know
- Write less
- Outline first
- Rubber ducking works for docs
- Write readably
- Dont write documentation for documentations sake

## Solutions?

I am always frustrated to read a rant column that offers no suggestions or possible solutions
so please refer to my next [article](/posts/docs) to get my opinions on a solution. (Spoiler: it involves code).
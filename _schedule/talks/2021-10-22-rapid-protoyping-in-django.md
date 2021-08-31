---
abstract: Building a prototype in a weekend is the dream of startups and established
  business alike.  But if you cut corners and the product takes off, you will be stuck
  with your mistakes for years.  This talk will show you the tools and techniques
  to build a minimal-regrets rapid prototype in Django.
accepted: true
category: talks
date: 2021-10-22 10:00
difficulty: All
image: /static/img/social/presenters/benjamin-zags-zagorsky.png
layout: session-details
permalink: /talks/rapid-protoyping-in-django/
presenter_slugs:
- benjamin-zags-zagorsky
presenters:
- bio: Zags is the CTO of Zagaran, Inc., a contract software company.  He has led
    dozens of full-stack software development projects between both the private and
    public sectors.  Zags graduated from Harvard in 2012 with bachelor's and master's
    degrees in Computer Science.  He previously worked at Google, mentors for TechStars,
    and is a published game theorist.
  company: Zagaran, Inc.
  github: ''
  name: Benjamin "Zags" Zagorsky
  photo_url: ''
  twitter: ''
  website: https://zagaran.com
published: true
room: ''
sitemap: true
slides_url: ''
summary: ''
tags:
- prototyping
- architecture
- design
- best practices
- tools
title: Rapid Protoyping in Django
track: t0
video_url: ''
---

Building a usable prototype in a weekend is the dream of startups and established business alike.  This is the lean startup approach.  You have many ideas.  Not all of those ideas will work, and all of them take attention away from known ways of making money.  So, you need to validate those ideas as cheaply as possible.  This means you need to build MVPs (minimum viable products) as fast as possible.  But there is a danger; if you cut the wrong corners and one of these new products takes off, that MVP will be the seed for a massive product and you will be stuck with your mistakes for years to come.  This talk will show you the tools and techniques to build a rapid prototype in Django, as well as how to minimize regrets later.

Outline of talk:

# Introduction
* Who I am and why I'm giving this talk: I'm the CTO of Zagaran, Inc., a contract software company based in Boston.  We've build dozens of Django websites.  Many of our projects have started with building a prototype on a small budget, and Django is one of our favorite technologies for doing this.
* The lean startup approach: why you should do no-regrets rapid prototyping.

# Before you write code, know what you are building
* Do user and market research (many things have been built).
* MVP: the thing you're trying to do needs to be minimal.
* Write out the backlog.  The things you're not building yet affect what you are building now.
* Figure out all the details of what you are building.

# Key tools
* Django's model forms (minimizes boilerplate code for HTML form rendering and validation)
* django-crispy-forms (gives you out of the box styling of forms and more backend control over layout)
* django-environ (improved ability to configure environment variables)
* django-storages (production-grade seamless file storage)
* social-auth-app-django (makes oauth logins really easy)
* django-extensions (makes debugging much easier)

# Corners to cut
* Minimal CSS
* Minimal JS
* Ignore pre-launch migrations
* Use Simple Object-based Permissioning
* Use the Django Admin
* Use SQLite Locally

# No regrets
* Delete and remake migrations once you're done prototyping
* Use Platform-as-a-Service (production-grade minimal maintenance hosing; Heroku, Elastic Beanstalk + RDS, or Google App Engine)
* Override Django's user model
* Have your database model lean too-restrictive rather than too-permissive (it's much easier to drop constraints than add them)
* Have Django settings switch between using a file for local development and os.environ for production deployments
* Have error handling from the start (Sentry is a good example of production-grade plug-and-play error handling and also does JavaScript errors)
* Security best practices: have SSL from the start, make sure Django's CSRF is enabled, do not modify data through GET requests, do not use raw SQL, set your servers and database to automatically install updates (easy on IaaS), encrypt your database and file storage

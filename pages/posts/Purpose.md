---
title: Why I built this Website (Vercel)
date: 2022/4/01
description: How and why I built this website from a non-developer's perspective
tag: sales engineering, vercel
author: You
---
import Image from 'next/image'

Building a website nowadays can really be as hard or as easy as you want it.  There are plenty of free websites that you can utilize with visual editors that can empower any non-developer to build their own website and make it look pretty good too!

Even though there are a lot of easy ways for people without development backgrounds to build websites it can be a great exercise in trying to build one yourself by coding it out! Transparently, I am not a developer and have never built a web application before, but I did have a lot of fun building this website (even though it's not the fanciest or most feature-intensive website).  In this article I will try to outline some of my thought processes on how I built the website and why I choose the framework and approach that I did!

## What does your web application do? How does it work?

Simply put my website is just a showcase for both me as Sales Engineer as well as me as a person! I want to showcase some of my work experience as an engineer, my thoughts on professional topics (Sales Engineering, Vercel, Next.Js), and photos that I love to take while traveling (and with my dog)!

Since I do not come from a development background I wanted to see if I could learn how to put together a basic website that could potentially be used to showcase myself to prospective employers in the future!

## What was your process for setting up a project and deploying previews and your production site on Vercel? What’s your development workflow look like?

Vercel really makes setting up a project and deploying the actually application super easy! I can easily work from a [Vercel Template](https://vercel.com/templates), and automatically have that repository for that template created within my GitHub account.  Then from there I can easily clone the repository from GitHub to my local machine and start coding instantly!

Even as a non-developer, I can really appreciate how efficient and streamlined Vercel makes the whole development process.  From a development standpoint, I can easily start doing work on my application in a preview/staging branch on my VS Code and then push those changes to my corresponding preview/staging branch in GitHub. Vercel is also fully integrated with GitHub, so once those commits are in my preview branch in GitHub then those commits are also deployed to a preview branch within Vercel.  But as a developer, I don't even need to go to Vercel separately to view those changes! I can simply initiate a pull request within GitHub and once that request is created I can see a preview for the website in Vercel right in GitHub UI!

![Pull](/images/pullrequest.png)

I can easily view the pull request, preview the actual changes on the website, and merge the changes to main while spending most of the time on GitHub (except for clicking into the preview).  Once the changes are merged to main then Vercel will instantly detect that as well and deploy and build the site automatically!

Vercel makes the CI/CD process so easy! No more going having to write individual scripts (and bug-checking) to build and deploy your website/application as it goes through the development lifecycle!

## What kinds of technologies did you choose to create your web application, and why?

I choose to use Next.js (via Nextra Static Site Generator) to build the website for a few different reasons, which I'll list below.  I'll approach this discussion from the perspective of myself as well as the perspective of a developer building a web application for production purposes.

#### <u>1. Performance</u>
This is always top of mind for a casual user or a developer building any application.  No one likes the feel of a staring at a loading screen or having to wait before being able to interact with a website.  Next.Js is a great option for production level applications where performance comes top of mind.  It is a framework built on top of the React library that was a gamechanging library built to streamline creating user interfaces and frontend web development.

Next.Js adds on ***server-side rendering*** and ***static generation*** functionality on top of React that can greatly increase performance over React's client-side rendering.  When you think about this from the perspective of a company's website, performance makes a big impact on SEO as well as overall customer experience.  Customers nowadays have an incredibly short attention span and poor performance on a website will dramatically increase bounce rate. Poor performance also results in a hit to SEO, as a Search Engine crawlers do consider performance when evaluating SEO; this can result in a negative feedback loop on traffic to your website which can be really scary!  This makes Next.Js a gamechanger for production level websites for many eCommerce and Financial Services companies!

#### <u>2. Ease of use</u>
The [Nextra static site generator](https://nextra.vercel.app/) that is used to build my website supports Markdown and React components and has a very logical file-system based routing that makes it very quick and easy for a non-developer like myself to make a website.  Nextra uses MDX (Markdown Extended library), which allows one to use both Markdown and React components in the same file.  [Markdown](https://www.markdownguide.org/basic-syntax/) gives me the ability to shorthand creation of long pieces of content by removing the need to write out full html.  This makes it a lot easier for a non-developer to write out the code and subsequently troubleshoot as well! Being able to easily bring in React components in a .md or .mdx file also gives me the ability to add in additional complexity without needed, while also making it easy for me author content directly in code.

The file-system based routing also makes it extremely easy for me to build out individual pages and posts within the pages as well!

![Pull](/images/nextra_routing.png)

You can see in this image that I could simple structure the page layout of my website by creating .mdx files within the /pages/ folder and similarly I could make separate Posts within the Posts page by adding different .mdx files as well.  This is very intuitive and easy to pick up and makes building and scaling on the website much simpler.
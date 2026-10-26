---
title: 'Personal Blog Website Creation - Establishing a Digital Online Presence'
description: 'Building a lightweight, high-performance personal blog from the ground up using Astro, custom typography, and interactive UI'
pubDate: 'Oct 28, 2026'
heroImage: './Images/picoftheblog.png'
---

In an era dominated by algorithmic, personalized content that preys on every habit to serve you algorithmic content, establishing an independent space on the web has never been more relevant. To share technical projects, essays, and ideas without platform constraints, I set out to build a lightweight, high-performance personal portfolio from the ground up. 

While my minor *is* Computer Science, the University of Memphis does not count Web Design as part of the minor, and so I have never attempted to build a website. I found some very basic tutorials to begin on LinkedIn Learning through my institution, and through YouTube for the rest. Specific aspects are credited at the end of this post.

 For the core framework, Astro eventually became clear as the ideal choice. Unlike traditional heavy single-page applications, Astro compiles down to static HTML and ships fewer JavaScript packets to the client by default, resulting in super-quick page loads. Pairing Astro with Markdown content collections kept the process more streamlined, particularly as someone who is not familiar with either JavaScript or CSS.

True platform ownership extended directly into the design and codebase architecture. Rather than relying on the platform's default templates, I stripped away redundant files and opted to make customized versions of them myself. I started by pruning old header and footer components, and instead replaced them with my favorite color and my personal links. (My favorite is any kind of Green!) The index page was structured with a centered branded header and a responsive grid layout dynamically populated from Astro content collections and automatically sorted by publication date. This also meant that by default, the site could be edited almost seamlessly by just adding an md file to the coding environment and pushing it to the assigned GitHub repository.

In order to customize the entire site to my specific tastes, I did edit some specific items besides the default site layout. For the font, I converted a professional royalty-free font named "Stenz Graxon Pro Cool Fancy Design" into a WOFF2 font file, and sourced it for my posts. I added a scrolling effect to the top image using some very basic CSS tutorials, and even an expanding widget that links to my personal profiles from each individual post.

To maintain a streamlined publishing pipeline, the entire project updates near instantly after every editing session through a hosting service named Vercel. I chose Vercel for two reasons:
1. It updates quickly and efficiently
2. It has an infinite free tier, so the link will always work when provided

 All source code and Markdown posts are managed locally and pushed directly to a remote GitHub repository, automating compilation and live updates within minutes of them being published.

 Finally, I had a site that was easily manageable, expandable, and customizable, and I genuinely enjoyed looking at it!

 Widget Turtorial: https://www.youtube.com/watch?v=WVJLrbiMKhM

 Astro Core Tutorial: https://www.youtube.com/watch?v=F2pw1C9eKXw&list=PLoqZcxvpWzzeRwF8TEpXHtO7KYY6cNJeF

 HTML and CSS Tutorials: https://youtu.be/9z8FP8ear2Y?si=4kkPWhmN2K4kE_Um | https://youtu.be/FQdaUv95mR8?si=RUekMR2t7Fj4gfxw

(Linkedin Learning is a paid service) : https://www.linkedin.com/learning/

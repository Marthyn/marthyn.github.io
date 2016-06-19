---
layout: post
title:  "Joy of Coding 2016"
date:   2016-06-17
excerpt: "2017 was my second year of the awesome 1 day conference Joy of Coding. It inspired me a lot, here is a recap of the most interesting things I learned"
feature: https://pbs.twimg.com/profile_images/729906197051101184/YVr1ch75_400x400.jpg
tag:
- joyofcoding
- fun
- conference
comments: true
---

> Celebrating the art, craft, science and joy of software development

A conference not purely to learn something but to remember after many many busy weeks/months of programming that there's not only deadlines, demanding customers and frustrating problems to solve. Programming is joyful and we should have more fun with it!

For me this edition was as, if not more, inspiring as the last time. Last year it inspired me to develop a small <a href="{{ site.url}}/hubot-praise">Hubot plugin</a> because of a talk by Ben Straub! This year once again there were many fun and inspiring talks, here is a list of my favourites.

# [Philip Wadler](https://twitter.com/PhilipWadler)

Professor at Edinburgh university, a very very smart man. In the beginning I had quite a hard time following his talk on category theory. And I'd have trouble explaining to you what it is exactly. But it got my head churning and it was actually a great start of the day. It inspired me to read more into this category theory and in general to read more about origins of programming languages.

It also helped that he is witty guy and he dressed as Lambda Man!!
![]()

# [Corey Haines](https://twitter.com/coreyhaines)

Corey Haines started by stating that he didn't knew Prolog and so could we! His premise was that you should try and learn a new language every year, not for your job but purely for fun. This will open up your way of thinking and the way you solve problems.

Prolog is a very interesting language, it is not a functional nor object oriented but a logical language. The way it works he said was "You state facts and ask questions and the system will find facts that prove the questions to be true". So you don't make a function in which you tell the system how to find the right variables.

## Grandparents

For example the parent() and grandparent principle.

```prolog
parent(david, john).
parent(jim, david).
parent(steve, jim).
parent(nathan, steve).

grandparent(A, B) :-
  parent(A, X), parent(X, B).
```

You state that david is the parent of john and jim the parent of david. When you call the grandparent function you pass in A (unassigned var) and david the system will find every variable that will make the statements in grandparent true.

He went on and made a little function that returned a drink based on a list of ingredients. But mainly he showed that there are many different ways of solving problems and it opened up my mind again.

# [Peter Hilton](https://twitter.com/PeterHilton)

I met Peter Hilton a few times already at the Rotterdam.rb Ruby meetup and got a little sneak peek at his Joy of Coding, mainly the jokes. It was about code documentation and how you can make it easier for yourself, and also why you do really need it.

## Why?

"Code can tell you what a function does but not why". That's the main reason you should write documentation and you can do that in many ways. For example the extended git commit. As I also explained in a lightning talk at work once, commit messages should consist out of 1 line followed by a blank line and a paragraph explaining why you did what you said you did in the first line.

```git
Change name of function X

I made it more descriptive so it's easier for new colleagues to understand why this method is there and what it does.
```

This is obviously an exaggeration and you shouldn't have to do this with every commit but sticking to this does force you to rethink, what am I actually committing?

Another form of documentation that inspired me was the "Today I Learned" repository. The idea is that every day you write a short summary of the things you learnt that day, which in the end results into a documented history of the work you did. Not only useful for colleagues but also for yourself since you have to recap for yourself too what you learnt, and it might force you to reread some stuff again. It might even make you realise you did something really stupid.

What I took from this talk is that writing what and why you do stuff is super important, not only for work but also on a personal level. It's the reason I started writing blog posts again.

# [Hilary Parker](https://twitter.com/hspter)

Hilary Parker had the difficult job of ending the day with a plenary talk. Everyone was tired, and dreaming of the (free) beer, wine and food coming up in a few minutes. She knew this and addressed also that right now we might not be most interested in a talk about 'data analysis'. With that the pressure was off in way.

She talked about her cats (like everyone) and about her former role at Etsy, a senior data analyst and her new job. Her talk was about a new type of person emerging in her field. Before her boss would want an all round dashboard in which he could see all the data ever. Something like that would be developed by an engineer and between the data analyst, engineer and the boss there were always problems, unachievable expectations and different views on the subject.

Her solution is the data developer. A data analyst that developer their own reports with a language that is easy enough to understand for someone without an engineering background but is powerful enough to automate the things they need to automate. She showed an amazing example, [Knitr](http://kbroman.org/knitr_knutshell/pages/Rmarkdown.html), in which you can use markdown and R together to make automated graphs from embedded R code chunks.

She made me think about something I've been noticing in different fields. Programming is no longer something that you have to to school for or that only a select group of people can use. Programming is becoming a staple like writing. It wouldn't surprise me if in 10 years programming is part of basic education at the same level as reading and writing. What it also means for us programmers is that we need to excel and prove our worth in an ever changing but exciting field of work.

# Cats

They were all great talks but cats were the talk of the day, and even the weekend after Corey Haines and Hilary Parker are visiting [some cats in Amsterdam](https://twitter.com/coreyhaines/status/744160526578630656)

So to end this post, here's my kitty cat Pickles! See you next year!

![Pickles sunbathing](https://i.imgur.com/qU7zrjI.jpg)
![Pickles derping](https://i.imgur.com/KFswkfe.jpg)

Oh also if you want to sponsor next year's event, [send an email](mailto:info@joyofcoding.org)

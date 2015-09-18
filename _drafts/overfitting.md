---
layout: post
title: Overfitting and the LSVRC
modified: 2015-08-23
categories: blog
comments: true
tags: 
image:
    feature:
---

##An entry-level guide to Machine Learning's "First Cheating Scandal"


###Setting the stage

At the end of May, the Large Scale Visual Recognition Competition, or [LSVRC](http://www.image-net.org/challenges/LSVRC/) (currently the word's top annual computer vision contest) announced that a team had violated the LSVRC's policies by over-submiting results. The [follow-up post](http://www.image-net.org/challenges/LSVRC/announcement-June-2-2015) named a team from Baidu as the perpetrators of this offense and explained that Baidu had been banned from submitting results to the LSVRC for a twelve-month period. [MIT Technology review](http://www.technologyreview.com/view/538111/why-and-how-baidu-cheated-an-artificial-intelligence-test/) called it "Machine learning's first cheating scandal."


It's not really posible to remove a paper from arXiv.org, so the offending team did the next best thing: they replaced [this functional draft on arXiv](http://arxiv.org/abs/1501.02876v4.pdf) with [this nonexistent one](http://arxiv.org/abs/1501.02876v5). And the primary researcher for the paper, Dr. Ren Wu, [was fired from his position](http://bits.blogs.nytimes.com/2015/06/11/baidu-fires-researcher-tied-to-contest-disqualification/) as "distinguished scientist at Baidu's Institute of Deep Learning." 


To the non-practitioner, it might seem a bit extreme. Why would submitting answers too often to a contest be an offense worthy of termination for a promising academic with a [good publication record](https://scholar.google.com/citations?user=0VxDjbcAAAAJ&hl=en)? And why should an entire corporation be banned from an international computer vision competition?

###The importance of contests:

The first thing we need to know about this situation is that machine learning as an academic discipline loves contests and datasets. In 1998, Yann LeCun (currently at Facebook and NYU) used the [MNIST dataset](https://gist.github.com/nebw/5504697c118744677c2d) to evaluate almost all the major computer vision algorithms people were studying at the time. This elevated the dataset to the position it held for over a decade: the MNIST became the dataset to evaluate computer vision (and machine learning in general) algorithms on, and [the article has had over 3700 citations](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=WLN3QrAAAAAJ&citation_for_view=WLN3QrAAAAAJ:u5HHmVD_uO8C). As one example, he tested convolutional neural networks (CNN's) on MNIST in 1998, though he had been working on CNN's for much longer than that. Variants of CNN's have recently become the state of the art in almost all computer vision tasks.

Benchmarking is highly important because Machine Learning is very performance focused: academics in ML do a lot of theoretical work, but algorithms are generally compared based on their performance on tasks that have specified training data.

After about a decade of MNIST's relative dominance as a benchmarking dataset.

In response, 

But why does the community 



###Overfitting!

When training a machine learning
![it's a thing](http://www.richardcorbridge.com/wp-content/uploads/2013/09/Overfitting.png)


 set the machine learning community ablaze: when there was a follow-up post.

To the outside observer

Link to the explanatory post:
http://www.image-net.org/challenges/LSVRC/announcement-June-2-2015


The paper itself:
http://arxiv.org/abs/1501.02876v5

>“The key sentence here is, ‘Please note that you cannot make more than 2 submissions per week.’ It is our understanding that this is to say that one individual can at most upload twice per week. Otherwise, if the limit was set for a team, the proper text should be ‘your team’ instead,” Wu wrote. “Our team has submitted about 200 times total in its lifespan. Our paper have five authors, and so based [on] the rule above, we should be allowed to submit around 260 times. And so, our 200 submissions were well within the 260 limits set by the rule. We obtained the world’s best result on this benchmark, and I am confident we are the best. There are two occasions that we have submitted more than 10 times per week. A mistake in our part, and it was the reason I made a public apology, requested by my management. Of course, this was my biggest mistake. And things have been gone crazy since. [To] state that we are cheating is baseless. Noted that we have obtained the world’s best results on other five benchmarks as well.”

The quote above is from:
http://www.enterprisetech.com/2015/06/12/baidu-fires-deep-images-ren-wu/

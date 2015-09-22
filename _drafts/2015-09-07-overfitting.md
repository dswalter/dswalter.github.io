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

## An entry-level guide to Machine Learning's "First Cheating Scandal"


### Setting the stage

At the end of May, the Large Scale Visual Recognition Competition, or [LSVRC](http://www.image-net.org/challenges/LSVRC/) (currently the word's top annual computer vision contest) announced that a team had violated the LSVRC's policies by over-submiting results. The [follow-up post](http://www.image-net.org/challenges/LSVRC/announcement-June-2-2015) named a team from Baidu as the perpetrators of this offense and explained that Baidu had been banned from submitting results to the LSVRC for a twelve-month period. [MIT Technology review](http://www.technologyreview.com/view/538111/why-and-how-baidu-cheated-an-artificial-intelligence-test/) called it "Machine learning's first cheating scandal."


It's not really posible to remove a paper from arXiv.org, so the offending team did the next best thing: they replaced [this functional draft on arXiv](http://arxiv.org/abs/1501.02876v4.pdf) with [this nonexistent one](http://arxiv.org/abs/1501.02876v5). And the primary researcher for the paper, Dr. Ren Wu, [was fired from his position](http://bits.blogs.nytimes.com/2015/06/11/baidu-fires-researcher-tied-to-contest-disqualification/) as "distinguished scientist at Baidu's Institute of Deep Learning."


To the non-practitioner, it might seem a bit extreme. Why would submitting answers too often to a contest be an offense worthy of termination for a promising academic with a [good publication record](https://scholar.google.com/citations?user=0VxDjbcAAAAJ&hl=en)? And why should an entire corporation be banned from an international computer vision competition?

### Benchmarking snd breakthroughs:

ML is a very performance focused discipline: academics in ML do a lot of theoretical work, but algorithms are generally compared based on their performance on tasks that have specified training data. The core idea is that when different algorithms are tested on the same data, we can gain a more objective sense of the relative performance. There are a few potential problems with this; I'll get to one of the major ones in a few paragraphs.

As an example of this benchmarking tendency, in 1998 Yann LeCun (perhaps the most influential researcher in computer vision right now, currently at Facebook and NYU) used the [MNIST dataset](http://yann.lecun.com/exdb/mnist/) to evaluate the most of the computer vision algorithms people were studying at the time. As a result, the MNIST became one of the most popular datasets to evaluate machine learning algorithms (often computer vision algorithms) on, and [the article has had over 3700 citations](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=WLN3QrAAAAAJ&citation_for_view=WLN3QrAAAAAJ:u5HHmVD_uO8C).

Various other benchmarking datasets have emerged through the years, such as [Caltech 101](http://www.vision.caltech.edu/Image_Datasets/Caltech101/), [Caltech 256](http://authors.library.caltech.edu/7694/), and the PASCAL VOC (Visual Object Classes), but the release of [ImageNet](http://www.image-net.org/papers/imagenet_cvpr09.pdf) by Fei Fei Li et al. was the great leap forward. I'll talk more about ImageNet in another post about datasets, but it dwarfs previous computer vision datasets in the number of classes and images per class. 

Because ImageNet is so much larger and contained much more varying classes, the LSVRC is a much more challenging competition than ones that came before it, so the algorithms that succeed need to have high representation capacity. Variants of Convolutional Neural Networks are the current state of the art and consequently most popular algorithm used; this was helped by a significant breakthrough in 2012 by alex krizhevsky, a PhD student at the time at the University of toronto. Krishevsky famously used the parallel computational capabiities of grapics cards (GPU's) to train much larger netorks than had previously been used, and [that paper](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) had a 9% lower error rate than the next best result on LSVRC 2012.

It was rightly hailed as a major breakthrough, and gpu training has since become pervasive. The authors of that paper (Krizhevsky, Sutskever, and Hinton) created a deep learning startup that was acquired in 2013 by Google, where they all currently work. I mention this story because it's ecactly what is hoped for from a major state of the art breakthrouh: a new technique or idea that is broadly applicable and improves the entire field.

In response,

But why does the community



### Overfitting!

One of the recurring problems in machine learning is evaluating the performance of your model in an objective way. For example, if you're trying to predict the stock market,
![it's a thing](http://www.richardcorbridge.com/wp-content/uploads/2013/09/Overfitting.png)



>“The key sentence here is, ‘Please note that you cannot make more than 2 submissions per week.’ It is our understanding that this is to say that one individual can at most upload twice per week. Otherwise, if the limit was set for a team, the proper text should be ‘your team’ instead,” Wu wrote. “Our team has submitted about 200 times total in its lifespan. Our paper have five authors, and so based [on] the rule above, we should be allowed to submit around 260 times. And so, our 200 submissions were well within the 260 limits set by the rule. We obtained the world’s best result on this benchmark, and I am confident we are the best. There are two occasions that we have submitted more than 10 times per week. A mistake in our part, and it was the reason I made a public apology, requested by my management. Of course, this was my biggest mistake. And things have been gone crazy since. [To] state that we are cheating is baseless. Noted that we have obtained the world’s best results on other five benchmarks as well.”

The quote above is from:
http://www.enterprisetech.com/2015/06/12/baidu-fires-deep-images-ren-wu/

---
layout: article
title: "#66DaysofData"
tags: data-science learning habit-building
author:
  Quilvio Hernandez
aside:
    toc: true
---

## Introduction
Recently I watched a YouTube video by [Ken Jee](https://www.youtube.com/channel/UCiT9RITQ9PW6BhXK0y2jaeg) introducing me to the [#66DaysofData](https://www.youtube.com/watch?v=qV_AlRwhI3I&ab_channel=KenJee) challenge. Research shows 66 days is the average time needed to ingrain a new habit. The goal is to spend at least 5 minutes every day learning data science to some degree. You're supposed to stay motivated by sharing your progress on the social media of your choice. In my case, I chose here! I encourage anyone reading this to try the challenge out for themselves! Stay tuned for daily (or maybe weekly) updates!

## Day 1  (04/27/21)
### General Adversarial Networks (GAN) [1] 
General Adversarial Networks (GAN) are useful for mimicking datasets and understanding how they're formed.  

#### Motivation  
One way to mimic a dataset (think generating dog images from a training set) is using parametric models. The weakness of parametric models is their faiulre to generate fine details. While parametric models may be useful for numerical datasets such as heights and weights, if we're trying to generate an image dataset there will be a lot of data loss. GAM solves this problem through implicit density estimation (meaning there is no analytical PDF that generates the dataset). 

#### How do they work?  
I will stay away from the math here because it is highly advanced, but I will address the genral framework. GAM generates two differentiable functions, G and D, that are essentially competed against one another in a game to outwit the other. D is known as the discriminator and G is known as the generator. D wants \\\(D(x) \approx 1\\\) when the sample \\\(x\\\) is taken from the data. When \\\(x\\\) is taken from the generative model the D's goal is \\\(D(G(z)) \approx 0\\\), while G hopes to fool D by convincing it \\\(D(G(z)) \approx 1\\\). In simpler terns, G is trying to generate a sample \\\(x\\\) using a deep neural network such that D cannot distinguish it from the the actual data (for reference, D is also a deep neural network). Through stochatic gradient descent algorithms (SGD), the Minimax game find an equilibrium, also known as the saddle point, of the discriminator loss. The generated results are oftentimes impressive, but also oftentimes far from perfect. 

[1] Goodfellow, I. (2017, April 3). NIPS 2016 Tutorial: Generative Adversarial Networks. arXiv.org. https://arxiv.org/abs/1701.00160. 

## Day 2  (04/28/21)
### Data Aggregation and Group Operations
Today I reviewed aggregating data and performing group operations by going through the corresponding chapter in [Python for Data Analysis](https://www.programmer-books.com/wp-content/uploads/2019/04/Python-for-Data-Analysis-2nd-Edition.pdf) by Wes McKinney. This has always been a good quick reference for me whenever I need to remember some pandas syntax or functions. 

## Day 3  (04/29/21)
### Clean Data Visualizations (Univariate Analysis)
The other day I came across [this notebook](https://www.kaggle.com/joshuaswords/awesome-eda-2021-happiness-population) that drew inspiration from another [good reference](https://www.kaggle.com/gaetanlopez/how-to-make-clean-visualizations). I also liked the first notebook in particular because it went above your "average" EDA and just goes to show that creativity is as important as any other skill in data science. 

Over the next couple days my goal is to create some visualization using the [student exam performance dataset](https://www.kaggle.com/spscientist/students-performance-in-exams?tags=13208-Data+Visualization).

Today's focus is on plotting univariate analysis.

## Day 4 (04/30/21)
### Clean Data Visualizations (Bivariate Analysis)

Today, I focused on density plots broken down by different categorical variables. For example, how does parent education affect student's scores in math, writing, and reading.

## Day 5 (05/01/21)
### Percentage Stacked Bar Chart 

Found another neat resource ([Python Graph Gallery](https://www.python-graph-gallery.com/stacked-and-percent-stacked-barplot)) to make a percent stacked barplot to see the percentage difference between test preparation and parent's education levels. 

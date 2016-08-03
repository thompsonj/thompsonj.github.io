---
layout: post
title:  "Review: A Practical Guide for Improving Transparency and Reproducibility in Neuroimaging Research"
date:   2016-07-28 14:05:00 +0200
comments: true
categories: [Journal club]
---
![Fig 1. Three pillars of Open Science: data, code, and papers.](http://journals.plos.org/plosbiology/article/figure/image?size=inline&id=info:doi/10.1371/journal.pbio.1002506.g001){: .center-image }
*Three pillars of Open Science: data, code, and papers.*

<!-- <div class="well well-sm">
Gorgolewski KJ, Poldrack RA (2016) A Practical Guide for Improving Transparency and Reproducibility in Neuroimaging Research. PLoS Biol 14(7): e1002506
</div> -->
<div class="alert alert-success" role="alert">Gorgolewski KJ, Poldrack RA (2016) A Practical Guide for Improving Transparency and Reproducibility in Neuroimaging Research. PLoS Biol 14(7): e1002506</div>

> "Having access to a plethora of denoising and modelling algorithms can be both good and bad. On one side, there are many aspects of brain anatomy and function that we can extract and use as dependent variables, which maximizes the chances of finding the most appropriate and powerful measure to ask a particular question. On the other side, the incentive structure of the current scientific enterprise combined with methodological plurality can be a dangerous mix. Scientists rarely approach a problem without a theory, hypothesis, or a set of assumptions, and the high number of “researcher degrees of freedom” can implicitly drive researchers to choose analysis workflows that provide results that are most consistent with their hypotheses."

As we stand on the verge of a reproducibility crisis[*](http://pps.sagepub.com/content/7/6/657) in neuroscience and psychology research, Gorgolewski and Poldrack advocate for the adoption of open science practices to improve transparency and reproducibility. Their [paper](http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1002506) succinctly outlines best practices for dealing with data, code and publication in ways that maximize reproducibility while minimizing additional effort. Here is my bullet point version of their paper.

## Data

Openly accessible data allows for:

* validation of results
* novel analyses
* combining data from multiple sources
* more citations
* maximizing benefits to research participants 

But there are several hurdles to making neuroimaging data openly available:

### Consent Forms

Get written consent from subject to share their data (and therefore maximize the benefits or their participation!). The authors have prepared several [templates](http://open-brain-consent.readthedocs.io/en/latest/ultimate.html) of data sharing clauses that can be inserted into consent forms. They provide clauses for normal populations and generic data and also clauses for sensitive populations/data, which may require that some of the data be approved by a data sharing committee to ensure protection of sensitive information. 

### Data Organization

We need common standards of data description and organization to facilitate sharing. The [Brain Imaging Data Structure (BIDS)](http://www.nature.com/articles/sdata201644) was recently proposed as a simple scheme to describe most MRI datasets. 

### Publishing Data

Data should be uploaded to a repository *before* the work is submitted for publication.

Field-specific Repositories:

* Functional Connectome Project/International Neuroimaging Data-Sharing Initiative (FCP/INDI)
* OpenfMRI

Field-agnostic repositories:

* FigShare
* Dryad
* DataVerse

Other suggestions:

* Consider long-term data retention
* [Open Science Framework (OSF)](www.osf.io) to link datasets with code and preprints
* Embargo period on submitted dataset to protect against "scooping"
* Make sure the necessary data and metadata are present using BIDS or XML-based Clinical and Experimental Data Exchange (XCEDE)
* Data paper - publication to describe new dataset rather than its analysis when dataset is large or complicated
* Share preprocessed volumes, statistical maps (see [NeuroVault.org](http://NeuroVault.org)), connectivity matrices (see UCLA Multimodal Connectivity Database), not just raw data.
* Accompany data with an appropriate license. The authors recommend an unrestricted Public Domain license (such as [CC0](https://wiki.creativecommons.org/wiki/CC0_use_ for_data) or PDDL). Note that data a treated differently than creative works or software by the legal system.

## Code

Sharing of analysis code is incredibly important not just for the interpretation and validation of results but also to address new research questions and accelerate science. 

Reasons people don't share code:

* Most researchers are not trained in software engineering so the code may be undocumented and lack formal tests
* Fear of obligation to provide user support
* Few incentives to spend the time writing high-quality, well documented code

>"Changes in the incentive structure of science will take years, but in the meantime, perceived poor quality of code and lack of thorough documentation should not prevent scientists from publishing it."

Why you should do it anyway:

* Sharing undocumented code is much better than not sharing code at all. See [Publish your computer code: it is good enough](http://www.nature.com/news/2010/101013/full/467753a.html)
* Sharing does not oblige to provide user support - consider establishing community-driven user support systems (e.g. google groups, NeuroStars.org).

How to improve the quality and "sharability" of your code:

* Use a version control system (VCS) like git. Version control will change your life, seriously. See [A Quick Introduction to Version Control with Git and GitHub](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004668) or this great free [Udacity course](https://www.udacity.com/course/how-to-use-git-and-github--ud775). 
* Automate whenever possible. A series of GUI clicks is not reproducible in the way that a script is. The authors have created a [fully automated analysis pipeline](https://github.com/poldrack/myconnectome-vm). 
* Adopt philosophy of "literate programming" for interactive data interrogation, combining analysis code, plots and text narrative. Tools like [Jupyter](http://jupyter.org) (for R, Python and Julia), [R Markdown](http://rmarkdown.rstudio.com) (for R), and [matlabweb](https://www.ctan.org/pkg/matlabweb) (for MATLAB) allow you to revisit a past interactive analysis and share with collaborators. 
* Share with an appropriate license, such as Apache 2.0, MIT, or GNU General Public License.

## Publications

* In addition to linking to data and code, accurate and thorough description of methods and data should be included in the supplementary material, if not in the main manuscript. 
* All results, even null ones, should be available somehow. For example, all additional contrasts that were not significant. Especially given how hard it is to publish null results separately.
* See  the Organization for Human Brain Mapping’s Committee on Best Practices in Data Analysis and Sharing (COBIDAS) [report](http://www. humanbrainmapping.org/cobidas/) for detailed recommendations on reporting.
* Make the manuscript publicly available. Preprints can be published on Biorxiv or arXiv. This allows for more feedback, can establish precedence, and, since preprints have DOIs, they can be referenced even before the manuscript is accepted for publication by a journal. 
* Consider sharing papers that have already been published in subscription-based journals. Some publishers allow for authors to post their manuscripts on noncommercial websites. See [SherPa/ROMEO](http://www.sherpa.ac. uk/romeo) to check what you are allowed to share. 

## Emerging Trends

* Preregistration - Write and register a study plan to reduce biases in published results. Some journals are participating in the Registered Reports program, wherein an experimental plan can receive "in-principle acceptance" and the journal guarantees to publish the final version of the paper.
* Public reviews - To motivate better quality reviews and give credit to reviewers. On occasions where anonymous reviews remain important, there should still be some method of assigning credit to the reviewers.

<p></p>
<div class="well well-sm"><h2>Simple Steps towards Open Science</h2>
Data: 
<ul><li>Include a section about data sharing in your consent forms.</li>
<li>Share your raw data upon paper submission using a repository dedicated to neuroimaging.</li>
<li>Consider writing a separate data paper for more complex and interesting datasets.</li>
<li>Remember that sharing your data improves the impact and citation rates of your research!</li>
</ul>
Code:
<ul><li>Use VCS’s for all your projects.</li>
<li>Share your code on GitHub.com <mark>even if it’s not well documented</mark>.</li>
<li>Set up a mailing list for user-related questions.</li>
<li>People reusing the code you shared will cite the relevant papers.</li>
</ul>
Papers: 
<ul><li>Include all extra analyses and null results in the supplementary materials without sacrificing the clarity of the message in the main body of the manuscript.</li>
<li>Submit preprints to claim precedence, solicit feedback, and give access to your research.</li>
</ul>
*Courtesy of Gorgolewski and Poldrack 2016*

<!-- You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated. -->

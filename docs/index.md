--- 
title: "Shiny on DataLabs (alpha version)"
author: "Michael Tso"
date: "2022-02-15"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib]
biblio-style: apalike
link-citations: yes
github-repo: NERC-CEH/ShinyDataLabsBook
description: "A book about the Shiny apps on DataLabs and their EDS use cases (created using the UKCEH bookdown template)."
---




# Preface {-}

<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>


A web app is application software that runs on a web server. It provides interactivity for users to explore its content and can provide live updating of the information displayed. However, building web apps would often require specialist knowledge in web development. Web development frameworks such as *Shiny* [@shiny] provides an easy way for scientists to build prototype web apps with the R language only. This means scientists can rapidly build these web apps themselves to engage their sceintific outputs with users.

The NERC DataLabs project (https://datalabs.datalabs.ceh.ac.uk) is a cloud-based cyberinfrastructure to allow environmental scientists to collaborate and share outputs more seamlessly. It includes powerful data store and notebooks environments and easy tools to publish Shiny apps.


This **live** book provides an entry point for users to discover the various use cases of Shiny web apps to advance envrionmental data science in DataLabs. It is **live** because it is dynamic and DataLabs users are welcome to add content to it. It also demonstrates to stakeholders the capabilities and added value UKCEH and the wider research community can offer to deliver projects via the use of Shiny apps.


Although each of the example apps discussed here have their specific use cases, where possible it also includes code snippets or a generic/minimal version of the app so that it can be readily transferable to other projects and applications.




<img src="img/UK_SCAPE_Logo_Positive_WithStrap.png" width="354" style="display: block; margin: auto;" />

 
---
All of the content of this repository is licensed 
[CC0](https://creativecommons.org/publicdomain/zero/1.0/).This [bookdown](https://bookdown.org/yihui/bookdown/) book is created using the template created by Pete Levy.


# Acknowledgment {-}


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

Project sponsor:

UK-SCAPE and various UKCEH projects.

# What is Shiny?


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

*Shiny* is a R package that underpins a web development framework to allow users to build web apps using the R progamming language only. In other words, you can turn any R code into a web app without the need to use any other programming language.

## The basic components of a Shiny app
Although *Shiny* apps can do fairly advanced things, a simple app is really easy to build. Its main  components are:

1. a user interface
2. a server-side function 



These two components are typically put in two separate files but they can be put in a single file too (e.g. `app.R`). Copy the above code chunk to your R terminal and run it.

Here is an example for a first Shiny app. You can run it in your local R terminal or R Studio during development. But the goal is to host them on a website, which you can do so easily on DataLabs (*link to DataLabs docs to be added*) (or with your organization or other web hosting providers).


## How can I get help or training?

There are number of free training available. Please also feel free to contact the author to discuss your requirements.

- Shiny gallery
- https://mastering-shiny.org/index.html
- UKCEH internal training



# Apps to allow improved contextual understanding of data


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

Data science methods provides new ways to analyze and understand environmental science data. Shiny apps can be a powerful way to showcase a methodological method with some real-world environmental science examples.

## ECN/Lakes state tagging app
In this example, @Tso2020 proposed a state tagging method to improved environmetnal data quality assurance. Contextual data (e.g. weather variables) are used to classify the state of the system arbitrarily. The user can then look at the inter- and intra-class variability of their observed variables. This method provides a step change to conventional range checks on envrionmental data.

In addition to two apps that demonstrates the method with ECN moth and Cumbrian Lakes chemistry data, a generic version of the app is also created to allow users to upload the same method to create the same analysis.

- https://statetag-ecnmoth.datalabs.ceh.ac.uk/
- https://statetag-lakes.datalabs.ceh.ac.uk/
- https://statetag-generic.datalabs.ceh.ac.uk/

<img src="img/statetagging1.png" width="281" style="display: block; margin: auto;" />


## Fuzzy changepoints demo app
Changepoints analysis is a method to detect sudden change in statistical properties in a time series. However, when comparing the changepoints from two time series, it may not be straightfoward due to due different frequencies and underlying generation process. @Hollaway2021 proposed a method to assess the agreement of changepoints detected in observe and simulated data using a fuzzy logic framwork, and demonstrated the method with a Shiny app.

https://dsne-fuzzycpteval.datalabs.ceh.ac.uk/


<div class="figure" style="text-align: center">
<img src="img/fuzzy.jpg" alt="A figure illustrating the fuzzy changepoints concept." width="379" />
<p class="caption">(\#fig:unnamed-chunk-4)A figure illustrating the fuzzy changepoints concept.</p>
</div>

## Cropnet demo app
https://cropnet-demonstrator.datalabs.ceh.ac.uk/

# Apps to improve custom use of data


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

## eLTER cookie-cutter app

# Promoting openness using Shiny apps


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

## GB Rainfall chemistry app
https://cptecn-sandboxdemo.datalabs.ceh.ac.uk/


While notebook technology provides powerful way for users to reproduce entire analyses, sometimes it may be helpful for users to experiment with some changes in small sections of a code in an isolated manner. One option is to turn a R Markdown document to a learnr (@learnr) document by specifying a few extra options so that the rendered notebook has executable 'sandboxes' for users to edit and re-run code chunks in real-time.Here the apporach is demonstrated on the outputs of a recent paper [@Tso2022]. This approach is further documented in @Tso2022RJ.

<div class="figure" style="text-align: center">
<img src="img/learnr.png" alt="A screenshot of the GB rainfall interactive notebook site. The main feature is the code box. When the site loads, the code that generates the published version of the figure is in the box and the published version of the figure is below it. Users can make edits and re-run the code in the code box and the figure will update accordingly. Users can use the “Start Over” button to see the published version of the code at any point without refreshing the entire site." width="640" />
<p class="caption">(\#fig:unnamed-chunk-5)A screenshot of the GB rainfall interactive notebook site. The main feature is the code box. When the site loads, the code that generates the published version of the figure is in the box and the published version of the figure is below it. Users can make edits and re-run the code in the code box and the figure will update accordingly. Users can use the “Start Over” button to see the published version of the code at any point without refreshing the entire site.</p>
</div>


## UKWIR AMR data explorer app
https://ukwir-testing.datalabs.ceh.ac.uk/

In some projects, a large number of measurements are taken and many plots would be generated if all results are plotted in a report. This app allows users to plot and filter the results.

The user may want to reproduce to plots in the app in their own R session. Using the Shinymeta R package [shinymeta], the user can simply import the underlying dataset, copy the code snippet from the 'Show code' box in the app, and reproduce the plot in their own R session.

<img src="img/UKWIR.PNG" width="628" style="display: block; margin: auto;" />


# Shiny apps to improve spatial comparison and visualization


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

## Map comparison tool

https://moisture-leaflet2min.datalabs.ceh.ac.uk/

Many environmental applications have a strong spatial component. The ability to compare maps becomes very helpful. This app provides a lightweight way to compare any two raster layers based on user inputs. The two interactive maps (powered by leaflet) are zoomable and synchronized.


<img src="img/map_comparison.png" width="960" style="display: block; margin: auto;" />

## PBMS demo app
https://statetag-pbmsdemo.datalabs.ceh.ac.uk/

Predatory Bird Monitoring Scheme is a citizen science project which members of the public submit the carcusses of birds of prey found for a biosy. The 20+ years worth of data is held in a database and has not been shared publicly. This app provides an easy way to visualize individual bird submission and provide data analytics, which is a great way to engage with various stakeholders.


<iframe src="https://statetag-pbmsdemo.datalabs.ceh.ac.uk/?showcase=0" width="672" height="600px" data-external="1"></iframe>



# Concluding remarks


<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

This book showcases the use to Shiny apps to advances the various aspects of envrionmental data science, using example apps hosted on DataLabs. This hopefully gives you some ideas on how to incorporate a Shiny app in your environmental science project to increase impact and engagement.

A more extended list of UKCEH Shiny apps is included in the appendix.

# Appendix {-}

<p align="center" style="font-weight: bold;color:orange">For Demonstration purposes only. Under development.</p>

Note that the source code of the many apps discussed are also deposited on GitHub and EIDC, e.g.:

- Fuzzy changepoint (https://doi.org/10.5285/49d04d55-90a7-4106-b8fe-2e75aba228e4)

UKCEH also host a number of Shiny sites under the https://shiny-apps.ceh.ac.uk/ domain. Here are some of the apps hosted there:

- [What's flying tonight](https://shiny-apps.ceh.ac.uk/whats_flying_tonight/)

# References {-}

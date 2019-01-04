November 23, 2018

Tracking Jupyter: Newsletter, the Fifth...
==========================================

by Tony Hirst

Welcome to this fifth edition of the _Tracking Jupyter_ newsletter (#TJ5). One more and it'll be six...  
  
_In case you haven't discovered it yet, a quick reminder about the new [Jupyter discourse site](https://discourse.jupyter.org/), a **community** focal point for discussion and help about all areas of the Jupyter ecosystem. Introduce yourself [here](https://discourse.jupyter.org/t/introduce-yourself/17/34)._  
 

Events and Announcements
------------------------

If notebooks move into the enterprise, they're likely to be of interest to the bad guys, not least because of their ability to execute arbitrary code; even notebooks previewed with _nbviewer_ may present a risk because they may embed arbitrary Javascript. So the availability of **security fixes **are likely to be of increasing interest to sys-admins. This week a couple of [Jupyter Notebook security fixes](https://blog.jupyter.org/jupyter-notebook-security-fixes-59817e86a711) were released via notebook v5.7.2. All versions of notebook from 5.3.0 to 5.7.1 were affected by the fixed issues. You have been warned... (Check by running _jupyter notebook --version_.) In case it's useful, here's a feed from the National Vulnerability Database (NVD):[ CVE (Common Vulnerabilities and Exposures)_ \[jupyter\]_](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=jupyter).  
  
Researchers and research software engineers may find the [Faraday Division Chemistry software tools meeting](http://www.rsc.org/events/detail/35843/faraday-division-chemistry-software-tools-meeting) on 12th December 2018 at the **Royal Society of Chemistry**, Burlington House, Piccadilly, London, W1J 0BA, of interest. Presentations include one on _The Data Science Revolution: Jupyter Notebooks & Python, R Notebooks & R_.  
  
Amazon seemed to have joined the managed notebook hosting party and announced [Amazon EMR Notebooks](https://aws.amazon.com/emr/features/)​,_"a managed environment, preconfigured to work with Apache Spark, based on Jupyter Notebooks, for data scientists, analysts, and developers. Hosting is inside Amazon VPC \[virtual private cloud\] with no internet access; notebook files are regularly backed up to S3"_ \[[announcement](https://aws.amazon.com/about-aws/whats-new/2018/11/introducing-emr-notebooks-a-managed-analytics-environment-based-on-jupyter-notebooks/)\].  
 

Making Sense of IT
------------------

Sharing means many things to many people, but in an organisation more often than not it means email. So if you feel the need to share a notebook that way, but its too much effort to save a notebook, context switch into email, faff around uploading the notebook (when you remember where you saved it) and then try to remember who you wanted to send it to and why, try this instead: a [Jupyterlab extension](https://github.com/timkpaine/jupyterlab_email) to email notebooks from Jupyterlab. Configure the server extension with your SMTP server details, then send your notebook inlined in an email (with or without code) or as an attachment (HTML, PDF). You can also attach data files. The developer has a wealth of repos under his belt, many of which feed into some notebook tools for J.P. Morgan. Do they run preconfigured email extensions under a centrally managed JupyterLab environment, I wonder?!  
  
Vincent/@_jvtoups_ [tweets](https://twitter.com/jvtoups/status/1063810061603086337): _Jupyter notebooks are an absolutely perfect example of a tool that lets you do the wrong thing more easily and for longer._ It's part of a thread, so check it out. Looking to the possible blockers and downsides is an important consideration when_TrackingJupyter_. Joel Grus' JupyterCon 2018 talk I don't like notebooks ([video](https://www.youtube.com/watch?v=7jiPeIFXb6U), [slides](https://docs.google.com/presentation/d/1n2RlMdmv1p25Xy5thJUhkKGvjtV-dkAIsUXP-AL4ffI/edit#slide=id.g362da58057_0_1)) is worth a look in this respect. So too are the thoughts on notebooks, IDEs, and R Markdown offered in response by Yihui Xie, creator of _knitr_ and a wealth of other reproducible publishing workflow tools for the R ecosystem: [The First Notebook War](https://yihui.name/en/2018/09/notebook-war/).  
  
In [#TJ4](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fourth), I gave several examples of how IBM uses notebooks to promote Watson AI cloud services. Other API providers, such as Microsoft, follow a similar approach, publishing demo notebooks for their [Microsoft Cognitive Services APIs](https://github.com/Microsoft/cognitive-services-notebooks) and [Cognitive Vision API](https://github.com/Microsoft/Cognitive-Vision-Python). They also have some [autonomous driving tutorials](https://github.com/Microsoft/AutonomousDrivingCookbook). On the extensions front, notebooks users can make use of [Kqlmagic](https://github.com/Microsoft/jupyter-Kqlmagic), a Microsoft Azure Monitor extension that allows developers to _"explore Microsoft Azure Monitor data: Azure Data Explorer (Kusto), ApplicationInsights, and LogAnalytics data using kql (Kusto Query language)"_.  
 

Deep in the Code
----------------

One of the things I was unsure about when I started the _TrackingJupyter_ newsletter was what sort of items might arise each week and whether they would be substantive enough to merit comment. If you're into standards, protocols and low level data engineering, one of the discussions currently on the JupyterLab Github repo (where discussions about what's going to happen next take place) proposes a [JupyterLab Data Bus](https://github.com/jupyterlab/jupyterlab/issues/5548). I think this could be an important discussion, at least for as long as everybody plays nicely. The original pitch related to a standard for MIME-typing datasets to help with object rendering via the UI, but the question also arises as to whether this could help support polyglot language use within a notebook. That is, should a databus be initially designed to support just kernel-to-output-cell comms, or kernel-kernel comms too.  
 

Notebook Deployments
--------------------

Via a tweet (thanks @ReadDavid), I am reminded of the UK **Ministry of Justice (MoJ)** [Analytical Platform](https://mojdigital.blog.gov.uk/2018/04/05/pushing-the-boundaries-of-data-science-with-the-moj-analytical-platform/)_"built on AWS and Kubernetes, ... to create virtual infrastructure that supports secure environments running analytical software like R Studio and JupyterLab"_. Word has it that R/RStudio are still the preference of many users, which is presumably why (or because?) the [user guidance docs](https://moj-analytical-services.github.io/platform_user_guidance/) seem to focus on RStudio/Shiny ecosystem. The intention is for the platform to be used by all 300 analysts across the MoJ and its associated agencies.  
  
_\[I note that in principle RStudio is available as [enterprise offering](https://www.rstudio.com/products/rstudio-server-pro/) (even if the free version is the one that is deployed) which may breed trust in it. This raises an interesting question as to whether the core Jupyter devs could/should spin out a commercial JupyterPro offering, or leave it to the market and/or open source community to provide hosting, enterprise integration and support? —Ed.\]_  
  
Some notes on the architecture of the complementary MoJ [Analytical Data Store (ADS)](https://moj-analytical-services.github.io/Analytical_datastore_architecture/index.html) have also just started to appear via an MoJ Analytical Services Github Sites [repo](https://github.com/moj-analytical-services/Analytical_datastore_architecture). Although recently closed, this [MoJ Technical Architect](https://jobs.jobvite.com/justicedigitalandtechnology/job/oBKw8fwJ) job ad (up to £85k, _\[i.e. untold wealth, if you work in academia, which is why I'm reduced to [selling t-shirts](https://ouseful.teemill.com/product/excel-went/) —Ed.\]_) possibly helps explain why we have such a problem in edu recruiting people with the necessary technical expertise.  
  
Corporate adoption of Jupyter notebooks, such as Netflix's widespread adoption ([#TJ1](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-first)), seems to be pretty established by now. This includes using centrally offered, internally branded and extended notebook environments, as well as providing notebook extension packages that can be used to extend any Jupyter notebook environment (see several examples in [#TJ4](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fourth)). Full reviews of many of the platforms, and the architecture surrounding them can be tricky to find, although there are often quick, team generated review blog posts, such as this one describing Uber's [_Data Science Workbench_](https://eng.uber.com/dsw/).  
  
Central service offerings from research institutions are also running in the wild. Examples include [SWAN (](https://swan.web.cern.ch/)[Service for Web-based ANalysis)](https://swan.web.cern.ch/) ([docs repo](https://github.com/swan-cern/help)), a CERN service that _"allows users to perform interactive data analysis in the cloud, following a 'software as a service' model"_.  
  
In the US, the [Data and Analytics Services ecosystem](https://docs.nersc.gov/services/jupyter/) operated by NERSC, the US National Energy Research Scientific Computing Center, uses JupyterHub to provide access, via NERSC credentials, to notebooks and JupyterLab. (There's a [repo](https://github.com/NERSC/jupyterhub-deploy) describing their Dockerised Jupyterhub deployment route.)  
 

Notebook Publishing / Documentation Generation
----------------------------------------------

One of the promises of **reproducible ****research** methods are publication workflows that can to be used to create publication quality PDF documents from original code and analysis containing notebooks, or code+markdown documents in the more mature (publication support wise) _RStudio/Rmd_ environment.  
  
But notebooks can also be used to support informal publication (blogging) and the production of technical documentation.  
  
Here's a nice example of a textbook served three ways: as [static HTML](https://www.fuzzingbook.org), as interactive notebooks via MyBinder, or as a slideshow: [Generating Software Tests](https://github.com/uds-se/fuzzingbook). From the repo directory structure, it looks like epub and PDF output formats may be on the way too. This mainly makes use of technology that's already to hand: previewing notebooks in Github, running notebooks in MyBinder, or rendering them them as an HTML site. The comprehensive Makefile details the processing required on the original notebooks. In part, it also seems to make use **IPyPublish**...  
  
[IPyPublish](https://github.com/chrisjsewell/ipypublish) \[[docs](https://ipypublish.readthedocs.io/en/latest/)\] provides_"\[a\] workflow for creating and editing publication ready scientific reports and presentations, from one or more Jupyter Notebooks, without leaving the browser"_. At heart, this looks like a wrapper around _nbconvert_ that generates a single notebook from a set of notebooks; from that, it can then generate variously formatted output documents.   
  
If you fancy using notebooks as a blog post editor, and if Jekyll is your thing, [Jupyter Books](https://github.com/choldgraf/jupyter-book) provides _a guide and template for hosting your own book using Jupyter Notebooks and Jekyll_. The Nikola static site generator also offers [support](https://getnikola.com/handbook.html#supported-input-formats) for generating posts from notebooks.  
  
For **documentation**,[nbsphinx](https://github.com/spatialaudio/nbsphinx)[(docs)](https://nbsphinx.readthedocs.io/en/0.3.5/) provides a Sphinx extension for generating Sphinx docs from notebook. (Sphinx is the publishing system used to generate **_readthedocs_** sites; if its new to you, here's a general [introduction to Sphinx and Read the Docs for Technical Writers​](https://www.ericholscher.com/blog/2016/jul/1/sphinx-and-rtd-for-writers/)). As an example of what it can do, this [pythonrobotcs readthedocs page ](http://pythonrobotics.readthedocs.io/en/latest/modules/Planar_Two_Link_IK.html?highlight=Two%20joint%20arm%20to%20point%20control)is generated from this [notebook](https://github.com/AtsushiSakai/PythonRobotics/blob/master/ArmNavigation/two_joint_arm_to_point_control/Planar_Two_Link_IK.ipynb). A Sphinx extensions module for generating a [gallery of notebook examples](https://github.com/Chilipp/sphinx-nbexamples) is already available, as are at least a couple of themes (["official" Jupyter sphinx theme](https://github.com/jupyter/jupyter-sphinx-theme) and the [Jupyter alabaster theme](https://jupyter-alabaster-theme.readthedocs.io/en/latest/index.html)).   
  
_(By the by, this looks like it could be a [handy trick](http://blog.rtwilson.com/how-to-get-nice-vector-graphics-in-your-exported-pdf-ipython-notebooks/) for generating multiple output formats from your matplotlib charts, which means you can get vectorised, rather than PNG, images into a document when converting a notebook to LaTeX or PDF.)_  
 

Charting
--------

There are lots of charting libraries out there, and lots that support Jupyter notebook and/or JupyterLab integration, but if you need to standardise on one, how do you go about choosing one from the many? This post from one of the developers on the UK Ministry of Justice Analytical Platform sets out some of his considerations: [Why I’m backing Vega-Lite as our default tool for data visualisation](https://medium.com/@robin.linacre/why-im-backing-vega-lite-as-our-default-tool-for-data-visualisation-51c20970df39).   
  
One of the considerations is the existence of advanced GUI tools. For VegaLite, [Voyager2](http://vega.github.io/voyager/) is one such tool, which is conveniently available as a Jupyter extension ([jupyterlab\_voyager](https://github.com/altair-viz/jupyterlab_voyager)). _\[I thought I'd referenced this extension in a previous TJ issue but I can't spot it. My tracking strategy is already broken... —Ed.\]_  
  
Another consideration might be who's leading on the package development. Several corporates have explored charting libraries, such as Bloomberg's[bqplot](https://github.com/bloomberg/bqplot) ([docs](https://bqplot.readthedocs.io/en/latest/)) which have been widely used in notebooks for some time.  
  
Also from the financial sector, a release from **JP Morgan Chase** in the form of [perspective](https://github.com/jpmorganchase/perspective), a _"streaming data visualization engine for Javascript that makes it simple to build real-time & user configurable analytics entirely in the browser"_. So why have I mentioned it here? Because there's a [JupyterLab extension](https://github.com/jpmorganchase/perspective/tree/master/packages/perspective-jupyterlab) that wraps it, that's why...  
  
New out from Spotify, comes [chartify](http://labs.spotify.com/2018/11/15/introducing-chartify-easier-chart-creation-in-python-for-data-scientists/) ([repo](https://github.com/spotify/chartify)) an open-source (Apache License 2.0) Python library that wraps Bokeh to make it easier for data scientists to create charts. There are, of course, [example notebooks](https://github.com/spotify/chartify/blob/master/examples)...   
  
In the Observeable notebook world ([#TJ1](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-first)), integration for Uber's [Hexagonal hierarchical geospatial indexing system](https://github.com/uber/h3) ([tutorial](https://beta.observablehq.com/collection/@nrabinowitz/h3-tutorial)). There _is_ an H3 Python package ([h3-py](https://github.com/uber/h3-py)), although at the time of writing it's lacking _\_\_repr\_\__ renderers, IPython magic, Jupyter extensions and a Binderised demo...  
 

Debugging Extensions and Utilities
----------------------------------

Another offering from the developer of the _jupyterlab\_email_ extension (_you can maybe see a theme running through some of the items in this issue?! —Ed._), the _[pylantern](https://pylantern.readthedocs.io/en/latest/index.html) _package([repo](https://github.com/timkpaine/lantern)) provides access to dummy data in a variety of formats, utility functions (for example, exporters to different filetypes and support for different table rendering (_Perspective_ (JP Morgan), _Plotly_, _QGrid_ (Quantopian), _ipysheet_ (QuantStack), lineup\_widget) and graphical back ends (_Matplotlib, Plotly, Bokeh_, with more on the way)).  
  
It also bundles a JupyterLab [variable inspector widget](https://pylantern.readthedocs.io/en/latest/widgets.html?highlight=variableinspector#lantern.VariableInspector). One of the oft heard complaints about Jupyter notebooks is that they don't provided debug support (or at least, not debug support IDE based developers are used to) — REPL just doesn't cut it — and a **variable inspector** is a small but useful contribution to such support.  
  
Remember that in the trad notebooks, there is always the [variable inspector extension](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/varInspector/README.html), though to my mind the usability is a bit off.  
  
Another step-up comes in the form of IBM's [PixieDebugger](https://medium.com/ibm-watson-data-lab/the-visual-python-debugger-for-jupyter-notebooks-youve-always-wanted-761713babc62) ([docs](https://pixiedust.github.io/pixiedust/1-1-8.html)), a visual debugger built using [PixieApps](https://pixiedust.github.io/pixiedust/pixieapps.html) (_"Python classes used to write UI elements for your analytics that run directly in a Jupyter notebook"_) and part of the _PixieDust_ package previously mentioned in [#TJ4](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fourth). This interactive widget provides a **code-stepper** to let you step through the code in a particular cell a line at a time, as well as set **break points**.   
  
If you're looking for a code stepper and simple variable inspector for simple examples in a teaching context, then you might find the [nbtutor](https://github.com/lgpage/nbtutor) extension, as inspired by the _Online Python Tutor_, more useful.  
  
Support is also provided in the _Script of Scripts/SoS (Python) kernel_, about which more next week, for [line by line code execution](https://vatlab.github.io/blog/post/sos-notebook/#side-panel-line-by-line-execution-of-cells) within a cell and [variable inspection](https://vatlab.github.io/blog/post/sos-notebook/#preview-of-variables-and-files).  
  
Personally, I step through code chunks by running code in separate cells, often a line of code in a cell at a time, which provides variable inspection and _de facto_ break points implicitly. REPL style debugging ftw... But then again, I'm just a scruffy tinkerer...  
 

Notebook Examples
-----------------

One of the great things about notebooks is that educators seem happy to share their notebook based course material on Github, although often without a license (make of that what you will;_ \[what sort of reuse do you think is implied??? —Ed.\]_) Take for example, this collection of [notebooks on statistics](https://github.com/jmportilla/Statistics-Notes): is it an open educational resource in a legal sense? How about in a _de facto_ sense?! Another thing to note about notebooks as potential OERs: learners get read/writability and interactivity for free when they view the notebook via a Jupyter notebook server, which you can do using services like MyBinder.  
  
One for the Deep Learning folk... The ONNX Model Zoo is _"a collection of pre-trained, state-of-the-art models in the ONNX format"_ ([ONNX](https://onnx.ai/), the _open Neural Network eXchange format_, is an open format supporting the representation of deep learning models). Deep in the collection are a set of models developed using ArcFace, a CNN (convolutional neural network) based model for face recognition ([paper](https://arxiv.org/abs/1801.07698)). A set of notebooks demonstrates how to [use the models to do inference in MXNet](https://github.com/onnx/models/tree/master/models/face_recognition/ArcFace). Another set of notebooks demonstrate how to perform [semantic segmentation on an image](https://github.com/onnx/models/tree/21909b7db480200f9b23075c998810510cc2f089/models/semantic_segmentation/DUC).  
  
Citable / DOI'd  notebooks..? Here are a couple of examples: [Pasrelmouth Praat Scripts in Python](https://osf.io/6dwr3/) (_"__measure pitch, standard deviation of pitch, and hnr in python using parselmouth, a package that runs Praat in python"_) \[_I'm not sure how the typo gets handled once you mint the DOI? —Ed._\]. This blog post — [The Green HPCG List](https://plasma.ninja/blog/hpc/manycore/top500/computing/hardware/energy/efficiency/2018/11/18/HPCG_Green.html) — also links to a [DOI'd](https://doi.org/10.14278/rodare.68) interactive Jupyter Notebook and source HPCG dataset.  
  
It's still a rare occasion when examples of Julia notebooks cross my path (maybe I need to tweak my filters?) but here's one: a [notebook that runs against a Julia kernel](https://github.com/vOptSolver/vOptSolver-notebook) to demonstrate how to use the vOptSolver optimisation tools provided by the vOpt Julia package.  
  
And finally, if computational fluid dynamics are your thing, there's a sequence of Jupyter notebooks featuring the ["12 Steps to Navier-Stokes"​](https://github.com/barbagroup/CFDPython).  
 

Tips and Tricks
---------------

If you've been using notebooks for a long time, you've probably got your own tips and tricks, but maybe also forgotten some of them along the way. And if you're new to notebooks, you've got a lot of treats to come... So in what may be a regular feature, or may be more irregular, here are some Jupyter [Tips'n'Tricks](http://mkhalusova.github.io/blog/2018/11/15/jupyter-tips-n-tricks).

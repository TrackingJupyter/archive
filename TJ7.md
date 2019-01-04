December 07, 2018

Tracking Jupyter: Newsletter, the Seventh...
============================================

by Tony Hirst

Welcome to this seventh edition of the _Tracking Jupyter_ newsletter (#TJ7). Is it helping you keep up, or get up to speed with, with what's relevant to you in the Jupyterverse?! Or is it just a Friday distraction???  
  
_This edition is a bit wordy, again; I need to look at how to drop some of the items into longer blog posts and then perhaps post summaries here that link out to them. (Plus, my personal blogging time has been suffering by spending time here rather than there!)_  
 

Errata
------

Well, it had to happen sooner, rather than later I guess! In the previous newsletter, #TJ6, which references Fred Reiss' _"5 Stages of Enterprise Jupyter Deployment"_, I sniped that the presentation was a plug for Jupyter Kernel Gateway. Kevin Bates pointed out that _\[i\]t's actually a "plug" for Jupyter Enterprise Gateway. :-) . Although JEG is built directly on JKG, it adds support for launching remote kernels across managed clusters - which enables enterprises to better scale kernels across their resources_. Oops.. my bad... that'll teach me to be snarky... _\[Note to self: must do better —Ed.\]_  
 

Announcements and Releases
--------------------------

I was just too late to catch this with last week's newsletter, but a two day sprint last week pulled together a [Teaching and Learning with Jupyter](https://jupyter4edu.github.io/jupyter-edu-book/) book ([repo](https://github.com/jupyter4edu/jupyter-edu-book/)) containing a wealth of ideas and (brief) case studies relating to educational (teaching and learning) contexts rather than research related examples. The sprint was funded under the first call of the Bloomberg funded_Jupyter Community Workshop_ series; the second[c](https://blog.jupyter.org/jupyter-community-workshops-call-for-proposals-26a8417e5b6a)[all for proposals](https://blog.jupyter.org/jupyter-community-workshops-call-for-proposals-26a8417e5b6a) is still open, with a deadline of December 10th. If you're looking to team up with someone, the official [Jupyter discourse community](https://discourse.jupyter.org/) could be a sensible place to look. _\[I really should have put something in, shouldnlt I? —Ed.\]_  
  
For Clojure fans, I note the appearance of _[iclojure](https://github.com/HCADatalab/IClojure)_, a Jupyter kernel for Clojure, inspired by [Clojupyter](http://https://github.com/clojupyter/clojupyter), and _"based on the [Unrepl protocol](https://github.com/Unrepl/unrepl)"_ (a _"common ground for better Clojure REPLs"_, apparently...).  
  
For R fans and py-R polyglotters alike, a new @mybinderteam example [Binderhub repository](https://github.com/binder-examples/r_with_python#r--python-binder-example) demonstrates several ways of running R and Python: the demo runs _RStudio_, _reticulate_, _Rmd_ and Jupyter notebooks _"all from one repository"_.  
  
For competitive data junkies, Google have announced [Kaggle integration with Google Data Studio](https://www.blog.google/products/marketingplatform/analytics/announcing-kaggle-integration-google-data-studio/) allowing users _"to connect to and visualize Kaggle datasets directly from Data Studio using the Kaggle Community Connector"_. (Google acquired Kaggle in March 2018). _\[As with other Google services, I guess it'll remain availble until they decide to drop it. To the extent these are "free" services, you should probably also consider how you're actually paying for them. —Ed.\]_  
 

Papers and Preprints
--------------------

A recent paper in _Nature Genetics_ ([A primer on deep learning in genomics](https://www.nature.com/articles/s41588-018-0295-5)) has an associated interactive tutorial in the form of a [notebook linked to run on Google CoLab](https://github.com/abidlabs/deep-learning-genomics-primer).  
  
And here are a couple of recent preprints appearing on arXiv: firstly, [Towards new solutions for scientific computing: the case of Julia​](https://arxiv.org/abs/1812.01219) reviews the _"features and shortcomings"_ of Julia, the Ju in Jupyter, to mark the release of its _"first stable version (1.0) ... in August 2018"_. with particular reference to astronomy and astrophysics applications; secondly, a review of the cloud-based architecture of JOVIAL (_Jupyter OVerrIde for Astronomical Libraries_), a multi-user notebook fronted, service offering high-performance, high-availability compute to astronomers ([JOVIAL: Notebook-based Astronomical Data Analysis in the Cloud](https://arxiv.org/abs/1812.01477)). There's also a [deployment guide](https://github.com/ChileanVirtualObservatory/jovial.chivo.cl).  
 

Integrated Scientific Research Platforms
----------------------------------------

As well as the JOVIAL platform mentioned above, here are two more platforms offering integrated notebook + thematic code environment + specialist data access services.  
  
First up, [SciServer](http://www.sciserver.org/), _"a collaborative research environment for large-scale data-driven science"_ from Johns Hopkins University ([original architecture](http://idies.jhu.edu/sciserver-compute-bringing-analysis-close-to-the-data/)). Within SciServer, Jupyter notebooks are provided as a first class client and can also be used as part of batch processing jobs. _\[Support for interactive operations, cache managed workflows, and  scheduled/batch jobs is going to be a key feature of such platforms, I think—Ed.\]_ Various [environment images](http://www.sciserver.org/support/compute-images/) are defined to support activity in different research areas, including earth sciences (_"packages to create maps and conduct geospatial analyses with Geographic Information Systems (GIS)"_), fluid dynamics, genomics and astronomy. The platform also provides support for [managing group based projects](http://www.sciserver.org/support/help/). Foot-in-the-door [notebook and JupyterLab extensions](https://github.com/sciserver/nb_sciserver) are also available.  
  
Secondly, the NOAO[(National Optical Astronomy Observatory) Data Lab](https://datalab.noao.edu/) platform designed to enable _"efficient exploration and analysis of the large datasets now being generated by instruments on NOAO and other wide-field telescopes"_. Once again, Jupyter notebooks are [integrated into the platform](http://datalab.noao.edu/analysis.php). An [architecture overview](https://authors.library.caltech.edu/73372/1/99130L.pdf) describes how support for four approaches to working with the data — catalog science, data exploration, user-defined custom workflows, collaborative research — are supported by various design components: large catalogs, pixel data, virtual storage, visualisation/interactive data exploration, compute processing (workflows running close to the data. Additional features include support for users to _"publish their own datasets, access external data/compute services, export workflows to run at larger-scale facilities, distribute software for use by others"_.  
  
Trend wise, there are a couple of things to note: firstly, platforms / architectures that support notebooks + data + workflow management + collaboration; secondly, containerised stacks/environments containing preinstalled and preconfigured packages relevant to a particular subject area and/or organisation.  
  
Looking around more widely, a 2017 article, [Jupyter and Galaxy: Easing entry barriers into complex data analyses for biomedical researchers](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005425) describes a way of extending [Galaxy](https://usegalaxy.org/), _"an open source, web-based platform for data intensive biomedical research"_ such that a containerised notebook server could be launched from the platform to provide an interactive notebook interface to other services running on the platform. Paraphrasing the paper, notebooks interact with Galaxy services via the Galaxy API and can be used to create scripts that can be used as templates for new Galaxy tools. The notebooks can then _"be re-run with changed parameters on different datasets, and like any other history item, it can be shared with other Galaxy users"_. By which I guess they mean, you can write, share and reuse your notebooks?  
  
For off-the-shelf Galaxy installs, a [Galaxy Docker image](https://github.com/bgruening/docker-galaxy-stable) provides an _"__easy distributable full-fledged Galaxy installation, that can be used for testing, teaching and presenting new tools and features"_. A Jupyter notebook server can be used to extend Galaxy as an _Interactive Environment (IE)_ launched inside a Docker container within **Galaxy Docker container**. _\[Reminds me a little bit of launching RStudio or OpenRefine (using [openrefineder](https://github.com/betatim/openrefineder)) from a Jupyter notebook "New" menu in MyBinder, although those are "command line" apps rather than docker-in-docker apps. Are there also equivalent examples for starting/stopping database servers ("data kernels"?!) from Jupyter environments, I wonder? —Ed.\]_  
 

Corporate Adoption
------------------

One for the system architects:Adyen, an online payments platform, have a write up of how they went about [Building our data science platform with Spark and Jupyter](https://medium.com/adyen/building-our-data-science-platform-with-spark-and-jupyter-1894c33e6dd0). Important considerations included the need for an on-premise stack and the ability to get a minimum viable product up and running within a month. _\[A month?! I would love to be able to get anything done in a month... —Ed.\]_ The article (briefly) reviews why they ended up with Spark and Jupyter notebooks. Kernel wise, they looked at [Apache Livy](https://livy.incubator.apache.org/) (_"a REST Service for Apache Spark_") and [Apache Toree](https://toree.incubator.apache.org/) (_"a kernel for the Jupyter Notebook platform providing interactively access to Apache Spark"_) before opting to create their forks of the official Python and R kernels _\[I don't see them amongst [their Github repos](https://github.com/Adyen) though? —Ed.\]_ Instrumentation was added to all levels of data analysis workflows (_"from looking when users looked in and which notebooks were opened to linking the code entered in notebooks with actual files created and accessed on HDFS"_) though a fork of Jupyter protocol client library. ETL automation is supported through a (closed source?) custom developed orchestrator/scheduler framework, _Spoink_.  
 

Automation & Scheduling
-----------------------

[Papermill](https://github.com/nteract/papermill) ([docs](https://papermill.readthedocs.io/en/latest/)) is a _"tool for parameterizing, executing, and analyzing Jupyter Notebooks"_ created under the auspices of the _nteract_ project (or at least, that's where the repo lives). The **origin story** can be found in a Netfix technology blog post: [Scheduling Notebooks at Netflix](https://medium.com/netflix-techblog/scheduling-notebooks-348e6c14cfd6). Workflows can be defined to run **parameterised notebooks** automatically. _Papermill_ also provides support for **summary notebooks** in the form of tooling for pulling resources (such as generated charts) out of one notebook and into another. In addition, _"users can save values to the notebook document to be consumed by other notebooks" \[This could presumably be used as the basis of notebook tests? —Ed.\]_. Handy.  
  
It never ceases to amaze me how quickly pieces can fall into place once you have certain enabling technologies to hand. For example, given the existence of something like _papermill_, what becomes possible if you bake it into a VM made available as a service (as per the [DeepLearning Images VM, Revision M12](https://blog.kovalevskyi.com/deeplearning-images-revision-m12-papermill-from-netflix-cudnn-7-4-chainer-5-0-0-6e4f87f514ef) machine learning image on the Google Cloud Platform ([guide](https://blog.kovalevskyi.com/deep-learning-images-for-google-cloud-engine-the-definitive-guide-bc74f5fb02bc)))? Well, this, for example: [How To Submit Jupyter Notebook For “OverNight” Training on Google Cloud Platform](https://blog.kovalevskyi.com/how-to-submit-jupyter-notebook-for-overnight-training-on-gcp-4ce1b0cd4d0d).  
  
More generally, if you want parameterised notebooks for **scheduled batch running**, how about something like _[paperboy](https://github.com/timkpaine/paperboy)_, a _"web frontend for scheduling Jupyter Notebooks as reports"_ using Papermill + **Apache Airflow**. If you want the completed notebook exported as a PDF report, or emailed to you, that can all be handled too. _(PayPal's notebook scheduling PPExtensions tool, as announced over the summer and mentioned in [#TJ4](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fourth), is still languishing (at best) as a Pull Request.)_  
 

Remote Code Execution Using Binderhub
-------------------------------------

Some of the OU courses I've enjoyed working on most were the "reflexive" ones, where the tech we were teaching about was the tech we were using as part of the course. The production method used to produce the _Teaching and Learning with Jupyter_ book looks to be via _R/bookdown_ (Yihui Xie's R publishing tools and their RStudio integration are still way ahead of the _Jupyter/py_ space, I think) although I'd imagined it might be a bit more "Jupyter-meta": written using notebooks to demonstrate a book publishing workflow, perhaps using something like [Jupyter books](https://predictablynoisy.com/jupyter-book/intro.html) / [nbinteract](https://www.nbinteract.com/), a template form creating Binderhub backed interactive textbooks created from markdown files and notebooks.  
  
Another approach might have been to use Binderhub support launched via [ThebeLab](https://minrk.github.io/thebelab/) or [Juniper](https://github.com/ines/juniper), two Javascript packages that allow you to create interactive read/write/execute code activities embedded in an IFrame in an arbitrary web page.  
  
One thing that struck me earlier this week was that if you wrap a command line application using [metakernel](https://github.com/Calysto/metakernel), you can call it from a web page using something like ThebeLab. Here's an example of [using Gnuplot via ThebeLab](https://blog.ouseful.info/2018/12/06/jupyter-is-not-just-notebooks/).  
  
_\[The way the book was created by a volunteer team as part of a sprint also reminded me of the [Data Journalism Handbook](https://datajournalismhandbook.org/), the second edition of which is due out any time; and it got me wondering: what would a Jupyer backed, interactive Data Journalism Recipe Book, written using Jupyter Books, be like? —Ed.\]_  
 

Notebook Galleries, File Management and Search
----------------------------------------------

Keeping track of notebooks in a multi-user setting, particularly across a larger organisation, can create all manner of file management issues, but a couple of other _nteract_ projects look like they might be helpful in this respect, at least if you work with an _nteract_ client: [bookstore](https://github.com/nteract/bookstore) provides _"tooling and workflow recommendations for storing, scheduling, and publishing notebooks"_ including automatic notebook versioning and remote storage handling; [commuter](https://github.com/nteract/nteract/tree/master/applications/commuter) is an _nteract_ server that _"reads notebooks from a local directory or Amazon S3, has a directory explorer to find notebooks, and provides a Jupyter compatible version of the contents API"__\[what "contents AP"I? — Ed.\]_.  
  
_\[I'd love to see an architecture diagram showing how the all the nteract pieces, erm, interact... Anyone? Anyone? —Ed.\]_  
  
Within a JupyterLab environment, the _[jupyterlab-quickopen](https://github.com/parente/jupyterlab-quickopen)_ extension allows you to _"quickly open a file in JupyterLab by typing part of its name"_ _\[h/t/ @ChekosWH\]._  
  
If it's a **notebook gallery** _service_ you're looking for, [nbgallery](https://github.com/nbgallery/nbgallery), a multi-user application that offers notebook storage and sharing, as well as the ability to launch notebooks onto a remote notebook server _may_ be worth looking at. (_I think... I didn't manage to get any notebooks uploaded to my test install due to an overly aggressive [notebook healthchecker](https://nbgallery.github.io/health_paper.html)!_). Some [extensions](https://github.com/nbgallery/nbgallery-extensions)supposedly let you save notebooks from a Jupyter environment directly into the gallery, but I couldn't get them to run properly either. _Which is to say, I'm having to take pretty much all the [claims about what nbgallery offers](https://gab41.lab41.org/jupyter-notebook-sharing-is-caring-5ed4831d7f71) on trust..._  
  
_nbgallery_ also includes an **Apache Solr** powered search engine and notebook recommender. The repo provides a docker-compose script for running the _nbgallery_ application that makes use of a linked Solr container, so if the _nbgallery_ search / recommender / health checker could be pulled into, a standalone notebook search application, that could be a useful jigsaw piece to have around...  
  
Related to this, notebook search engines in general still seem to be lacking, particularly ones that can do sensible things when returning code or markdown results. With a bit of code dependency profiling, I could imagine a search engine that might even let you run code results. In terms of what's currently publicly and openly available, _nbgallery_ aside, [nbscan](https://github.com/conery/nbscan) is a simple script that lets you search for and print contents of cells in Jupyter notebook, and [sqlbiter](https://github.com/thombashi/sqlitebiter) has [support](https://github.com/thombashi/sqlitebiter/issues/51) for parsing notebook cells into a set of linked SQLite database tables. (I can also imagine something like the _papermill_ summariser having a role to play, for example, searching across notebooks and pulling various charts out of them into a notebook based search report.)  
  
_If you know of any notebook related search solutions, or work on a "Jupyter search engine", please let me know..._  

Example Notebooks and Extensions
--------------------------------

One set of signals I'm looking out for relate to how notebooks integrate with other everyday tools that might help integrate notebook working with other everyday activities. For example, here's a [demo notebook](https://github.com/WillKoehrsen/Data-Analysis/blob/master/slack_interaction/Interacting%20with%20Slack.ipynb) showing how to use the Python Slacker package to interact with Slack. I can so easily imagine this as some IPython magic... _\[I've also wondered before about what a Slack kernel might mean! Or a Slack \\slash command that lets you fire off some code or magic to a Binderhub engine, ThebeLab-, Juniper- or nbinteract-like and get the response returned back to your Slack environment? —Ed.\]_  
  
In terms of notification-style working, _[jupyter-notify](https://github.com/ShopRunner/jupyter-notify)_ provides _"Jupyter magic for browser notifications of cell completion"_. Just prefix a long running cell with _%%notify_ and you'll get a notification when it completes via a browser push notification. And if a browser notification, why not a Slack channel notification?  
  
If you want to have a go at visualising **LIDAR** data, this blogpost (and associated notebook) — [Visualizing LIDAR data with Datashader](http://quorumetrix.blogspot.com/2018/06/visualizing-lidar-data-with-datashader.html) — may help get you started...  
  
If [datashader](https://github.com/pyviz/datashader) is new to you, it's a three step data rasterization pipeline for visualising large datasets. In the first **projection** step, _"each record is projected into zero or more bins of a nominal plotting grid shape, based on a specified glyph"_. In the second **aggregation** step, _"reductions are computed for each bin, compressing the potentially large dataset into a much smaller aggregate array"_. In the third **transformation** step, the _"__aggregates are then further processed, eventually creating an image"_. _\[It'd probably make sense to split the datashder examples out into their own Binderised repo? —Ed.\]_  
  
Alternatively, you may be more interested in [plotting seismic activity](https://towardsdatascience.com/how-to-plot-seismic-activity-with-anaconda-and-jupyter-notebooks-7ed23ce9aa5). Although not strictly a notebook demo, [rayshader](https://github.com/tylermorganwall/rayshader) is _"an open source R package for producing 2D and 3D hillshaded maps of elevation matrices using a combination of raytracing, spherical texture mapping, and ambient occlusion_". It's not currently Binderised, so if you fancy a quick weekend project...  
 

* * *

_**Disclaimer: this newsletter is produced independently of the official Jupyter project.**_  
  
_All errors are down to the editor... Oops.. If I make any that I later become aware of, or I'm informed of, I'll announce them in the first possible issue thereafter. If it's really bad, I'll do a Stop Press/emergency issue._

November 16, 2018

Tracking Jupyter: Newsletter, the Fourth...
===========================================

by Tony Hirst

Welcome to this fourth edition of the _Tracking Jupyter_ newsletter (#TJ4), a week in which the Binderhub team were breaking the news...  
  
You may have noticed I've tagged this newsletter **#TJ4** (it's hopefully self-evident as to why!). Something I need to work out is a social bookmarking system for keeping track of what appears in the newsletter when, and a tagging scheme may help with that.  Logging the rate of adoption of successful ideas as well as the rate of decline of false starts (and more egregious practices, like openwashing) is something high on the to do list. (I may also try to chivvy folk along every now and again...!)   
 

Background and History
----------------------

If Jupyter notebooks are new to you, if you keep seeing old references to IPython Notebooks and wonder how they relate to each other, or if you just want to refer someone to a reasonably comprehensive introduction to them and the **current and historical context** they operate in, I found this great introduction on the DataCamp community blog: [IPython Or Jupyter? A discussion of the evolution of and some of the key differences between IPython and Jupyter](https://www.datacamp.com/community/blog/ipython-jupyter).    
  
If you're putting together an institutional case for adopting Jupyter, it may be worth mentioning the odd award, such as the [2017 ACM Software System Award](https://blog.jupyter.org/jupyter-receives-the-acm-software-system-award-d433b0dfe3a2). Previous recipients include UNIX (1983), TeX (1986), TCP/IP (1991), the World Wide Web (1995), Java (2002) and Eclipse (2011). In terms of notable users and use cases, that post describes how _"the LIGO Collaboration, recipients of the [2017 Nobel Prize in Physics](https://www.nobelprize.org/nobel_prizes/physics/laureates/2017/press.html) for the observation of gravitational waves, offer their data and analysis code for the public in the form of Jupyter Notebooks hosted on Binder at their [Open Science Center](https://losc.ligo.org/tutorials)"_.  
 

News, Calls and Announcements
-----------------------------

An official news announcement this week that [MyBinder.org has served two million launches](https://blog.jupyter.org/mybinder-org-serves-two-million-launches-7543ae498a2a), with 80k launches a week. The post also mentions the availability of redesigned Binder badges to promote your Binderised repo or local Binderhub ([generate your own badge](https://mybinder.readthedocs.io/en/latest/howto/badges.html)). In related news, _repo2docker_ has also just got its own logo...  
  
If you don't believe the numbers, a [daily archive of analytics events](https://archive.analytics.mybinder.org/) from MyBinder.org is now available in the form of daily JSON data dumps, describing what repos were launched when. Also available are [d](http://mybinder-sre.readthedocs.io/en/latest/analytics/events-archive.html)[ocs](http://mybinder-sre.readthedocs.io/en/latest/analytics/events-archive.html) showing how to make use of it.  
  
A new set of Azure Notebook kernel images started to be released this week (beginning Monday, 12th November, 2018) although you [might wonder if it was worth it](https://github.com/Microsoft/AzureNotebooks/wiki/Azure-Notebooks-Fall-2018-Package-Update). For example, the _pandas_ package remains on version 0.19.2, for example (last time I checked, _pandas_ current stable version is in the 0.23s) and _ipywidgets_ stays at 7.2 compared to 7.4 current stable.  
  
Cloud computing using trad servers nowadays is old hat, with providers increasingly providing GPU, and even FPGA, powered servers. If you're using your notebooks to crunch certain sorts of dataset, and/or run certain sorts of machine learning algo, you might find using GPU compute helps speed things up. Which is probably why IBM have announced the forthcoming availability of [GPU-powered Notebooks in Watson Studio](https://medium.com/@chenyi_75002/gpu-powered-notebook-is-coming-to-watson-studio-56876f60c056), with Spark, Tensorflow and PyTorch packages, among others, preinstalled. [Sign up to the waitlist](https://datasciencex.typeform.com/to/oQg9G7).  
  
(On the other hand, if you want to run Jupyterhub on your own computer and make the most of your computer's GPU support, you'll need to tweak the base container. Here's a recipe for that: [Docker and JupyterHub for Deep Learning](https://negativesign.com/blog/2018/11/11/docker-and-jupyterhub-for-deep-learning/).)  
  
If you're looking for a **research software engineering (RSE) position**, in part supporting Jupyter deployments, European XFEL have an opening for a [Software Engineer - Open Science Cloud Developer](https://fangohr.github.io/vacancies.html#software-engineer-f-m-open-science-cloud-developer) on the EC-funded PaNOSC (Photon And Neutron Open Science Cloud) project (deadline: 2nd December, 2018).  
  
(A recent preprint on [Jupyter as Common Technology Platform for Interactive HPC Services](https://arxiv.org/abs/1807.09929) may be relevant to such RSE positions in general.)  
  
A second **call for proposals** for [Jupyter Community Workshops](https://blog.jupyter.org/jupyter-community-workshops-call-for-proposals-26a8417e5b6a) is now open (deadline: 10th December, 2018, 8am Pacific time (1600 UTC)). Workshops "_should involve 1–2 dozen participants over a 2–3 day period, and have a total Jupyter-funded budget of approximately $10,000 to $20,000. Events should be hosted no later than June of 2019._" I checked, and it seems that "_\[I\]t is not required that the proposal be for an event in the US. International proposals are welcome._" You know you want to...  
  
There'll be a [Pangeo tutorial](https://medium.com/pangeo/pangeo-agu-workshop-d9565667ad48) on Wednesday 12th December, 2018 at AGU, the American Geophysical Union's Fall meeting this year. Attendees will get to _"learn about the Pangeo project and how to use some of its core software packages (Jupyter, Xarray, and Dask) for their own data analysis tasks"_.  
 

Shopping Around...
------------------

One of the disadvantages of Chromebooks is that whilst you may be able to run "apps" on them, you can't install desktop software packages. With recent versions of ChromeOS starting to support Docker, you can run containerised applications on your Chromebook if it's powerful enough (a new Pixelbook, for example). And what better demo than a **Jupyter notebook server running on a Chromebook** inside a Docker container: [Pixelbook Revisited: Running Docker Containers](https://hackernoon.com/pixelbook-revisited-running-docker-containers-aa7c742a7dec). _Note: I haven't tried this. If anybody would like to gift me a new Pixelbook so I can try it, I can send you my shipping details..._  
  
Jupyter notebooks are designed to run in a  browser (they're fine in Chrome/Firefox/Safari, but they still don't seem to like Microsoft Edge), so you stand a good chance of being able to run them, for free, on an iPad or your iPhone. But if you prefer an app experience, and are happy to shell out £10.99 more than you have to pay to subscribe to the _Tracking Jupyter_ newsletter (free), the [Juno for Jupyter app](https://itunes.apple.com/gb/app/juno-for-jupyter/id1315744137?mt=8), a **Jupyter notebook client for iOS 10.3+** devices (iPhone, iPad and iPod touch) may provide what you need. Please note - I haven't tried it (my iPod touch and iPad stopped being able to update iOS a long time ago). _Once again, I can let you have my shipping details...!_  
 

Alternative User Interfaces
---------------------------

One of the things I have been waiting to see are new user interfaces built on top of Jupyter protocols — I'd particularly love to see something like [BlockPy](https://think.cs.vt.edu/blockpy/) as a Jupyter client running Jupyter kernels rather than using executing Python code using the Javascript based, client side Python interpreter that is _Skulpt_.  
  
In this regard, last week's release of a Microsoft Visual Studio front end (of a sort) to a Jupyter kernel was interesting (#TJ3). That was an _official_ release, but  it's also good to see projects from "the fringe" (I've been reading Amy Webb...) appearing there too in the form of[neuron](http://blogs.msdn.microsoft.com/uk_faculty_connection/2018/10/29/data-science-in-visual-studio-code-using-neuron-a-new-vs-code-extension/), a community contributed Visual Studio Code extension ([repo](https://github.com/lorenzo2897/vscode-ipe)). Type code snippets in the Visual Studio code editor, and display outputs in interactive cards rendered by the _neuron_ extension. I'm not a Visual Studio user, so it'd be interesting to hear from anyone who is how this compares with Micro official Jupyter support.  
​  
Jupyter notebooks are also supported inside other code editors. For example, the **PyCharm IDE** [load and run .ipynb notebooks](https://www.jetbrains.com/help/pycharm/using-ipython-notebook-with-product.html) inside a panel within the PyCharm environment.  
 

Deployment - Proxies
--------------------

If you're making multiple web services available via a unified online workbench, you probably don't want to upset users by sending them to a variety of _:port_ numbers on the workbench domain. [nbrsessionproxy](https://github.com/jupyterhub/nbrsessionproxy) provides Jupyter server and notebook/JupyterLab extension that launches and proxies an RStudio server process from the Jupyter notebook. So if you want to launch an RStudio environment from a Jupyter one, you can do so. Similarly, [openrefineder](https://github.com/betatim/openrefineder) gives you access to a notebook homepage launched **OpenRefine** instance running inside MyBinder. I also use the more general [nbserverproxy](https://github.com/jupyterhub/nbserverproxy) notebook server extension to proxy web services, which can be handy if you have to run everything through a single port 80; proxied ports appear down the path, such as _http://example.com/proxy/3333/_ for an OpenRefine server on its default port (and in that case, _yes, you do need the trailing slash_).  
  
Alternatively, you may want to run your own proxy as part of a more elaborate environment. One of the things I'm trying to curate as part of an _Institute of Coding_ related project is a set of detailed instructions for installing Jupyterhub in a variety of contexts. From OpenDreamKit, a Horizon 2020 European Research Infrastructure project, there's a [useful looking post](https://opendreamkit.org/2018/10/17/jupyterhub-docker/) describing the deployment of a **JupyterHub server** "targeted to a **medium sized institution** \[00s of users\], with external authentication and containerized components". This docker compose solution has been used to support the Faculty of Science at the University of Versailles. A Traefik container provides a reverse proxy on the front, a Jupyterhub container is configured to use the dockerspawnerand oauthenticator in the middle, and a JupyterLab container, customisable to a local specification, provides the notebook / JupyterLab environment on the back. User data is persisted using Docker volumes and docker networking used to limit external internet access from the user environment. If you fancy trying it out — _let me know how you get on!_ — [here's the repo](https://github.com/defeo/jupyterhub-docker).  
  
As far as proxies go, I've been testing _nginx_ as a proxy server fronting a Jupyter notebook server running inside a course VM on OpenStack, although getting things running [wasn't quite as easy](https://blog.ouseful.info/2018/11/07/getting-the-tm351-vm-running-on-ou-openstack/) as at first I'd hoped. I've still to try the Jupyterhub/Kubernetes/Openstack recipe linked to in [#TJ1](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-first).  
  
The extent to which students and researchers should be able to work with the command line in order to get the piece of software they need to do their project up and running in the first place — it can be "good for them" to know what's going on, you might argue — is sometimes just a distraction. This **CLI tutorial** from Microsoft Azure shows something of what's involved in getting a notebook server running on Azure: [Create a Data Science Virtual Machine with the Azure CLI](https://docs.microsoft.com/en-us/learn/modules/interactive-deep-learning/3-create-a-dsvm-with-the-azure-cli). What sort of course _would_ that sort of activity be useful for? What about all the others?  
 

Corporate Adoption and Support
------------------------------

In [#TJ1](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-first), I linked to a couple of items describing how Netflix are using notebooks across their organisation (more recently, episode 54 of the Data Engineering Podcast goes into even more detail: _[Using Notebooks As The Unifying Layer For Data Roles At Netflix](https://www.dataengineeringpodcast.com/using-notebooks-as-the-unifying-layer-for-data-roles-at-netflix-with-matthew-seal-episode-54/) with Matthew Seal_).  
  
But it's not just Netflix.  
  
[PayPal Notebooks, powered by Jupyter: Enabling the next generation of data scientists at scale](https://medium.com/paypal-engineering/paypal-notebooks-powered-by-jupyter-fd0067bd00b0) describes how staff at Paypal originally got into notebook UIs using Apache Zeppelin, but adopted Jupyter notebooks as a platform in Q2 2017 with 50 initial users, rising to 100 users when the platform was made generally available inside PayPal in February 2018, and growing to over 1,300 by the end of August 2018. A rather more comprehensive presentation given at JupyterCon 2018 ([video replay](https://www.youtube.com/watch?v=KVGrACWVUgE)) provides a walkthrough of their **PPExtensions** functionality, including: a _%csv_ magic that SQL commands on CSV files and another allows data to be published to Tableau; a Github extension that allow notebooks to be pushed and pulled from Github; a scheduler extension that schedules notebooks using _Apache Airflow_; and a pipeline magic that allows pipelines to be defined and run across several separately parameterised notebooks (parameter defaults are defined in the first cell of each notebook in the pipeline), in series or in parallel, using a shared namespace. That said, only the magics have appeared so far in the [publicly released extensions](https://github.com/paypal/PPExtensions) ([docs](https://ppextensions.readthedocs.io)) and the announced [online group](https://groups.google.com/forum/#!forum/ppextensions) looks like it never really properly started... The PRs for Github integration and scheduling seem to have made some progress over the last few days so hopefully they'll be merged soon...   
  
In the meantime, the [githubcommit](https://github.com/sat28/githubcommit) notebook extension looks like it provides **github integration** from a notebook, though I have to admit I haven't tried it yet...  
  
IBM**Pixiedust** is another set of corporately developed notebook extensions for Python and Scala (via a Python-Scala bridge). It adds **support for Spark** in the form of a Spark process monitor, support for installing Spark packages and visualising Spark objects (tables, charts, maps) using a plugin extensible API; data export as CSV or to connected cloud storage service is also supported. The [online demos](http://github.com/pixiedust/pixiedust) are, as you might expect, via Watson Studio rather than via MyBinder, although guidance for local installs is also provided.  
  
_If you know of other companies who have developed magics and extensions to support customised notebook environments for use within the organisation to support organisational workflows, and either open or closed code, please let me know..._  
 

Interfacing With Data Stores
----------------------------

One of the ways Apache Zeppelin ([#TJ2](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-second)) distinguishes itself from Jupyter notebooks is through the range of native interpreters that allow it to connect to a wide range of data sources. If it's just the connectivity you want, [_Apache Drill_](http://drill.apache.org/) may help with that in a Jupyter context. If you haven't come across it before, Apache Drill is a rather wonderful (if clunky to set up) query engine that lets you _"treat your data like a table even when it's not"_ and provides you with SQL query interface to pretty much everything. The [Jupyter Drill](https://github.com/JohnOmernik/jupyter_drill) extension provides some simple notebook magic for running _Apache Drill_ queries from a notebook ([about](https://mapr.com/blog/mining-the-data-universe/), [installation](https://mapr.com/blog/mining-the-data-universe/)). If you're looking for a small Binder-it project, this would be a useful one to do: as well as the demo itself, it'd also template how to Binderise an extension that calls on a third party service running in the same container...   
  
Alternatively, integration with external datasources such as Teradata and Apache Hive as provided by the _PPExtensions_ magics draws on the power of [gimel](https://gimel.readthedocs.io/en/master/), another open source offering from PayPal. _gimel_ provides data access from a wide range of storage backends: HDFS, GS, Alluxio, Hbase, Aerospike, BigQuery, Druid, Elastic, Teradata, Oracle, MySQL, SFTP.  
  
If you run **BeakerX**, the Jupyter notebook environment that runs JVM kernels, the **SQL kernel** provides another way of connecting to SQL databases. Queries are run via code cells, returning results in a rich table display that supports sorting, filtering, cell highlighting and CSV export. _%%python_ magic allows you run with the data returned from a query and wrangle it in a Python context.  
  
There are also several **SQL magics** for IPython kernels that provide support for running SQL queries against connected relational databases: [ipython-sql](https://github.com/catherinedevlin/ipython-sql) is the original stalwart; [SQLCell](https://github.com/tmthyjames/SQLCell) looked like it might start to offer a range of richer output and analysis features although it now appears to have stalled without Python3 support. As well as standard SQL database connections, [sql\_magic](https://github.com/pivotal-legacy/sql_magic) provides additional support for connecting to Spark or Hive.  
  
If Apache Zeppelin doesn't work for you, maybe _Jupyter + Apache Drill_, or _Jupyter + PPExtensions + gimel_ or one of the magic alternatives will?  
  
In terms of overall system diagrams, custom kernels, or query layers masked with magic inside the notebook, that provide access to arbitrary data stores round the back, or even further off-stage, is an architectural pattern that keeps repeating.  
 

Notebooks in Action
-------------------

An increasingly common use of notebooks is to use them to present tutorials to demonstrate how to perform particular computational tasks, and along the way require a log in to a particular cloud based platform or API... (Give away the code, but tie it to a paid for platform in some way.) For example, IBM have just released a two part, notebook based tutorial on Github exploring image classification using convolutional neural networks and Keras ([part 1](https://github.com/IBM/image-classification-using-cnn-and-keras)) and Tesseract OCR and IBM Watson Natural Language Extraction _(other cloud based NLP services are available! —Ed.)_ for information extraction([part 2](https://github.com/IBM/image-recognition-and-information-extraction-from-image-documents/blob/master/README.md#3-text-extraction-using-optical-character-recognition)). What's interesting from the Jupyter perspective is that it's Jupyter notebooks that provides the glue and the environment people actually experience. If analysing business data is more your thing, they also have also have [customer churn analysis](https://github.com/IBM/Client-Retention-Through-Data-Analysis-On-zOS) demo. You can find more examples if you [filter the IBM Github repos by _Jupyter notebook_](https://github.com/IBM?utf8=%E2%9C%93&q=&type=&language=jupyter+notebook). And if you want to give quantum computing a go, IBM also make available a set of [tutorial notebooks](https://github.com/Qiskit/qiskit-tutorial) for QISkit, their cloud based quantum computing simulator.  
  
Corporate demos aside, a big part of the attraction for me of Jupyter notebooks is how they are being used across the academy. If economics is your field, the new [QuantEcon Notes](http://notes.quantecon.org/) might be worth a look — they've just opened up an open notebook library for economic modelling for collating economics related notebooks. ([QuantEcon](https://quantecon.org/) is a NumFOCUS project _"dedicated to development and documentation of modern open source computational tools for economics, econometrics, and decision making"_).  
  
And its not just the academy, but the wider GLAM community too. From the **British Library**, a set of Binderised [LibCrowds Notebooks](https://github.com/LibCrowds/notebooks) for exploring the _[LibCrowds](https://www.libcrowds.com/)_ platform, which hosts several experimental crowdsourcing projects related to British Library collections.  
  
Even more widely, notebooks provide an element of transparency in **data journalism** investigations as this handy round up of [notebooks from the LA Times Data Desk](https://github.com/datadesk/notebooks) shows.   
  
If it's something a bit more visual you need to take inspiration from, [3D Slicer](https://www.slicer.org/) is an open source software platform for medical image informatics and 3D medical imaging. [Slicer code can be run in Jupyter notebooks](https://discourse.slicer.org/t/jupyter-notebooks-are-now-usable-in-3d-slicer/3438) and the resulting slicer/3D views rendered in code output cells. [Try it out on MyBinder](https://github.com/lassoan/SlicerNotebookDemos).  
  
Alternatively, but still in the biological domain, if you fancy giving _[BioJava](https://biojava.org/)_, an open source Java framework for bioinformatics, a spin, there's a Binderised [BioJava notebooks demo](https://github.com/sbl-sdsc/biojava-notebooks) available. Among other things, this shows how to get started using a Java Kernel developed by the BeakerX project.

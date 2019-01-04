November 30, 2018

Tracking Jupyter: Newsletter, the Sixth...
==========================================

by Tony Hirst

Welcome to this sixth edition of the _Tracking Jupyter_ newsletter (#TJ6). Time's been tight for me this week, so a handful of items I'd intended to group in various ways for this week's newsletter have been rolled over to future issues...  
 

Releases and Announcements
--------------------------

One for the mapmakers: the [latest release](https://scitools.org.uk/cartopy/docs/latest/whats_new.html#what-s-new-in-cartopy-0-17) (v. 0.17.0, 16th Nov 2018) of cartopy includes prettified support for displaying projection objects in Jupyter notebooks.  
  
Possibly also relevant to Python notebook users, I note a [new release](https://github.com/h2oai/datatable/releases/tag/v0.7.0) (v0.7.0, 16th November, 2018) of datatable, _"a Python package for manipulating 2-dimensional tabular data structures (aka data frames), close in spirit to pandas or SFrame, closely related to R's data.table,  with specific emphasis on speed and big data support"_.  
  
Scripted Forms, the markdown to interactive form rapid application generator that lets you _"q__uickly create live-update GUIs for Python packages using Markdown and a few custom HTML elements__"_, also [bumped up](https://github.com/SimonBiggs/scriptedforms/releases/tag/v0.10.0) to v0.10.0 (22nd November, 2018). If you haven't tried it, I had [lots of fun](https://blog.ouseful.info/2018/04/25/scripted-forms-magic/) when I first played with it... There's an [issue](https://github.com/SimonBiggs/scriptedforms/issues/284) with the current version not working correctly with JupyterLab and a current discussion about [possible deployment routes](https://github.com/SimonBiggs/scriptedforms/issues/278#issuecomment-441146505) if anyone fancies chipping in...  
  
Amazon made a shed load of AI related announcements over the last few days, (I wasted too much time looking through their AI model catalogue) but I've only spotted one so far that related to the **Amazon SageMaker notebooks**, which was that they now support [Git integration](https://aws.amazon.com/blogs/machine-learning/amazon-sagemaker-notebooks-now-support-git-integration-for-increased-persistence-collaboration-and-reproducibility/). More generally, if you want to know how to apply machine learning and deep learning in Amazon SageMaker, there are [notebook examples](https://github.com/awslabs/amazon-sagemaker-examples).  
  
A [post](https://github.com/jupyterlab/jupyterlab/issues/5548#issuecomment-442545500) in the issue thread associated with the **JupyterLab DataBus** mentioned last week ([#TJ5](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fifth)) clarified _"that this project will focus on the JLab frontend and visualization of data, not on data processing and data exchange among kernels"_.  
  
Via the [official Jupyter blog](https://blog.jupyter.org/outreachy-jupyter-supporting-diversity-in-open-communities-dfa78db4b0bd), _"__Project Jupyter has accepted 2 interns through the Outreachy program — an internship program coordinated by the Software Freedom Conservancy — which supports open community members from under-represented backgrounds"_. The interns will be working on a highly available proxy for JupyterHub using Traefik and better native user management features for   
  
**IPython 7.2** has just been [released](https://ipython.readthedocs.io/en/stable/whatsnew/version7.html#ipython-7-2-0), with minor bugfixes, improvements, and new config options.  
 

Making Sense of IT
------------------

One of the reasons I started the _TrackingJupyter_ newsletter was to try to get a feel for how enterprises are making use of Jupyter tools, both in terms of use cases and IT architecture, as well as the **paths to adoption** and **routes to deployment**. A presentation from the Chief Architect at the Center for Open-Source Data and AI Technologies (CODAIT), and previously Chief Architect at the IBM Spark Technology Center, on [The Five Stages of Enterprise Jupyter Deployment](https://www.slideshare.net/FrederickReiss/the-five-stages-of-enterprise-jupyter-deployment) identifies four key challenges (_multi-user collaboration, large scale data analysis, security and authentication, auditing and data access control_) and the following five stages: _denial_ (so why's it useful for the user?), _anger_ (base proposition is single user personal notebook server), _bargaining_ (requirements from all directions), _depression_ and finally _enlightenment_ **Jupyter Kernel Gateway**. So yes, it's a plug for the [Jupyter Kernel Gateway](https://jupyter-kernel-gateway.readthedocs.io/en/latest/), as originally developed for IBM production use, as well as IBM services, but no-one ever got fired for reading through an IBM presentation, right? And the blocking issues identified may resonate with some who've already faced a similar situation, or provide a heads-up for others looking to go down a similar deployment path.  
  
_If your org has been through, or is going through, a scoping exercise relating to Jupyter adoption and/or deployment, and there's a blog post or public report arising from it, please share it along...:-)_  
 

Alternative Notebook Document Formats
-------------------------------------

Anyone working with Jupyter notebooks in a _git_ context knows that things can become messy when reviewing code changes. The _.ipynb_ notebook format is a JSON format with a lot of structural elements and clutter that can make it confusing when trying to commit just the change you want, whilst at the same time not breaking the notebook document structure format by failing to commit essential structural elements that may be associated with the intended commit.  
  
Over the years, several converters have appeared that can transform between notebook JSON and a python+markdown equivalent (think something like _Rmd_ but for Python), although none have really gained any traction. Examples include [ipymd](https://github.com/rossant/ipymd), [podoc](https://github.com/podoc/podoc) (an experimental "pandoc for notebooks", a handy complement to [nbconvert](https://github.com/jupyter/nbconvert), and with added steroids when you factor in pandoc too, with which it shares the same internal intermediate document representation), [notedown](https://github.com/aaren/notedown) and [pynb](https://github.com/minodes/pynb). With a little bit of string and glue, you can then come up with recipes that allow for things like [converting Rmd to notebooks](https://bl.ocks.org/ramnathv/10012123), as well as roundtripping between them.  
  
Via _PyParis 2018_, I came across a more recent offering, and one of the most complete I've seen, at least in terms of demonstrated workflows: [jupytext](https://github.com/mwouts/jupytext) (the [slides/script](https://github.com/mwouts/jupytext_pyparis_2018) are available, as is a [video replay](https://www.youtube.com/watch?v=y-VEZenk824) which is well worth a watch over a coffee). Document handlers can be registered with Jupyter notebooks or JupyterLab that allow a notebook to be background saved in both _.ipynb_ and Jupytext (py+md) _.py_ files ("paired notebooks"), and Jupytext _.py_ files to be opened directly as notebooks. Run the [demo on MyBinder](https://mybinder.org/v2/gh/mwouts/jupytext/master?filepath=demo) and click on the _Paired Jupyter notebook and python script.py_ link (that is, a _.py_ file. Or the _World population.md_ markdown file. Or the _World population.Rmd_Rmd file. Good, eh? And if that's not enough, you can also _turn a GitHub repository containing Sphinx-Gallery scripts into a live notebook repository_. One of the the things that appealed to me were the paired notebooks: changes can be tracked using the "input cell only" Python or markdown document formats, and full notebooks with output cells replete saved as a previewable, executed co-document. I think need to take the dog on a _very long walk_ to think this through...  
 

Kernel Execution Models
-----------------------

One of the arguments made against Jupyter notebooks, and arguably one of the dirty little secrets that can trip up unaware novices, as well as more seasoned practitioners, is that cells can be executed in any order, and (historical) cell outputs may not reflect the the current state of the underlying kernel.  
  
Observeable notebooks ([#TJ1](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-first)) _"__function like a spreadsheet, where cells (like formulas) run automatically whenever their referenced values change. Observable runs cells independently of their order in the notebook"_ ([How Observeable Runs](https://beta.observablehq.com/@mbostock/how-observable-runs)). An [Observeable notebook visualiser](https://beta.observablehq.com/@mbostock/notebook-visualizer) can be used to display the cell execution graph.  
  
The [Jupyter Dataflow Python kernel](https://dataflownb.github.io/) ([repo](https://github.com/dataflownb/dfkernel), Binderised example available) attempts to provide a similar execution model in the Jupyter context, by creating unique persistent IDs for each code cell and _"implementing a recursive dataflow mechanism for cell execution: if a cell references the output of another cell, the kernel will check if cell is up-to-date and execute it if it is not"_. If you change an upstream cell, a downstream cell that depends on it is not recalculated automatically but is flagged to demonstrate an upstream dependency has changed. A [dependency graph viewer](https://dfkernel.readthedocs.io/en/latest/dep-view-tutorial.html) is also provided. See also the related JupyterCon presentation: [Supporting reproducibility in Jupyter through dataflow notebooks](https://www.youtube.com/watch?v=xUZGP2dGRKQ) and the Binderised demo.  
  
Alternatively, _[reactivepy](https://github.com/jupytercalpoly/reactivepy)_ provides a **reactive Python kernel** in which dependencies between variables are tracked such that if the value of one variable is changed, any cells which use that variable will be recalculated with the updated value. _"Each notebook cell for a reactive kernel contains a single definition of a variable, function, or class. When a cell is run, the kernel conducts static analysis to automatically extract and run dependencies -- saving users the trouble of remembering dependencies and re-running individual cells."_ Sounds interesting, but I couldn't get it to work on MyBinder.  
  
Another package, [RxPY](https://github.com/ReactiveX/RxPY) — **Reactive Extensions for Python** — provides a library _"for composing asynchronous and event-based programs using observable collections and LINQ-style query operators in Python; developers represent asynchronous data streams with Observables, query asynchronous data streams using operators, and parameterize concurrency in data/event streams using Schedulers."_ I have no idea what that means either, and I really need to make time to play with it to get a feel for what it enables...  
 

Jupyter Goes 3D
---------------

In [#TJ4](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fourth) I described a recipe from _OpenDreamKit_ for medium sized, containerised JupyterHub deployments. It seems the _OpenDreamKit_ folk are also active on the user tools front, as the [K3D-jupyter](https://opendreamkit.org/2018/10/28/3d/)3D visualization package demonstrates. A particularly nice feature is that K3D plots are _ipywidgets_ — it's going to be increasingly interesting to see how that framework builds out with community created extensions. The K3D notebook and lab extensions can be installed from a single pip package (_k3d_) and the code is available via a [Github repo](https://github.com/K3D-tools/K3D-jupyter).  
  
Via news around _PyParis 2018_, I came across [_ipyvolume_](https://github.com/maartenbreddels/ipyvolume), a WebGL powered _ipywidgets_ based 3D plotting extension for Jupyterlab  ([lightning talk video](https://youtu.be/tyMzLxSO-NA?t=1305)). If that's too distracting, the TLDRTDDW(?!) summary is that _ipyvolume_ offers interactive 3D plots of scatter plots, quiver plots, meshes (surfaces/wireframes), volume rendering eg 3D _numpy_ array and isosurfaces. It's good for a million points or so with a high grade graphics card; if you have time series data available, it'll interpolate between keyframes to animate your data for you.  
  
Unfortunately, the widgets don't seem to work in Azure Notebooks; I think this may relate to a long standing [issue](https://github.com/akaihola/jupyter_abc/issues/2) I've noticed with other extensions that load additional asset files... Expecting extension writers to tweak their code that runs fine elsewhere so that it runs in a Microsoft environment too is something we've seen before, I think? _\[Cough, browser standards, cough... —Ed.\]_  
 

Extension Examples
------------------

**ESASky** is _"an application that allows you to visualise and download public astronomical data from space-based missions"_. It's glossy, and shiny, and handy for browsing over a coffee, but not ideal for getting work done. Step in the[ESASky Jupyter widget](https://github.com/fab77/pyesasky), which allows you to script interactions and use the ESASky application as a display widget. It's very clunky in a notebook (the widget is fixed in the output cell into which it's created) but I could see this making for a nice JupyterLab extension, with the widget ripped into its own panel and controlled from a parent notebook.  
  
An extension that _does_ work in the JupyterLab context is [jupyterlab-drawio](https://github.com/QuantStack/jupyterlab-drawio) which allows you to embed the **draw.io** drawing package in a JupyterLab window. I'm not sure how useful (or interesting) this is, other than as an example of how to use JupyterLab as a universal environment for launching standalone web apps. One use case might be to draw a diagram, save it, then include the generated image file in a notebook or markdown document, for example, all from within the JupyterLab environment. There don't appear to be any callbacks via the widget mechanisms into other Jupyter docs, but I guess the overall package structure may act as a useful code pattern for other integrations.  
  
A recent preprint on arXiv, [A Notebook Format for the Holistic Design of Embedded Systems](https://arxiv.org/abs/1811.10820), describes the use of notebooks for **embedded system specification** using _pCharts_, a "visual formalism for embedded systems", enabled via a custom Jupyter extension: [pstate-jupyter](https://gitlab.cas.mcmaster.ca/lime/pstate-jupyter).  
 

Integration
-----------

New to me (but then again, so much is...), [_Flare_](https://www.cresset-group.com/flare/) is a computational chemistry environment for supporting structure based molecule design (I think?!). And now, via a Python extension, it supports [integrated Jupyter notebooks](http://upflow.co/l/kvCf/2018/11/jupyter-notebook-flare). Is _"Jupyter Inside"_ a pattern we'll be seeing more of?  
  
_Trend-wise, there are various things to watch out for: on the one hand, __integration of panels within JupyterLab that display windows or outputs from other environments or simulators__; on the other,__ panel based environments that can integrate a notebook panel, with communication across panels via the command line or shared files__. Some time ago, I explored how to control the [VREP simulator](https://github.com/psychemedia/ou-robotics-vrep) from a notebook, as well as how to embed video streams from the simulator back in the notebook. Something like that could work really well as a JupyterLab extension, for example? Alternatively, I could also imagine the simulator embedding a notebook UI with integrations enabled that allow it to control the simulator models and displays._  
 

Example Notebooks
-----------------

[Me\_Bot](https://github.com/Spandan-Madan/Me_Bot) is _"a simple tool to make a bot that speaks like you, simply learning from your WhatsApp Chats"_. The code makes use of a simple Tensorflow model and is provided via a notebook...  
  
You might think using [notebooks in a Classics context](https://github.com/clemsciences/old_norse_notebook/blob/master/j%C3%B6tunn.ipynb) to study some Old Norse texts isn't a typical use of Jupyter notebooks, but then again: maybe this is _exactly_ the sort of thing you'd expect to see notebooks being used for, to wit, providing a literate computational tool environment across all subject areas. Alternatively, the [Computational Assyriology project](https://github.com/niekveldhuis/CompAss) _"provides examples of Assyriological research questions that can be approached computationally"_. So if you fancy playing with **cuneiform** in notebooks, there's no reason not to...  
  
Returning to theme of notebooks for working with AWS services, a Medium post on [Using Jupyter Notebooks as your cloud IDE for DevOps](https://medium.com/@guyernest/using-jupyter-notebooks-as-your-cloud-ide-for-devops-a49c03e5cb3f) explores how to use a Jupyter notebook to interactively develop an **AWS Lambda function** and then use shell commands within a notebook to deploy it.

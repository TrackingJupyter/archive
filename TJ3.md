November 09, 2018

Tracking Jupyter: Newsletter, the Third...
==========================================

by Tony Hirst

Welcome to this third _Tracking Jupyter_ newsletter. If you have news for future releases (thanks to the contributors to date) please get in touch...  
  
This edition of the newsletter is rather long (I'm trying to find a workflow and a balance...). It also feels a bit wordy to me: there's a bit more context setting and review and an element of catch up around some Jupyter related things that have been out there some time, that I want to get into the _Tracking Jupyter_ archive... I've started experimenting with **strong emphasis** (bold font) on topic terms to help the skimreaders. Feel free to let me know how you get on with it (and particularly if you don't...). That said, there are announcements — and things worth tracking — appearing every day...  
 

Sign-Up Opportunities / Upcoming Events
---------------------------------------

[JupyterDay in the Triangle](https://libcce.github.io/TriangleJupyter/),The Carolina Club at UNC (University of North Carolina), Chapel Hill, US, November 13, 2018, 09.00-17.15. The [programme](https://libcce.github.io/TriangleJupyter/2018/10/23/announcing-full-program.html) features over 20 **talks**, including what look to be several vendor inspired ones \[_contributed: Chris Erdmann_\]. _Tracking sponsors and the titles / topics of vendor provided talks at Jupyter heavy events could start to be instructive, I think..._  
  
[_PyData_ Bristol](https://www.meetup.com/PyData-Bristol/), Ovo Energy, Temple Quay, Bristol, UK, November 13, 2018, 18.30-21.00. **Talks** include Enrico Rotundo on _"JupyterLab & its extensions: towards a broad open source ecosystem"_.  
  
The **user research** team for IBM's [_Pixiedust_](https://www.ibm.com/cloud/pixiedust) open source notebook productivity tool are looking for user testers: [find out more](https://www.reddit.com/r/learnpython/comments/9vf6z6/data_scientists_and_python_developers_wanted_for/).  
  
The newly announced [Google AI Hub](https://cloud.google.com/blog/products/ai-machine-learning/introducing-ai-hub-and-kubeflow-pipelines-making-ai-simpler-faster-and-more-useful-for-businesses), a one stop-shop for Google's AI and ML tools, integrates Jupyter notebooks: [sign up for the alpha](https://cloud.google.com/ai-hub/).  
 

General News and Views
----------------------

As part of a **community development** effort, the Jupyter core team have launched an [official Jupyter Community Forums site](https://discourse.jupyter.org/). This complements the current Gitter channels and Jupyter Github repositories as a place to engage. The comms strategy has been a bit all over the place to date, particularly if you aren't comfortable asking questions of developers (although I've always found everyone to be open and helpful). If you have an interest in Jupyter, I'd encourage you to introduce yourself [here](https://discourse.jupyter.org/t/introduce-yourself/17/29) and help contribute to, as well as learn from, the nascent community there.  
  
The _Nature_ article mentioned in [last week's newsletter](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-second) has been getting lots of love on social media, but an article from earlier this year in The Atlantic — [The Scientific Paper Is Obsolete](https://www.theatlantic.com/science/archive/2018/04/the-scientific-paper-is-obsolete/556676/) — further sets out the **historical context** for notebook based scientific publishing. The Atlantic article also prompted Paul Romer to an outspoken piece of personal notebook advocacy in his blog post [Jupyter, Mathematica, and the Future of the Research Paper](https://paulromer.net/jupyter-mathematica-and-the-future-of-the-research-paper/): "_Mathematica failed, despite technical accomplishments, because the norms of its developers clashed so obviously with the norms of its intended users. Jupyter is succeeding because the norms of the community that is developing it are aligned with the norms of its users._" (Romer was previously Chief Economist and Senior Vice President of the World Bank and co-recipient of the 2018 Nobel Memorial Prize in Economic Sciences for "_integrating technological innovations into long-run macroeconomic analysis_".)  
  
Relevant to the **skills development** agenda, and activities that can promote and/or benefit from the use of Jupyter notebooks, I notice that [Library Carpentry](https://librarycarpentry.github.io/) has joined Software Carpentry and Data Carpentry and been accepted as an official Carpentries Lesson Programme ([announcement](https://carpentries.org/blog/2018/11/welcoming-library-carpentry/)). The Library Carpentry folk also maintain an [awesome list](https://github.com/LibraryCarpentry/awesome-jupyter-glam/blob/master/README.md) of Jupyter notebook projects and guides in the GLAM (Galleries, Libraries, Archives, and Museums) community ("awesome lists" are _a thing_...).  
 

Preprints
---------

One for the **research librarians**: [Ten Simple Rules for Reproducible Research in Jupyter Notebooks](https://arxiv.org/abs/1810.08055). The first rule sets the scene of using notebooks as a narrative device: _Rule 1: Tell a Story for an Audience_. The next encourages you to explain your work as your go along: _Rule 2: Document the Process, Not Just the Results_. For the rest, I guess you'll just have to click through...  
 

Online Hosted Notebook Environments
-----------------------------------

There are several of them out there... My intention is to mention, as catch-up, one or two a week, so you can try them out one at a time if they're new to you, rather than swamp you with too many to try out in one go... As new platforms are released, I'll try to share them as news items.  
  
Last week, I mentioned _Apache Zeppelin_, a query engine fronting alternative to Jupyter Notebooks. This week's offering is from Google: _Colab_. In many respects, [Google Colab](https://colab.research.google.com/) can be thought of as a notebook equivalent to Google Docs or Google Sheets. Derived from an earlier (now deprecated) Jupyter project (_Jupyter CoLaboratory_ — github.com/jupyter/colaboratory), but now an official Google project with a closed codebase, files are saved to Google Drive and support for **collaborative editing**, with multiple users editing the same notebook at the same time. A handy code snippets tool provides boilerplate code for a range of common tasks, such as generating interactive charts using various Javascript chart frameworks. As well as being a space to run your own notebooks, Google also appear to be exploring its use as a home for live / executable documentation / tutorials (example: [Android Management API - Quickstart Guide](https://developers.google.com/android/management/quickstart); see also this [brief review of Google Colab](https://blog.ouseful.info/2018/09/28/notebooks-seep-into-the-everyday/)), a signal that I think is worth tracking...  
 

Notebook Fronted Deep Learning / AI / ML Deployments
----------------------------------------------------

In passing, I spotted a _Towards Data Science_ Medium blog post by Jeff Hale reviewing the **hosting / compute costs** associated with environments that let you use Jupyter notebooks to run deep learning models on rented servers. It's a clumsy, clickbait title — [Best Deals in Deep Learning Cloud Providers](https://towardsdatascience.com/maximize-your-gpu-dollars-a9133f4e546a) — but it covers the bases, reviewing relative costs of running _TensorFlow_ & _Keras_ (Google warez) or _PyTorch_ (Facebook) & _FastAI_ on cloud hosted GPUs from _Google Colab_, _Google Cloud_, _AWS EC2,_ _Paperspace_, _vast.ai_ and _Kaggle_. _Amazon Sagemaker_ priced itself out pennywise, and _IBM Watson_ and _Microsoft Azure_ _"both failed the easy to setup test miserably"_. My takeaway of the TL:DR recommendation is to go for _vast.ai_ if you can forego data privacy, _Google Cloud_ to scale-up, _but I can't really comment based on the lack of my own personal experience of using the services referred to in that way..._  
  
If you do want to use **Amazon SageMaker**, (it provides [Amazon Sagemaker notebook instances out of the can](https://docs.aws.amazon.com/sagemaker/latest/dg/nbi.html)), a recent blog post shows how to get started in the context of the _Amazon Neptune_ graph database: [Analyze Amazon Neptune Graphs using Amazon SageMaker Jupyter Notebooks](https://aws.amazon.com/blogs/database/analyze-amazon-neptune-graphs-using-amazon-sagemaker-jupyter-notebooks/). In a follow on post, which appears to be the first in a series — [Let Me Graph That For You – Part 1 – Air Routes](https://aws.amazon.com/blogs/database/let-me-graph-that-for-you-part-1-air-routes/) — the same approach of prompting you to launch an AWS free tier machine, and then fire up a notebook server, is in play. The notebook style UI is not going to disappear; indeed, there are signs that it will become ubiquitous and widely familiar...  
 

Notebook Productivity
---------------------

Something I've noticed recently is that Github **notebook previewer** is struggling to load at times (Github will render notebook previews as static HTML). In such cases, I tend to drop the URL into [nbviewer](http://nbviewer.jupyter.org/) and preview the notebook there (see also: [_nbviewer_ extensions / bookmarklet](http://jiffyclub.github.io/open-in-nbviewer/)). _nbviewer_ has the added advantage that it will render things like interactive Javascript charts embedded in a notebook in a way that the Github previewer won't...  
  
For previewing notebooks in other contexts, I note that there is an [Azure DevOps Jupyter (.ipynb) notebook renderer](https://marketplace.visualstudio.com/items?itemName=ms-air-aiagility.ipynb-renderer) available (**Azure DevOps** is the latest incarnation of _Microsoft Visual Studio Team Services (VSTS)_). The renderer allows you to select any Jupyter Notebook (_.ipynb_) file in your [Azure DevOps](https://azure.microsoft.com/en-gb/blog/introducing-azure-devops/) git repositories and render them in a preview pane.  
  
If you want to _run_, rather than just preview, a found notebook, a new **Chrome browser extension** released this week — [Open in Colab extension](https://chrome.google.com/webstore/detail/open-in-colab/iogfkhleblhcpcekbiedikdehleodpjo) — allows you to launch notebooks hosted on Github in the aforementioned _Google Colab_. If you want to roll your own extension or bookmarklet, you can try to play a Github hosted notebook by replacing the _https://github.com_ part of the notebook URL with _https://colab.research.google.com/github/_ .  
  
Whilst handy, there are still no guarantees that the notebook code will execute on _Colab_ if the code has package dependencies. Perhaps more useful is the **Open With Binder extension** (available for [Firefox](https://addons.mozilla.org/en-US/firefox/addon/open-with-binder/) and [Chrome](https://chrome.google.com/webstore/detail/open-with-binder/napgohblobncpnagnehjpooinnimhpkc)) which will open a Github hosted notebook using [MyBinder](https://mybinder.org/). If the repository has been suitably defined, the Binderhub launched container will be built along with any dependency packages already installed as specified in the repository.  
  
By the by, there are at least a couple of other **Binderhub instances** out there (the [Pangeo binder](http://binder.pangeo.io/) and the [Gesis Binder](https://notebooks.gesis.org/) from the Leibniz-Institute for the Social Sciences) but it'd great to see more... or perhaps even see a federated mechanism whereby separate institutions can donate server capacity or credits in to the main _MyBinder_ site?  
  
For **Microsoft Visual Studio Code** users, the [October 2018 Release](https://blogs.msdn.microsoft.com/pythonengineering/2018/11/08/python-in-visual-studio-code-october-2018-release/) includes Jupyter support. Notebook _.ipynb_ files are converted into a clunky annotated python file (think something like Rmd but with markdown and code blocks prefixed _#%% \[markdown\] and __#%%_ respectively). Individual cells can be run against a Jupyter kernel launched in the background with markdown and code cell outputs (including charts) rendered in a _Python Interactive_ window.  _I'll round-up some other variants / converters around .ipynb in a future newsletter._  
 

JupyterLab Extensions
---------------------

Although _Jupyter_ notebooks arguably provide the most common way in to the _Jupyter_ ecosystem, the next generation _JupyterLab_ environment, which still features notebooks, but in a more structured environment, is the user environment where a lot of development effort is currently directed.  
  
A useful overview of **working effectively with Jupyterlab** can be found in this blog post from Florian Wilhelm: [Working efficiently with JupyterLab Notebooks](https://florianwilhelm.info/2018/11/working_efficiently_with_jupyter_lab/). It allays some of the concerns developers used to traditional IDEs might have about working in a Jupyter environment.  
  
Sometimes a live demo makes things clearer... The first seven minutes or so of a video introduction to the newly released **[JuptyerLab Chart Editor](https://www.crowdcast.io/e/introducing-JupyterLab-Chart-Editor/) **provides a handy overview of _JupyterLab_ environment, demoing various filetype renderers (rendering markdown as HTML, or CSV data in a paged, interactive table). The next seven minutes of the video goes on to showcase the new [plotly JupyterLab Chart Editor extension](https://github.com/plotly/jupyterlab-chart-editor), an interactive GUI that makes the online _plotly Chart Studio_ available in offline context within _JupyterLab_ (no need for a _plotly_ account, MIT licensed). (You can dispense with the second half of the video if you just want the gist).  
  
The **chart studio** provides an editor and renderer that manipulates _plotly's_ JSON chart definition files behind the scenes and allows customisation of all chart elements independently of each other (palettes, fonts, labels, and so on). Chart annotations can be added using a point-and-click interface. Charts can be prepared for print publication, e.g. resizing them as desired, and exported as png files. The underlying JSON chart definition file can be load back into Python, whereupon the chart may be exported as an SVG or PDF vector format chart suitable for publication. Apparently, the next version of _plotly_ should support templating, in which case I assume the editor will allow you to create a templated style that could presumably be applied to other charts.  
  
I'm not wholly convinced by the editor — I like notebooks because they let me write down each step in the creation of a chart rather than forget what menus I used to to style bits of a chart when — but the ability to use it to create chart templates that can be shared and reuse elsewhere could be handy. A trend this signals to me is of **web based apps being framed within the _JupyterLab_ environment as filetype registered viewers manipulating files that can be variously process by other _JupyterLab_ components.**  
 

Jupyter Kernels
---------------

If you're looking to use notebooks for teaching statistics, particularly as part of a "traditional" stats curriculum, or your analytics team want to use notebooks to do the sorts of stats that they want to do using languages specifically designed for stats analysis, the default _IPython_ kernel may not be your kernel of choice. But there are a handful of alternative kernels to choose from that may be more appropriate.  
  
For starters, the original **[IRkernel](https://github.com/IRkernel/IRkernel)** is well on it's way to becoming a first class Jupyter environment — Binder can install _IRkernel_ and _RStudio_ by default against a specific version of R on MRAN (_Microsoft R Application Network_, a Microsoft hosted mirror of the CRAN, using _repo2docker_. The [Binder examples repo](https://github.com/binder-examples/r) provides several examples of how to use it as a kernel from a Jupyter notebook (_Jupyter+R_). The demo also shows how **Binderhub runs RStudio** from Jupyter notebooks and how to run **_R Shiny_ apps** in them.  
  
The official [rocker/binder repository](https://github.com/rocker-org/binder) provides an alternative (official?) containerised version of _RStudio_ that runs on Binderhub.  
  
There's also a rival offering, being sponsored by [Bloomberg](http://www.techatbloomberg.com/), in the form of the **[JuniperKernel](https://github.com/JuniperKernel/JuniperKernel) R kernel**. This has been written from the ground up, and also offers **_xwidgets_** integration, so a wide range of rich interactive interfaces should be possible. _(If you have a good demo of xwidgets running in a JuniperKernel notebook, please share it along... There is a demo of [xwidgets running against a C++ kernel](https://github.com/QuantStack/xwidgets). The JuniperKernel repo also seems to be lacking a Binderhub demo if you feel a small PR coming on...)_  
  
If R's not your thing, there's always the **[Stata kernel](https://kylebarron.github.io/stata_kernel/)** \[contributed: _Sergio Sánchez_\].  
  
Or maybe the** [SAS kernel](https://github.com/sassoftware/sas_kernel)** that lets you connect to a SAS environment (either locally, or remotely), execute SAS code and view results inline. If you can make the aforementioned _JupyterDay in the Triangle_ event, I note that _Deep Learning in Jupyter with Python and SAS_ is one of the advertised talks.  
 

Notebooks in Research
---------------------

Here's another trend: **notebooks being used to demonstrate how to get started with various Python packages. **  
  
A recent Medium post described reviewed a new approach for [Land Cover Classification with eo-learn](https://medium.com/sentinel-hub/land-cover-classification-with-eo-learn-part-1-2471e8098195). [eo-learn](https://eo-learn.readthedocs.io/en/latest/) is "_an open-source Python library that acts as a bridge between **Earth Observation/Remote Sensing** and Python ecosystem for data science and machine learning_". Walked through examples of how to use the package are provided using Jupyter notebooks, such as this recipe for [Measuring the water level of a Theewaterskloof Dam in South Africa](https://github.com/sentinel-hub/eo-learn/blob/master/examples/water-monitor/WaterMonitorWorkflow.ipynb). You can also [try the eo-learn demos on Binderhub](https://mybinder.org/v2/gh/sentinel-hub/eo-learn/master) (look in the examples/ folder). To run the notebooks, you need a (free) Sentinel Hub instance ID although I have to admit I couldn't get it to work on a quick first attempt ([issue](https://github.com/sentinel-hub/eo-learn/issues/31)). More elaborate use cases (eg downloading tiles) are billable against AWS credentials to download data from _Requester pays_ AWS storage buckets ([Sentinel Hub configuration](https://sentinelhub-py.readthedocs.io/en/latest/configure.html)).   
  
Another example comes in the form of [pythonOCC – 3D CAD for python](http://www.pythonocc.org/), a Python package for scripting the creation of **3D CAD models.** The installation of all the required packages can be painful and take a long time to build, but if you want to try it, you can, prebuilt (unless the repo has been recently updated!) on Binderhub, as this [pythonocc-binderhub](https://github.com/tpaviot/pythonocc-binderhub) demo shows.  
  
Channeling Rule 9 (_Rule 9: Enable Your Notebooks to Be Read, Run, and Explored_ — you did click through, right?), if you're involved in Python package development, or perhaps R package development, and your code repository is on Github, is it _Binder_ised and does it have a simple _Getting Started_ notebook to introduce it and what it is capable of, a line of code at a time?  
  
**Releases:**  
_Shh, quiet, this isn't really a release at all. More a marker in the sand from which to build future releases: [binderhub v0.1.0 on PyPi](https://pypi.org/project/binderhub/). If you want to try it, word has it that you're probably safer installing from the repo master, at least until 0.2.0 is out..._

December 14, 2018

Tracking Jupyter: Newsletter, the Eighth...
===========================================

by Tony Hirst

Welcome to this eighth edition of the _Tracking Jupyter_ newsletter (#TJ8). One more and that'll be me done for the year...  
 

News and Announcements
----------------------

I spotted this mere seconds too late for last week's mailing: the [PayPal PPExtensions](https://github.com/paypal/PPExtensions) notebook scheduler and Github integration tools are now available in beta. _\[Note to self: do not snark anymore, it only goes wrong... —Ed.\]_  
  
Also following up on the notebook scheduling tools mentioned in [#TJ7](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-seventh), here's a _Jupyter Enterprise Gateway_ [Notebook Scheduler UI Extension](https://github.com/lresende/enterprise_scheduler_extension).  
  
The **KNIME** Analytics Platform (v. 3.7) and KNIME Server (v. 4.8) now [integrate Jupyter notebooks](https://www.knime.com/whats-new-in-knime-37#jupyter-integration).  
  
Azure notebooks[have had a facelift](https://blogs.msdn.microsoft.com/uk_faculty_connection/2018/12/10/azure-notebooks-new-ui-and-project-features-get-you-academic-content-showcased/) in the form of _"a refreshed user interface"._ The _Azure Machine Learning SDK_ has also been made available to the Python 3.6 kernel, which effectively integrates the _Azure Machine Learning Service_ with _Azure Notebooks_. Whilst Azure Notebooks are free to use, other Azure services may not be. But [if you're a student](http://azure.microsoft.com/en-us/free/students/), you can get some free credit to try Azure subscription services out.  
  
It can be difficult knowing where to get started when using notebooks particularly on your own computer. [First Python Notebook](http://www.firstpythonnotebook.org/index.html) is an online text book that takes you through the steps of getting your own environment up and running as well as some of the things you can do once it is running...  
  
Data competition platform **Kaggle** _\[which is to say, Google...—Ed.\]_ published an overview of "[different types of data scientists](https://www.kaggle.com/aamster/overview-of-different-types-of-data-scientists)"  based on their 2018 data science survey which attracted 23,000 or so respondents. Could be handy if you're scoping requirements for a datascience platform. _\[I'm reminded that O'Reilly used to publish a "State of the Computer Book Market" review each year, that among other things introduced me to treemaps. I'd be interested to see a recent version of something equivalent to that. But then, the computer book market is perhaps not as healthy as it once was...—Ed.\]_  
  
A blogpost on the official Jupyter blog announces [first class Binder support for _Stencila_](https://blog.jupyter.org/elife-sprint-integrating-stencila-and-binder-18834e9ad584) arising from an _eLife Innovation Sprint_. If you need a richer editing environment than notebooks provide for writing reproducible research reports, and one with reactive code cells to boot, **Stencila** could work for you. The _eLife Innovation Sprint_ folk have a [write-up](https://elifesciences.org/labs/d42fe2b9/integrating-binder-and-stencila-the-building-blocks-to-increased-open-communication-and-transparency) of the integration too. _\[So how come no-one has produced a similar tool for helping author rich interactive online eduction materials? —Ed.\]_  
  
And [another official post](https://blog.jupyter.org/the-future-of-jupytercon-2019-and-beyond-9e3002faaf48) calls for volunteers from the community for a committee to help decide **the future of JupyterCon** and other Jupyter related organised events (expressions of interest by December 21st, 2018).  
  
The Binder demo for the [reactivepy](https://github.com/jupytercalpoly/reactivepy) kernel ([#TJ6](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-sixth)) now seems to be working. If running a demo is too much for you, at least watch this [animated gif](https://user-images.githubusercontent.com/1448859/49834485-cb293100-fd9c-11e8-9786-c710d51f440c.gif). _\[The folk who complained about notebook history drifting from underlying state will now of course complain that history is lost in notebooks running this kernel whenever they update a cell...—Ed.\]_  
  
**Educational User News**  
  
If you're fishing for an LMS solution, [IllumiDesk](https://www.illumidesk.com/) claims to _"make it easy for you and your students to use Notebooks for your classes so you can get on with teaching"_ with their Canvas LMS + Jupyter offering.  
  
Alternatively, if it's pop-up JupyterHub servers you need to teach a class or workshop, [Hub Hero](https://hubhero.net/) may be able to help you out. For a flat fee, they'll install JupyterHub good enough for a small cohort (up to 30 users) on your own cloud server.  
  
The _Azure Notebooks_ refresh also includes an improved gallery to showcase notebook libraries. So if you're using Azure Notebooks for course delivery, and you're proud of ur warez, why not try to plug them?  
 

Official Releases
-----------------

_repo2docker_ version 0.7.0 came out this week (11th December, 2018) ([release notes](https://github.com/jupyter/repo2docker/blob/0.7.0/CHANGES.rst#version-070)) with support for building images from a repository subdirectory and making edits to a local source repository from a live container.  
 

Corporate Adoption
------------------

I've been holding back on this company in the hope of finding better public examples, but as they keep not appearing, here we go anyway: Bloomberg. For some time, Bloomberg have been active participants in the Jupyter project, sponsoring the Jupyter Community projects and supporting the [bqplot](https://github.com/bloomberg/bqplot) charting library and a [Kerberos authenticator](https://github.com/bloomberg/jupyterhub-kdcauthenticator). If you haven't tried it, _bqplot_ is _"a 2-D visualization system for Jupyter, based on the constructs of the Grammar of Graphics"_. I like the R _ggplot2_ library _a lot_, but have to admit I haven't really got into bqplot, lapsing instead to _pandas_ ._plot()_ methods and _matplotlib_. I probably should give _bqplot_ a proper go...   
  
[Live](https://www.youtube.com/watch?v=i40d8-Hu4vM) [demos](https://www.youtube.com/watch?v=1XTMkcrVyQg) at JupyterCon in 2017 and 2018 from Bloomberg staffers have used a customised Jupyter notebook environment, with stylised black background theme. I'm guessing this is **BQuant**  _\[I've also seen reference to BQNT and or BQNT Notebooks...—Ed.\]_ the _"Bloomberg Analytics and Data Platform"_, a Jupyter notebook based quantitative analysis platform that _"combines data science, quant ready datasets, 'community' features  and integration with the Bloomberg ecosystem, allowing users to easily create, validate, monitor and share investment ideas"_. Bloomberg job ads around the world _("Corporate Adoption, BQuant (Python Data-Science Platform)"_) and _Linked In_ profiles (_"\[d\]esigned a SaaS application for serving Conda packages for BQuant, a Jupyter Notebook based data science platform for financial analysts"_) also keep referring it...  
  
Offhand I couldn't find any product launch announcements, but one [blog post](https://smarterbeta.wordpress.com/2017/10/26/bloomberg_bquant/) reviewing it claimed that "_\[a\]ccording to their sales team, Bquant will be the fifth screen of Bloomberg Terminal"_ and a second announced [JupyterLab support](https://adrian-gao.com/2018/02/13/bloomberg-bqnt-1/). The same blogger also posted a couple of [demo](https://smarterbeta.wordpress.com/2017/10/28/bquant-1-explore-altmans-z-score-with-bquant/) [reviews](https://adrian-gao.com/2018/04/06/bloomberg-bqnt-2/). A [recent interview](https://www.cio.co.uk/cio-interviews/bloomberg-cto-reveals-how-data-science-is-guiding-finance-industry-3686443/) with the Bloomberg CTO doesn't mention notebooks or Jupyter explicitly.  
  
I'm assuming BQuant also integrates with [Bloomberg BQL](https://github.com/business-science/tidyquant/issues/107), the **Bloomberg Query Language**, _"which allows users to perform custom calculations/analysis in the Bloomberg Cloud"_. Integration is provided for Excel users if this [Introduction to BQL Using Bloomberg Query Language in Excel](http://fintools.com/BQL/Introduction_to_BQL_for_Excel%20080718_f%20jb.pdf) guide is anything to go by, so presumably it's integrated within _BQuant_ too _\[Does anyone know if there are custom notebook extensions integrating this? —Ed.\]_  
 

Spreadsheet Like — Direct Data Manipulation
-------------------------------------------

Across many computational data science initiatives, the notion of a 2-dimensional dataframe for representing tabular data is widely used. But spreadsheets continue to dominate, I suspect in no small part because of their "cell editability". Outside the Jupyter ecosystem, RStudio [recently updated Shiny](http://www.bryer.org/post/2018-22-26-dtedit/) to allow for [editable DataTables](https://blog.rstudio.com/2018/03/29/dt-0-4/) _("edit a cell by double-clicking on it"_).  
  
Within the Jupyter context, the [Quantopian qgrid widget](https://github.com/quantopian/qgrid) also supports cell-level editing against a pandas dataframe object representation, although at the cost of losing reproducibility: if you edit dataframe cell values directly via the grid widget, you don't get the option of capturing the line or lines of _pandas_ code that would allow you to replay those changes to the original dataframe programmatically. (Compare this with tools such as [OpenRefine](https://github.com/OpenRefine/OpenRefine/wiki/History) or Columbia Journalism School's [Workbench](http://workbenchdata.com/) ([old review](https://blog.ouseful.info/2018/08/30/linear-cell-based-workflows-with-workbench/)) which do provide you with a stepwise history that can be undone, or exported and replayed.)  
  
On the topic of spreadsheet like direct manipulation, I'm also reminded of the [Python pivottablejs package](https://github.com/nicolaskruchten/jupyter_pivottablejs) which adds an interactive, pandas powered pivot table widget to Jupyter notebooks. Again, one of the issues I had with that widget was that the manipulation steps were locked into the widget and that you couldn't get a history of _pandas_ operations that would replay a manual set of actions programmatically. For reproducibility, some mechanism for recording and exporting-as-code programmed steps triggered from direct manipulation would be handy for reproducibility and another step towards replacing spreadsheets... It would also mean that you could do things like manipulate a pivot table visually, through direct manipulation, and then just "save out" the commands that would reshape your original dataframe to the pivoted form.  
  
By the by, I also notice [ipypivot](https://github.com/PierreMarion23/ipypivot), another Jupyter widget that wraps the same _pivotTable.js_ package. This does allow you to save and restore pivot-table settings, as well as programmatically access the manipulated dataframe object as a modified pandas dataframe. Presumably, a workflow _does_ exist in here somewhere that allows you to use this widget as part of an direct manipulation workflow and then immortalise the settings, with data transformations being played through the widget, rather than as exported code step transformations.  
  
_Direct manipulation editors such as these may make even more sense in a JupyterLab context: I could easily imagine ripping a pivot table out of a notebook into its own panel, manipulating it there and updating a dataframe object being analysed and reported on in a notebook. But the risks of breaking reproducibility are high unless some programmatic way of achieving the same data shaping effect was communicated back into the notebook. (I wonder if the mooted JupyerLab databus ([#TJ5](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fifth)) should be able to handle such things? I can see how a pivot table widget could subscribe to a data frame type and returned modified dataframes back, but how could it communicate replayable programmatic transformations back?_  
  
In Stencila, data and formula containing [spreadsheet documents](https://stenci.la/blog/introducing-sheets/) can be created as well as notebooks. The execution context for each spreadsheet cell can be separately defined, so you could define a polyglot spreadsheet (though I'm not sure how cell referencing works in anything other than the default cell context).   
  
Elsewhere, I wonder what the [pyspread](https://manns.github.io/pyspread/) ([repo](https://github.com/manns/pyspread)) Python backed spreadsheet package might look like as a Jupyter client or JupyterLab component? _\[I can't offhand find mention of folk working on this, but I've only made the most cursory of searches. —Ed.\]_ Dedicated alternatives chasers might also be interested in the (deprecated?) [SciSheets project](https://github.com/ScienceStacks/SciSheets) ([2017 SciPy paper](http://conference.scipy.org/proceedings/scipy2017/pdfs/joseph_hellerstein.pdf)) which aimed _"__to deliver the power of programming with the simplicity of spreadsheets"__._ _\[py2.7, so would presumably need some work... —Ed.\]_  
 

Polyglot Notebooks and Kernels
------------------------------

Using magics, it's quite possible to use different code cells in a single notebook to run code from different programming languages. For example, you might blend Python code in the linked kernel in one set of cells, and SQL queries run on a connected database in another set; or mix and match R and Python code in different cells, as demonstrated in the newly released Binder example mentioned in the announcements above.  
  
A blog post (May, 2018) by one of the Jupyter developers — [I Python, You R, We Julia](https://blog.jupyter.org/i-python-you-r-we-julia-baf064ca1fb6) — describes the use of magics to support execution of Python, Julia and Fortran, R bash script and Perl code in same notebook. An official MyBinder [example repo](https://github.com/binder-examples/multi-language-demo) complements the post.  
  
The [BeakerX polyglot magics](https://github.com/twosigma/beakerx/blob/master/doc/groovy/PolyglotMagic.ipynb) provide support for polyglot notebooks via magic block cells. Magics are provided for each of the BeakerX languages: _%%python_, _%%groovy_, _%%java_, _%%scala_, _%%sql_, _%%clojure_ and _%%kotlin_. There is also a _%%kernel_ magic to access any kernel available to Jupyter; widget support is also provided though these magics. [Autotranslation](https://github.com/twosigma/beakerx/blob/master/doc/groovy/AutoTranslation.ipynb) of variable types supports communication between languages (including JavaScript, Python, Groovy, Scala, and SQL) by serializing objects to JSON, although support for **Arrow** and shared memory techniques are on the agenda.  
  
Using magics may be seen as a bit of a fudge, so are there any truly polyglot kernels around, and what would such a thing mean? (Here's an early discussion on [allowing multiple languages in one notebook](https://github.com/jupyterlab/jupyterlab/issues/2815).) A demo at JupyterCon of [Script of Scripts (SoS)](https://vatlab.github.io/sos-docs/), from the University of Texas / MD Anderson Cancer Center supports, amongst other things, a _"Jupyter-based polyglot notebook that allows the use of multiple Jupyter kernels in one notebook"_. A [binderised version](https://github.com/binder-examples/jupyter-sos) is available if you want to try it out. SoS provides a 'super kernel' that can launch and communicate with other kernels ("subkernels") — 11 language subkernels are supported to date — with each cell running code against a selected kernel. _\[An interesting test of SoS might be to see how easy it is to map these Python and C++ scripts that model [processor hardware effects](https://github.com/Kobzol/hardware-effects) into a set of polyglot notebooks. —Ed.\]_ The top SoS kernel, an extended IPython kernel, uses magic to capture responses returned from subkernels and pass them to other subkernels. Best-effort variable type conversion (e.g. using Feather for passing dataframes) is provided for moving state between kernels, either in memory or via file transfer. A [JupyterLab SoS extension](https://github.com/vatlab/jupyterlab-sos) is also available that provides front-end extensions, such as line by line code execution (a code stepper, essentially, with a preview of code output on line by line basis) and a variable inspector. The best way to get your head round SoS is probably to watch a demo, so grab yourself a coffee then sit back and watch the [JupyterCon SoS talk](https://www.youtube.com/watch?v=U75eKosFbp8).  
  
As well as reactive cells _\[downstream cells only seem to update if you change them, and there is no visual clue that such cells have a dependency that has changed? —Ed.\]_ the aforementioned **Stencila** application also supports polyglot notebooks and polyglot spreadsheets using Stencila's own "execution contexts" (which include R, Python, SQL, Node.js and JavaScript) as well as at least the Python Jupyter kernel. A data interchange format allows state to be passed between some execution contexts.  
  
Outside the Jupyter ecosystem, [Wrattler](http://tomasp.net/academic/papers/wrattler/) provides an alternative notebook environment that supports _"reproducible, live and polyglot notebooks"_.  
 

Streaming Video and WebRTC
--------------------------

One of the really attractive features of notebooks (and JupyterLab) is the support for embedding a wide range of media types in Python notebooks at least using the _IPython.display_ machinery. Most of use are familiar with embedding charts and tables, maybe even audio and video files using the built in audio and video player support. But what about streaming video?  
  
[ipywebrtc](https://github.com/maartenbreddels/ipywebrtc) provides a WebRTC extension for Jupyter notebooks/ JupyterLab by the seemingly ever-productive package developer, Maarten Breddels. It allows you to _"create a MediaStream out of any ipywidget, video file, image file, audio file or your webcam/camera"_ from which you can then _"record a movie, image snapshot, or audio fragment, stream it to peers using a simple chat function, or use it as a texture in ipyvolume"_. So for example, you can play a video in notebook, grab a still image frame from it, and then manipulate or process that frame at your leisure. Or record a movie of changing widgets. One more reason to develop widgets as _ipywidgets_, I guess... There's a brief review[here](https://towardsdatascience.com/video-streaming-in-the-jupyter-notebook-635bc5809e85).  
  
On the other hand, if you just want to manipulate a video file using the **ffmpeg** application from within a notebook, the [ffmpeg-python](https://github.com/kkroening/ffmpeg-python)package could be what you're looking for; its claim over other Python _ffmpeg_ wrappers is that it supports complex signal graphs that let you easily apply multiple filters to frames in a video file. The [demo notebook](https://github.com/kkroening/ffmpeg-python/blob/master/examples/ffmpeg-numpy.ipynb) runs with a couple of [minor tweaks](https://github.com/kkroening/ffmpeg-python/issues/147) to Binderise the repo. Based on my tinkering last week with running a _gnuplot-kernel_ from _ThebeLab_, now I'm wondering whether using [_metakernel_](https://github.com/Calysto/metakernel) around an _ffmpeg_ wrapper kernel could be handy?  
 

Interesting Extensions & Notebooks
----------------------------------

If you find yourself using similarly structured notebooks, but don't necessarily want to go down the route of using parameterised notebooks (e.g. using something like papermill), you might find this extension for providing J[upyterLab templates](https://github.com/timkpaine/jupyterlab_templates/) handy for creating new notebooks from notebook templates.   
  
A nice example of getting started with notebooks and using magics can be found in this [tutorial](https://techcommunity.microsoft.com/t5/Threat-Intelligence/Automating-Security-Operations-Using-Windows-Defender-ATP-APIs/td-p/294434) on working with the **Windows Defender Advanced Threat Protection API**. So if you want to _"build automation around hunting scenarios"_ this will show you how. Various magics help the workflow: the _%wdatp\_alert_ magic looks up reports associated with valid WDATP data Alert IDs; and the _%%wdatp\_ip_ magic uses regular expressions to scan a block of text for IP addresses look up reports for any it finds.  
  
If you're curious as to how regular expressions actually work, and fancy refreshing your computer science skills, a [blog](https://reindeereffect.github.io/2018/06/24/regex/)[series](https://reindeereffect.github.io/2018/12/08/recursive-descent-part1/), derived from Jupyter notebooks that allow you to play along, tells you how...  
  
One for the amateur meteorologists: if you've ever wondered how to plot your own **weather maps**, this [set of notebooks](https://github.com/MethaneRain/Weather-Jupyter-Notebooks) will show you. Or if it's contour weather maps you're after, [try this notetebook](https://github.com/stefmarais/contour-weather-map).  
  
And for radio hams, [SigPlot](https://github.com/LGSInnovations/sigplot) is a Javascript package that _"provides fast, interactive plotting for software defined radio applications"_. The [jupyter-sigplot](https://github.com/LGSInnovations/jupyter-sigplot)  extension wraps SigPlot for use in notebooks as a widget.  
 

Handy Tips
----------

Knowing which Python environment to install a package into when using a Jupyter notebook can often be problematic ([issue](https://stackoverflow.com/a/39022003/454773)). This post on [Installing Python Packages from a Jupyter Notebook​](http://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) identifies best practice, but an easier way from the author of that post is coming to IPython with the inclusion of some _%pip_ and _%conda_ magic for installing packages into the current kernel ([PR merge](https://github.com/ipython/ipython/commit/a8165da9102a62203c824f8cb59988e188fc6032)).  
  
If you tend to run your Jupyter environments as Anaconda environments, managing those can be problematic too. In which case, the [nb\_conda\_kernels](https://github.com/Anaconda-Platform/nb_conda_kernels) extension for managing _conda_ environment-based kernels may help.  
  
And finally, effective version control using tools like git is an with Jupyter notebooks because the metadata  and code output elements in the _.ipynb_ JSON file can make it hard to see what changes you actually made to markdown and code cells. This post on [How to Version Control Jupyter Notebooks](https://nextjournal.com/schmudde/how-to-version-control-jupyter) reviews the issues and provides some practical steps for making your life easier in this regard...

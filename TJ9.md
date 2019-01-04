December 21, 2018

Tracking Jupyter: Newsletter, the Ninth...
==========================================

by Tony Hirst

Welcome to this ninth edition of the _Tracking Jupyter_ newsletter (#TJ9). I was in two minds about whether to bother this week, with a holiday week for many upcoming, but then it struck me that one or two of you might be interested in a holiday project, so this newsletter includes several opportunities for doing just that...  
  
In contrast to other weeks, where I try to demo each thing I mention to check it works prior to inclusion, this newsletter is filled with things on my to-do list. But as it's holiday time for many, in case you: a) fancy a project; b) write it up, and c) share a link back to me, I may be able to get a better idea of how these things work rather more vicariously...  
  
_This will be the last newsletter of the year. I'm not sure in what form it will come back next year — in terms of time the newsletters take produce, it's not sustainable when taken alongside other things I've been neglecting, such as posting recipes to [ouseful.info](https://blog.ouseful.info/) and tinkering with WRC motorsport data to feed my [RallyDataJunkie](https://rallydatajunkie.com/) automated journalism site..._  
 

News and Announcements
----------------------

Jupyter notebooks bumped up to 5.7.3 to fix a security issue (there was _"a window of time in which another logged-in user could see the authentication token in command line arguments and authenticate with it before the real user"_) , then quickly after to 5.7.4 to handle a consequent issue. The latest version is available via pip and conda.  
  
The December 2018 release of the _Python Extension for Visual Studio Code_ improves Jupyter integration (originally announced in [#TJ4](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-fourth)), with support for adding connections to remote Jupyter servers and the ability to export Python files as Jupyter notebooks.  
  
Microsoft are also advertising for a [Product Manager for Azure notebooks](https://careers.microsoft.com/us/en/job/552665/Program-Manager-II) to _"manage and drive improvements to the Azure Notebooks free tier, as well as satisfy those customers who wish to pay for additional resources in Azure"_. Tasks include competitive analysis of other Jupyter notebook experiences, identifying customer segments, crafting UX mockup workflows, writing specs, blog posts, and documentation, building demos, and engaging in community development. _\[If you go for it and this is the only place you saw the ad, well, you know, ... —Ed.\]_  
 

Papers
------

Recently posted on Figshare, a paper on [Supporting distributed, interactive Jupyter and RStudio in a scheduled HPC environment with Spark using Open OnDemand](https://figshare.com/articles/Supporting_distributed_interactive_Jupyter_and_RStudio_in_a_scheduled_HPC_environment_with_Spark_using_Open_OnDemand/6887693). This describes [**Open OnDemand**](http://openondemand.org/), _"an NSF-funded open-source HPC portal based on OSC’s original OnDemand portal. The goal of Open OnDemand is to provide an easy way for system administrators to provide web access to their HPC resources"_. If you want to poke around in the detail, here's the [repo](https://github.com/OSC/Open-OnDemand)...  
 

Roll Your Own Jupyter Kernel
----------------------------

[Metakernel](https://github.com/Calysto/metakernel) is a_ "Jupyter kernel base class which includes core magic functions (including help, command and file path completion, parallel and distributed processing, downloads, and much more)"_. It extends [IPython wrapper kernels](https://ipython.readthedocs.io/en/stable/development/wrapperkernels.html) which themselves re-use the IPython kernel machine to make new kernels. The wrapper kernels use _Pexpect_ (cf. [Expect](https://pexpect.readthedocs.io/en/stable/)) to allow scripts to spawn child applications and control them _"as if a human were typing commands"_; which means you can automate against free-standing applications, pass commands to them, retrieve responses from them, and then wrap those responses in the way that the IPython kernel expects to receive them. _Metakernel_ has be used to create a wide variety of kernels, including: _[matlab\_kernel](https://github.com/Calysto/matlab_kernel)_, _[octave\_kernel](https://github.com/Calysto/octave_kernel)_, _[calysto\_scheme](https://github.com/Calysto/calysto_scheme)_, _[calysto\_processing](https://github.com/Calysto/calysto_processing)_, _[gnuplot\_kernel](https://github.com/has2k1/gnuplot_kernel)_ and _[iwolfram](https://github.com/mmatera/iwolfram)_ kernel.  
  
If you fancy a holiday project, why not have a look at creating a wrapper kernel around a command line tool so you can use it as a kernel, via a %magic, or called from an arbitrary web page using something like ThebeLab ([recipe](https://blog.ouseful.info/2018/12/06/jupyter-is-not-just-notebooks/)).  
  
For the more hardcore geeks who want to build a kernel from the bottom up, [Xeus](https://github.com/QuantStack/xeus), a _"C++ implementation of the Jupyter kernel protocol ... meant to facilitate the implementation of kernels for Jupyter._ may be more appropriate ([JupyterCon 2017 presentation](https://www.youtube.com/watch?v=-O6uuqHk34A)).  
  
Not a kernel generator as such, but a slightly different way of thinking about them, [Jyve](https://github.com/deathbeds/jyve) offers a set of run-in-the-browser _"kyrnels"_ that allow you to execute unsecured Javascript or browser based Python code used (using Brython, for example); this presumably means they should work offline, once loaded into the browser (a quick test suggested this does seem to be the case). As the README describes, _"JupyterLab currently disables or limits the scope of of arbitrary JavaScript in output cells, Markdown documents and other places"_ unlike the classic notebook where you could write Javacscript to your heart's content. Jyve kernels can write to their own iframe embedded dedicated DOM and provide scriptable access to the JupyterLab Application instance. As a playground for learning how to work with JupyterLab, this looks like it could be useful.  
 

Reproducible Environments and Binderised Repos...
-------------------------------------------------

_\[If this were a "tracking" report, I'd write this section in a different tone, as a noticing of how Jupyter tools are being used in the wild. But for once, it's an invitation to action...—Ed.\]_  
  
For many people, Jupyter = notebooks, but it's worth remembering that notebooks are just one small part of the Jupyter ecosystem (which is partly why I felt the need to start _TrackingJupyter_). One of the really handy family of tools that have come out of the project relate to (re)creating reproducible software environments._ \[I remember way back when we thought all we needed was open data, then folk realised that was useless for reproducibility without the code. Then they realised the code was often so wound up with a particular environment, they needed the environment too...—Ed.\] _[MyBinder](https://mybinder.org/) is a [Binderhub](https://github.com/jupyterhub/binderhub) instance lets anyone create a running notebook server in Docker containers spawned from a Docker image built from a set of environment definition files, notebooks and datafiles contained in a Github repository. Under the hood, [repo2docker](https://github.com/jupyter/repo2docker) creates the image, a handy little tool that can be used to build images locally, as well doing the grunt work for MyBinder (or other Binderhub servers).  
  
Many Python packages include demo notebooks and the necessary configuration files for running them on MyBinder. But not all of them do... So if your favourite Python package, or notebook repository isn't "Binderised", why not spread some seasonal goodwill and help make it runnable on MyBinder, and perhaps add a couple of notebook demos. See the [MyBinder docs](https://mybinder.readthedocs.io/en/latest/using.html)  and [Binder example repos](https://github.com/binder-examples) for more...  
  
If you're feeling even more confident, you could perhaps contribute an extension that maps some magic round a package in meaningful way to simplify working with it (for example, here's [an extension](https://github.com/psychemedia/ipython_magic_folium) I tried to build around the _folium_ mapping package); or if you want to get really involved with package code, maybe look at extending it with some **\_\_repr\_\_** [formatting machinery](https://ipython.readthedocs.io/en/stable/api/generated/IPython.core.formatters.html#classes) to provide [rich display](https://ipython.readthedocs.io/en/stable/config/integrating.html?highlight=rich%20display#rich-display) notebook outputs when displaying package objects. (For an overkill example, see the [pandas dataframe \_repr\_html formatter](https://github.com/pandas-dev/pandas/blob/master/pandas/io/formats/style.py#L158).)  
  
The _repo2docker_ command line tool is a really handy one to have around, and it's interesting to keep tabs on other tools of this ilk to see where **repo2docker** might go next. For an overview of where is is _now_, see this [introductory blogpost](https://blog.jupyter.org/introducing-repo2docker-61a593c0752d).  One thing I hadn't realised was that if the _repo2docker_ [buildpack](https://repo2docker.readthedocs.io/en/latest/architecture.html?highlight=build%20pack#buildpack) detects you want an R environment, it will automatically install RStudio for you. (You can always use your own Dockerfile if you want to exert more control over what goes into the built container.) If you're new to Docker as well as repo2docker, start here: [Docker for Data Science Without the Hassle](https://towardsdatascience.com/docker-without-the-hassle-b98447caedd8).  
  
The Stencilanotebook project have an similar tool called **[Dockter](https://github.com/stencila/dockter)**, _"a Docker image builder for researchers"_. As with _repo2docker_, _"if the the folder already has a Dockerfile, Dockter will build the image from that. If not, Dockter will scan the source code files in the folder and generate one for you"_. Languages currently handle by _Dcokter_ inlcude R, Python and Node.js, with one or more languages per project.  
  
Both projects seem to draw inspiration from **[source2image](https://github.com/openshift/source-to-image)** (s2i), a _"tool for building/building artifacts from source and injecting into Docker images"_. A rationale for why Jupyter went with their own repo2docker package rather than **s2i** can be found [here](http://words.yuvi.in/post/why-not-s2i/). (A big part of the TLDR is: _repo2docker_ supports composability, so if you want an Python environment and and R or Julia one, you can just add another layer in.)  
  
One of the things I wonder about these image builders is the extent to which they create efficient images, size wise (this may be an issue if you want to run a container on a service with an image size limit, or that is otherwise resource limited (for example, when using an IoT device)).This post on building [smaller Python Docker images](https://simonwillison.net/2018/Nov/19/smaller-python-docker-images/) contains some good examples of how to remove unnecessary files from your Docker images. _\[I wonder if a collection of 'rm' based one liners, or Dockerfile fragments, that can help reduce your docker container image sizes for particular builds would be useful? —Ed.\]_ See also this [rationale for a minimal Jupyter image](https://nbgallery.github.io/minimal_image.html) as used in _nbgallery_ ([#TJ7](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-seventh)).  
  
One of the things that I'm still struggling with is how to use **continuous integration** methods: a) at all, b) to check Binderised environments, c) to test that notebooks run, and d) test that notebooks run correctly. There is a [continuous build](https://github.com/binder-examples/continuous-build/) Binder example, but as with so much in this week's newsletter, I've yet to play with it...  
 

Jupyter and the Internet of Things (IoT) / Raspberry Pi
-------------------------------------------------------

_For those of you who are likely to spend some of the holiday break tinkering with hardware, here are some Jupyter hooks for you... Note that I haven't tried any this stuff, so if you do and it works, or it doesn't, please let me know..._  
  
I don't really get what's going in in the IoT space, but people I trust seem to think this [Jupyter MicroPython kernel](https://github.com/goatchurchprime/jupyter_micropython_kernel) for interacting with MicroPython on ESP8266 chip (a low cost, low power, system on a chip micro-controller with integrated WiFi and TCP/IP stack) is one to watch; [example notebooks](https://github.com/goatchurchprime/jupyter_micropython_developer_notebooks) seek to demonstrate how an asynchronous webserver and various sensor datalogging and analysis services. This [tutorial blog post](https://towardsdatascience.com/micropython-on-esp-using-jupyter-6f366ff5ed9) looks like it walks you through what you need to do...  
  
If it's a Raspberry Pi you have to hand, there are various guides around how to install a Jupyter notebook server on to it. [This tutorial](https://www.hackster.io/mjrobot/rpi-physical-computing-using-jupyter-notebook-056fa8) gets you up and running in a quick and gentle way with a basic _jupyter_ package install a short project showing how to get started reading and displaying sensor data. This [quick guide](https://www.techcoil.com/blog/how-to-setup-jupyter-notebook-on-raspberry-pi-3-with-raspbian-stretch-lite-supervisor-and-virtualenv-to-run-python-3-codes/) shows how to set up a _supervisord_ config to run the notebook server automatically. [This repo](https://github.com/kleinee/jns) walks you through the build a _Raspberry Pi_ image that contains a Jupyter notebook server in more detail. If you prefer a _Docker_ route, here's a [Dockerfile](https://github.com/mkjiang/rpi-jupyter) for creating a notebook server including _Raspberry Pi _image running _Hypriot OS_. _\[I keep thinking that a digital library shelf for different Raspberry Pi pre-packaged environments would be a handy thing. —Ed.\]_  
  
I remember when we were looking at the possibility of running a robotics residential school using Lego Mindstorms EV3s ([example notebook based Lego Mindstorms / EV3 activities](https://github.com/psychemedia/ev3robotics)). In particular, we explored using a notebook server on each EV3 brick and a central notebook server that supported connections to a remote kernel running on each brick. _\[In the end, we dumped the Python and went with the Lego LabVIEW based software, so the activities were never actually used. —Ed. \]_ This makes me think it might actually make sense to run kernels on RPis and the notebook server somewhere else? This [remote\_ikernel](https://bitbucket.org/tdaff/remote_ikernel) approach may help with that?  
  
_In passing, I note a couple of blockly style UIs for programming EV3s: [RobertaLab](https://github.com/OpenRoberta/robertalab), which we also explored, and the more recent [Microsoft MakeCode](https://makecode.com/blog/lego/05-15-2018). I'd still love to see someone demo a blockly style UI running against a Jupyter kernel..._  
  
As well as using RPis for sensor/actuator I/O, you can also use them in as a cheap way in to building your own cluster. [raspi.farm](https://raspi.farm/) provides details for building a Raspberry Pi cluster from two or more RPis that runs Apache Spark and JupyterHub. _\[Presumably, you could also connect to the Pi Spark Cluster as a remote kernel from your own notebook server? Is there a recipe for that? —Ed.\]_  
  
If working at the IoT transport layer is more your thing, here are [some notebooks](http://github.com/gmr/RabbitMQ-in-Depth) that play around with MQTT. _\[Hmmm, thinks: would an MQTT kernel be in any sense meaningful, and if so, how would you use it? —Ed.\]_  
  
And finally, for Node-RED users, here's a [possible workflow](https://github.com/IBM/node-red-dsx-workflow as a possible bridge between notebook and node-red) for bridging between Norde-RED and Jupyter worlds. _\[Thinks: Node-RED as a JupyerLab plugin?! —Ed.\]_  
 

Controlling Graphical Applications from Notebooks
-------------------------------------------------

One of the reasons for Tracking Jupyter is to help me spot signals regarding where it might go in the future. _\[The approach to futurism I follow is similar to that of Amy Webb, as described in [The Signals Are Talking](https://www.hive.co.uk/Product/Amy-Webb/The-Signals-Are-Talking--Why-Todays-Fringe-Is-Tomorrows-Mainstream/21774494). —Ed.\]_  
  
Here are a couple of signals that may or may not be indicating of another possible way in which Jupyter protocols, or at least, Jupyter UIs, may come to be used as display / control surfaces for (remote) graphical desktop applications.  
  
First up, a [video demo](https://www.youtube.com/watch?v=0fRXGKq7yB4) of **Blender** scripting using [blender-vraag](https://github.com/akloster/blender-vraag), _"a__ high level API for Blender, modeled after JQuery"_. Apparently, _"it's the [blender-asyncio](https://github.com/akloster/blender-asyncio) project which implements a kernel inside a blender instance. Then the notebook server starts blender with that script and connects to the exposed Zeromq ports"._ I haven't found a runnable demo yet, but it would be nice to see a VM or Dockerised build that provides a quick start for this.  
  
Less integrated, but an earlier proof of concept that complemented Lego EV3 robots mentioned above with an exploration of simulated robot operation, is this example of using [Jupyter notebooks to control the VREP 3D simulator](https://blog.ouseful.info/2017/09/10/distributing-virtual-machines-that-include-a-virtual-desktop-to-students-v-rep-jupyter-notebooks/). Once again, the early proof of concept wasn't taken up, but code for building a VM containing linked notebooks and VREP simulator, as well as demo notebooks, can be found [here](https://github.com/psychemedia/ou-robotics-vrep/tree/master/robotVM). _\[I wonder if the webRTC package mentioned in [#TJ8](https://tinyletter.com/TrackingJupyter/letters/tracking-jupyter-newsletter-the-eighth)  might help embed video streams from the simulator in a notebook? Or whether [nbmultitask](https://github.com/micahscopes/nbmultitask) might help with running things in parallel that would otherwise be blocking in a single Python thread? —Ed.\]_  
  
One of the issues with running graphical desktop applications, particularly ones that you might want to embed in a Jupyterkab panel, is the need to run something like a **noVNC** clients. [nbnovnc](https://github.com/ryanlovett/nbnovnc), a _"Jupyter notebook extension for proxing a VNC session"_ looks interesting in this respect (here's an [older, alternative attempt](https://github.com/Mechatronics3D/jupyter-vnc) by someone else).  
  
In terms of fully blown demos, [SimPhoNy Remote](https://pyvideo.org/euroscipy-2017/simphony-remote-accessing-containerized-desktop-and-web-applications-with-a-web-browser.html) is _"a web application that coordinates the execution of Docker images, tailored to a specific use case: accessing a Desktop or Web application combining JupyterHub, Docker and noVNC"_ ([repo](https://github.com/simphony/simphony-remote), [docs](https://simphony-remote.readthedocs.io/en/latest/)).  
  
Form the Swiss Data Sceince Center, a [Jupyterlab VNC extension for Renku](http://also https://github.com/SwissDataScienceCenter/renku-jupyterlab-vnc), which itself is a _"__software platform designed to enable reproducible and collaborative data science"_. The extension _"__creates a menu, palette and a launcher for opening a VNC frame in a Jupyter tab. This extension does not provide a VNC server. The VNC server must be started by the docker container in which this extension is installed"_. An official Jupyterlab-noVNC extension would be a Good Thing to have, I think...  _\[One of the things I've yet to see demoed as a Binder demo is a proxied containerised service run inside a Binder container. That plus this could be interesting...—Ed.\]_  
  
Once you have the jigsaw pieces in place, that more elaborate combinations look like they can easily fall into  place. For example, here's a recipe I've yet to try for [Preparing a headless environment for OpenAI’s Gym (with Docker and Tensorflow)](https://medium.com/coinmonks/preparing-a-headless-environment-for-openais-gym-with-docker-and-tensorflow-1bd0e0d31663) that (I think?!) exposes OpenAI Gym's renderer using noVNC. (Picking up on the GPU thing again. the same post links to a [repo](https://github.com/phizaz/docker-cuda-gym/tree/master/tensorflow) containing a CUDA and notebook supporting Docker build for OpenAI's Gym with Tensorflow.)  
  
Finally, in terms of _"I have no idea if this is even possible"_ desktop GUI integration projects, I've been wondering about QGIS lately, and whether that can be controlled from notebooks as Blender can be. A [report](https://lists.osgeo.org/pipermail/soc/2017-August/003841.html) from a GSoC project to develop a [QGIS Web API and remote control Plugin (for Notebook integration)](https://summerofcode.withgoogle.com/archive/2017/projects/4854198344613888/) _\[RStudio notebooks, maybe? —Ed.\]_ described a _"working version of the QGIS 'networkapi' plugin which makes many of the most useful PyQGIS API functions available over a HTTP interface, as well as a well-documented 'qgisremote' R package which makes these functions available to R"._ Code is available [here](https://qgisapi.gitlab.io/), but I haven't spotted a notebook demo anywhere and haven't made time myself yet to have a play...

  
On the Robot Front...
------------------------

I'm not sure if [Amazon RoboMaker](https://aws.amazon.com/robomaker/) or the [Amazon DeepRacer](https://aws.amazon.com/deepracer/) robots hook into AWS SageMaker Notebooks, or Microsoft's [recently announced](https://blogs.windows.com/windowsexperience/2018/09/28/bringing-the-power-of-windows-10-to-the-robot-operating-system/) ROS for Windows 10 or ROS for Azure have notebook based demos available? On the **ROS** (_"Robot Operating System"_ front, a generic OS for robot software development), I'm not sure how stable this [jupyter-ros](https://github.com/wolfv/jupyter-ros) set of "widget helpers" is? Alternatively, there's a [repo](https://github.com/AdoHaha/ipython_robot_prototyping) available from the IPython Robot Prototyping workshop at PyCon PL 2017, although again, no off-the-shelf VM.  
  
_\[As regards VM solutions, I wonder if any of these could also be Binderised? —Ed.\]_  
 

GPU Plus
--------

_Untested by me so at your own risk... If you try any of these out, or come up with recipes of your own, please let me know how you get on..._  
  
Lots of example notebooks out there require some heavy number crunching, exactly the sort of thing that support from GPU can help with. But how do you go about running Jupyter applications in a GPU context?  
  
The easiest way is probably a hosted solution: **Paperspace** offers _"effortless infrastructure for Machine Learning and Data Science with 1-click Jupyter notebooks"_ (as described in [Jupyter notebooks the easy way! (with GPU support](https://blog.paperspace.com/jupyter-notebook-with-a-gpu-the-easy-way/)) but you'll probably have to stump up some credit card details.  
  
On the other hand, **Google Colab** provides free _\[as in Google free, so who knows how you're paying... —Ed.\]_ GPU support to notebooks run via Google Colab ([Google Colab Free GPU Tutorial](https://medium.com/deep-learning-turkey/google-colab-free-gpu-tutorial-e113627b9f5d)); you can also get TPU accelerator support using Google's [Tensor Processing Units](https://cloud.google.com/blog/products/gcp/an-in-depth-look-at-googles-first-tensor-processing-unit-tpu). If you want a notebook to try it out with, here's one — [Train and serve a TensorFlow model with TensorFlow Serving](https://www.tensorflow.org/serving/tutorials/Serving_REST_simple​) — but note the stern warning!  
  
For Windows users, this recipe for [running GPU powered Tensorflow / Keras on Windows in 10 easy steps](https://medium.com/@saurabh502/up-and-running-with-tensorflow-keras-gpu-on-windows-10-10-easy-steps-a40ad61032dd) seems to have the brevity I'd expect from a _Bake Off_ technical challenge using store cupboard packaged ingredients. But that's not to say it won't rise to the occasion.  
  
For Linux users, you could perhaps try out this recipe for  setting up _"[TensorFlow with Docker + GPU in Minutes Along with Jupyter and OpenCV](https://blog.sicara.com/tensorflow-gpu-opencv-jupyter-docker-10705b6cd1d)"_.  
  
If you don't need a tutorial, but just some build files to copy from, [this repo](https://github.com/zifeo/deep-jupyter) contains a Dockerfile that builds on a base Nvidia CUDA image to provide a Jupyter notebook server with access to a range of pre-installed deep learning tools. A docker-compose file also shows how to run the notebook server via an https proxy.  
  
Alternatively, [this repo](https://github.com/FAU-DLM/GPU-Jupyterhub) contains a couple of similarly based Dockerfiles for creating CUDA enabled images along with docker-compose file that sets up JupyterHub instance with a linked PostgreSQL database rather than the default SQLite database backend. A [blogged tutorial](https://negativesign.com/blog/2018/11/11/docker-and-jupyterhub-for-deep-learning/) walks through the deployment process using this [more committed fork](https://github.com/whlteXbread/GPU-Jupyterhub) of the repo.  
  
If you're looking for something even more ambitious, how about setting up Binderhub with GPU support? With various parts of the Jupyter system still very much in a state of flux, a couple of places I look to for _de facto_ documentation, or at least, examples of how to get things working, are tests and Github issues (questions haven't necessarily made their way to Stack Overflow yet, and many features still aren't stable enough for documenting in official docs). Seeing how talented developers work through issues can also be instructive. A good example comes in the form of this issue thread discussing [GPU demos for the NeurIPS conference](https://github.com/jupyterhub/team-compass/issues/85) and this more technical one on how to [set-up a GPU enabled Binderhub](http://github.com/jupyterhub/team-compass/issues/92) to run the demos.  
  
Most of the examples I've found seemed to use NVIDIA's CUDA, which supports a wide range of GPUs found on many consumer graphics cards; but if you're looking for a cross-platform solution, OpenCL, which runs on Intel, ARM and AMD GPUs as well as NVIDIA ones, is probably the way to go. I haven't found much in the way of Jupyter builds and notebook examples, but  [Introducing PyOpenCL](https://community.arm.com/graphics/b/blog/posts/introducing-pyopencl) may provide a starting point. _\[Apparently; I am so out of my depth here! —Ed.\]_  
 

Ideas from Newsletters Past
---------------------------

If that's not given you enough ideas for Jupyter related projects over the break, you can always check out the [_Tracking Jupyter_ archive](https://tinyletter.com/TrackingJupyter/archive)... But do make sure you take at least some time off and away from the screen...!

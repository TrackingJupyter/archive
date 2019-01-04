October 28, 2018

Tracking Jupyter: Newsletter, the First...
==========================================

by Tony Hirst

Welcome to this first issue of the _Tracking Jupyter_ newsletter, a hopefully regular, possibly occasional, round-up of news and examples from the Jupyter universe.  
  
The newsletter represents the author's personal views and is independent of, and not formally associated with, the original Jupyter project.  
 

Jupyter Notebooks in Use
------------------------

Each year, the Economist publishes the _Big Mac Index_, an informal model based on the idea that currency exchange rates should settle on pricing globally available commodities, such as the Big Mac, equally. The model has traditionally been developed using a spreadsheet, but as described in [Peeling back the curtain _How the Economist is opening the data behind our reporting_](https://medium.economist.com/peeling-back-the-curtain-487bd3be0c47) this year's model was not only developed using a Jupyter notebook, but the Economist has also followed many other news organisations on the road to reporting transparency by [sharing their data and working on Github](https://github.com/TheEconomist/big-mac-data).  
 

Jupyter in Education
--------------------

New to me from the OWLTEH18 event in Coventry last week is [Noteable](https://noteable.edina.ac.uk/), a hosted Jupyterhub notebooks service offered by Edina for staff and students at the University of Edinburgh. From the [Noteable FAQ](https://www.ed.ac.uk/information-services/learning-technology/noteable/noteable-faqs), this appears to be an experimental, internally provided free service, funded in pilot phase until the end of December 2018. Users can log in with their university credentials and have 10GB of persistent storage space available to them.  
 

Jupyter in Industry
-------------------

I didn't make it to JupyterCon over the summer, but a large number of presentations have been published by O'Reilly via their [JupyterCon in New York 2018](https://www.youtube.com/playlist?list=PL055Epbe6d5b572IRmYAHkUgcq3y6K3Ae) YouTube playlist.  
  
A short keynote delivered by Michelle Ufford from Netflix described their use of notebooks across the organisation — [Beyond Interactive: Scaling Impact with Notebooks at Netflix​](https://youtu.be/3LH_nRtrx5U?t=117) — showing how notebooks are used across the board, from data analysis, through literate devops and engineering, to the marketing department. If you'd rather read about it than watch the keynote, there's a supporting post on the Netflix blog: [Beyond Interactive: Notebook Innovation at Netflix](https://medium.com/netflix-techblog/notebook-innovation-591ee3221233).  
 

Productivity Tools
------------------

Identifying meaningful differences between different versions of the same notebook can be a challenge when comparing Github commits. A [newly announced](http://towardsdatascience.com/introducing-reviewnb-visual-diff-for-jupyter-notebooks-6797e6dfa20c) Github connected application, [ReviewNB](https://www.reviewnb.com/), allows you to connect to your public Github repositories, browse through commits and pull requests, and view changes inline. As with many of these sorts of service, it looks like the payment plan will kick in when you want to work with private repositories. It seems to be early days for the project, and as a single developer effort may be considered high risk, but these things can mature quickly. The same developer has another project on the go — [nurtch](https://www.nurtch.com/) — for using notebooks to support IT incident response.  
 

Deployment
----------

For organisations looking to deploy their own Jupyter environments on their own stack, a new guide to [Deploying JupyterHub with Kubernetes on OpenStack](https://blog.jupyter.org/how-to-deploy-jupyterhub-with-kubernetes-on-openstack-f8f6120d4b1) has been published on the Jupyter blog. The authors are looking for feedback, both on the post specifically and on deploying Jupyter using OpenStack more generally. It'd be good to see this being worked up as comprehensive Zero to JupyterHub with OpenStack guide.

Alternative Notebook Environments
---------------------------------

It's not just the Jupyter ecosystem that is promoting the use of notebook style interfaces: a wide variety of alternative notebook based UI applications are also starting to appear, which I'll mention on an occasional basis.  
  
First up, the [Observeable](https://beta.observablehq.com/) notebook from _d3.js_ developer Mike Bostock. The notebooks provide an interactive browser based read/write interface supporting markdown and live Javascript code cells. As you might expect, there is tight integration with _d3.js_ for providing rich interactive graphics. The original motivation can be found in a post from Mike Bostock eighteen months or so ago ([A Better Way to Code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0)) announcing the original incarnation, _d3.express_. The [quickstart guide](https://beta.observablehq.com/@mbostock/five-minute-introduction) is provided as an Observeable notebook and [several dogfooding tutorials](https://beta.observablehq.com/collection/@observablehq/tutorial) are also available along with some rather more involved [developer tutorials](https://beta.observablehq.com/collection/@observablehq/introduction). A [runtime](https://github.com/observablehq/notebook-runtime) is available so you can publish your own Observeable notebooks anywhere.  
 

Recent Releases
---------------

_IPython 7.1_ has been released on PyPi ([update notes](https://ipython.readthedocs.io/en/stable/whatsnew/version7.html#ipython-7-1-0)). New features include new `width` and `height`arguments for `IPython.display.Video` ,  and a major update of the “latex to unicode” tab completion map.  
 

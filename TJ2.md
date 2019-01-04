November 02, 2018

Tracking Jupyter: Newsletter, the Second...
===========================================

by Tony Hirst

Welcome to this second _Tracking Jupyter_ newsletter, and thanks for signing up.  
  
It'll probably take me a few issues to work out how regularly the newsletter will appear, but I seem to manage to come newly announced and new-to-me Jupyter related projects, extensions, applications and deployments every day of the week. One issue is likely to be not overloading each newsletter! Feedback / comments as to whether there's too much / too little in the newsletter would be useful...  
  
Anyway, here are some hopefully interesting nuggets I've gathered together over the last few days...

Jupyter in the News
-------------------

An article in _Nature_ explores [Why Jupyter is data scientists’ computational notebook of choice](https://www.nature.com/articles/d41586-018-07196-1), (_Nature_ 563, 145-146, 30th October, 2018). I first recall seeing Jupyter notebooks  — in their incarnation as IPython notebooks — in _Nature_ back in November, 2014 ([Interactive notebooks: Sharing the code](https://www.nature.com/news/interactive-notebooks-sharing-the-code-1.16261)), a report that also featured a [live demo](https://www.nature.com/news/ipython-interactive-demo-7.21492?article=1.16261), even way back then.

Notebook Productivity
---------------------

[Jupyter Notebook Templates for JupyterLab](https://github.com/timkpaine/jupyterlab_templates) allow you to predefine templated notebooks to provide a quick start to a new notebook based analysis. So what sort of templated notebooks would you find useful, and how would any of your current workflows have to change in order to accommodate them? \[Contributed: Sergio Sánchez\]  
  
[Codekodo Jupyter](http://www.codekodo.net/codekodo-jupyter.php) is a portable Python/JupyterLab distribution for Windows, with what looks like the intention to make it easier to launch JupyterLab in an educational setting. It seems to be early days — if this was a portable app, you'd expect _no_ side-effects or permissions issues — but I think it provides some indication about user expectations around how to to launch Jupyter end-user applications most naturally \[Via: [Python Forum](https://python-forum.io/Thread-Portable-Jupyter-for-Windows)\].  
  
In a similar vein, though a far more mature offering, albeit still under active development, is the [_nteract_](https://nteract.io/desktop)[ Desktop](https://nteract.io/desktop) ([repository](https://github.com/nteract/nteract)). This is a NumFOCUS supported project that presents Jupyter notebooks as a desktop / electron app, pre-bundled with a _node.js_ kernel. An early issue requested that the app bundles it's own Python kernel, but as yet, that's still not part of the application. The README suggests that connections to remote Binderhub kernels, as well as local ones, are supported, (although that's perhaps just in the service based, browser accessed playground?) but I can't see any evidence of how to achieve that in the desktop app. One really handy feature is the built in support for publishing a notebook as a Github gist to your connected Github account.  
  
The (unofficial) [JupyterLab Credential Store](https://github.com/lean-data-science/jupyterlab-credentialstore) ([announcement](https://towardsdatascience.com/the-jupyterlab-credential-store-9cc3a0b9356)) is a JupyterLab extension that allows you to keep AES encrypted key-value credentials (API credentials, etc) secret, whilst calling them into notebooks and scripts as if they were environment variables. Keeping credentials handy, whilst also _not_ sharing them when you push notebooks to a public repository, is fiddly, and this sort sort of credential wallet approach could make it much simpler.

Workbenches
-----------

One very apparent trend is how notebook style user interfaces are starting to become ubiquitous.  
  
A recent report by Forrester (The Forrester Wave™: [Notebook-Based Predictive Analytics And Machine Learning Solutions, Q3 2018](https://www.forrester.com/report/The+Forrester+Wave+NotebookBased+Predictive+Analytics+And+Machine+Learning+Solutions+Q3+2018/-/E-RES143219), Sept5, 2018), available via [Domino Data Lab](https://www.dominodatalab.com/resources/forrester-wave-notebook-based-predictive-analytics-machine-learning/), reviews nine enterprise platforms offering differentiated notebook fronted workbenches for predictive analytics and machine learning (PAML); the Oracle Data Science Platform and Domino Data Lab lead the scorecard. Jupyter notebooks feature prominently as first class user interfaces, as do RStudio and Apache Zeppelin notebooks. Amusingly, readers wishing to explore Forrester's "detailed product evaluations" are prompted to access the Forrester Wave Excel-based vendor comparison tool. Erm... Excel?  
  
If you prefer to roll your own environment, IBM's [Fabric for Deep Learning](https://github.com/IBM/FfDL)(FfDL, "fiddle") allows you to run your own integrated deep learning platform as a service using Kubernetes, with a Jupyter notebooks front end and TensorFlow, Caffe, PyTorch etc. on the back. I could see this sort of thing being useful in an educational context too. \[Contributed: Rod Norfor\]

Alternative Notebook Environments
---------------------------------

Started in 2013, and adopted as an Apache Foundation incubator project at the end of 2014, [Apache Zeppelin](https://zeppelin.apache.org/) is a web-based notebook environment for running and analysing data queries, with built in support for Apache Spark (a scaleable query and analysis engine designed for use with large data sets and streaming data).  
  
As with Jupyter notebooks, the notebook combines markdown and code cells, with some limited built-in support for simple chart display. A wide range of [Apache Zeppelin ](https://zeppelin.apache.org/supported_interpreters.html)[_interpreters_](https://zeppelin.apache.org/supported_interpreters.html) (rather then Jupyter _kernels_) are available, including Python, Spark, BigQuery, PostgreSQL, Cassandra, neo4j and ElasticSearch.  
  
To give it a go, it's probably easiest to run it standalone using a Docker container (for example, using [xemuliam/zeppelin](https://hub.docker.com/r/xemuliam/zeppelin/)), although it probably makes most sense to use it under _docker compose_ and connect it to a pre-existing query engine or database to try it out that way.

Jupyter in Education
--------------------

In his JupyterCon 2018 keynote — [Sea change: What happens when Jupyter becomes pervasive at a university?](https://www.oreilly.com/ideas/sea-change-what-happens-when-jupyter-becomes-pervasive-at-a-university) — Fernando Perez reports how introductory data science courses delivered through Jupyter notebooks are well on track to reach 50% of the student population at UC Berkeley. Yes, you read that right: 50%.The keynote is less than 15 minutes long, but packed with insight and vision, so grab a coffee and watch it through.  
  
Fernando asks what pervasive familiarity with using notebook interfaces might achieve, and it seems that the management team at Berkeley are also trying to think this through with their [announcement of the creation of Division of Data Science and Information](http://www.dailycal.org/2018/11/01/uc-berkeley-announces-creation-of-division-of-data-science-and-information/) \[[press release (November1, 2018)](https://news.berkeley.edu/2018/11/01/berkeley-inaugurates-division-of-data-science-and-information-connecting-teaching-and-research-from-all-corners-of-campus/)\]:

> The new division will be a peer to other campus colleges and divisions, such as the College of Engineering or the division of biology. The division will stress interdisciplinary collaboration among existing departments and will work to integrate data and information science into a suite of existing academic and scientific fields.

This is reinforced by _"hopes that the new division will promote “permeable boundaries” among disciplines and help create a universitywide culture of “shared purpose.”"_ Exciting times... The Division's homepage is already up and running: [Berkeley Division of Data Sciences](https://data.berkeley.edu/).

Deployment
----------

Jupyter notebooks are already offered as first class user interfaces in data analysis suites offered by IBM, Microsoft, Google and Amazon, as the aforementioned Forrester report describes. It seems that other cloud infrastructure service providers are also looking at offering Jupyter as an enterprise service with the announcement of the Mesosphere Jupyter Service (MJS) on October 25th, 2018 ([press release](https://mesosphere.com/blog/announcing-dc-os-1-12-multi-kubernetes-data-science-across-multi-cloud-edge/)) ([release notes](https://docs.mesosphere.com/1.12/release-notes/1.12.0/)). With this release comes the availability of [JupyterLab on DC/OS](https://medium.com/@nzaporozhets/jupyterlab-on-dc-os-tips-and-tricks-e4d3b66c3e31).

Jupyter Notebooks in Use
------------------------

Picking up on an example from Fernando Perez' keynote, check out the [Computational and Inferential Thinking](https://www.inferentialthinking.com/chapters/intro) interactive textbook used to support one of the Berkeley courses. To see how it's done, check out the repo: [data-8/textbook](https://github.com/data-8/textbook).

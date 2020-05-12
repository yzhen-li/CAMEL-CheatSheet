*IC: Yi Zhen, Yang Yang,*

*Manager: Tie Wang, Bo Long*

This doc is to summarize the recent progress on artificial intelligence
and machine learning on software engineering. Under the umbrella of
AIOps and AI Quality, our focus is on **SCQA (source code quality
assurance)**, which is in line with data quality and model quality our
`AIQF <http://go/aiqf>`__ team has been working on.

`Portal (go/DeepCode) <#portal-godeepcode>`__\ **2**

`Microsoft AIOps Initiatives
(Confidential) <#microsoft-aiops-initiatives-confidential>`__\ **2**

`Glossary <#glossary>`__\ **2**

`Machine Learning on Source Code
(MLonCode) <#machine-learning-on-source-code-mloncode>`__\ **2**

   `Summary <#summary>`__ 2

   `Demo <#demo>`__ 4

   `Resources <#resources>`__ 4

   `Literature Review <#literature-review>`__ 4

   `Research Groups <#research-groups>`__ 4

   `Product <#product>`__ 4

   `People <#people>`__ 4

`Machine Learning on Testing
(MLonTest) <#machine-learning-on-testing-mlontest>`__\ **4**

   `Summary <#summary-1>`__ 4

   `Resources <#resources-1>`__ 5

   `Course <#course>`__ 5

   `Research Groups <#research-groups-1>`__ 5

   `Articles <#articles>`__ 5

   `Products <#products>`__ 5

`LinkedIn Resources <#linkedin-resources>`__\ **6**

`Related Works <#related-works>`__ **6**

   `MLOps <#mlops>`__ 6

`Proposal <#proposal>`__\ **6**

`References <#references>`__\ **7**

Portal (`go/DeepCode <http://go/DeepCode>`__)
=============================================

Microsoft AIOps Initiatives (Confidential)
==========================================

-  `Abstract <https://microsoft.sharepoint.com/:w:/r/teams/mingvirtualteam/_layouts/15/doc2.aspx?sourcedoc=%7BA86D5975-D950-4CEB-B4F1-54B49014E589%7D&file=The%20Microsoft%20AIOps%20Initiative%20-%20one%20year%20update.docx&action=default&mobileredirect=true&DefaultItemOpen=1&cid=f942ce48-52ec-4339-a0c1-782cb1824feb>`__

-  `Slides <https://microsoft-my.sharepoint.com/:p:/r/personal/blong_linkedin_biz/_layouts/15/guestaccess.aspx?e=BtjZLp&share=EWZY1i9f2ydOqkPX2M5pX10BonWyJG9k1pnyIqbRgzEiyQ>`__

-  AIOps Pillars

   -  AI for Infra/System

   -  **AI for DevOps**

   -  AI for Customers

-  AI Quality Pillars

   -  Data quality

   -  Model quality

   -  **Code quality**

-  **Devops lifecycle**

   -  Requirement

   -  Design

   -  **implementation/code**

   -  **Test**

   -  **Deployment**

   -  **maintenance**

Glossary
========

-  DevOps:
      `DevOps <https://www.exitcertified.com/blog/primer-to-devops?gclsrc=aw.ds&&gclid=CjwKCAjwguzzBRBiEiwAgU0FTyW20TEWrUW0QHUhuVnoErbn0lFfXBNCw4yLuFgMhRGZ__5lFSQBERoCtMUQAvD_BwE>`__
      is an application development culture in which software developers
      collaborate with operations to ensure that the software is
      deployed into production with a minimal number of errors.

-  AIOps

-  MLOps

Machine Learning on Source Code (MLonCode)
==========================================

Leveraging machine learning to find statistical patterns in large
corpora of code and to drive new software development tools and program
analyses.

Summary
-------

+----------------------+----------------------+----------------------+
| Area                 | topic                | applications         |
+======================+======================+======================+
| Code Search and      | Code to Code search  | Learning to rank     |
| Recommendation       |                      | code examples `(Niu, |
|                      |                      | Keivanloo, and Zou   |
|                      |                      | 2017) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?smdKeG>`__ |
+----------------------+----------------------+----------------------+
|                      | Natural language to  | Bimodal modeling     |
|                      | code search          | between source code  |
|                      |                      | and natural language |
|                      |                      | `(Miltos Allamanis   |
|                      |                      | et al.               |
|                      |                      | 2015) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?fz8ZWD>`__ |
+----------------------+----------------------+----------------------+
| Code Generation      | Code migration       | Python2 to Python3   |
|                      |                      | `(Aggarwal, Salameh, |
|                      |                      | and Hindle           |
|                      |                      | 2015) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?XY9HHo>`__ |
+----------------------+----------------------+----------------------+
|                      | Idiom mining         | Find idiom of code   |
|                      |                      | `(Miltiadis          |
|                      |                      | Allamanis and Sutton |
|                      |                      | 2014) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?nvPZQh>`__ |
+----------------------+----------------------+----------------------+
|                      | documentation        | Auto documentation   |
|                      |                      | from code `(Barone   |
|                      |                      | and Sennrich         |
|                      |                      | 2017) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?40CpC9>`__ |
+----------------------+----------------------+----------------------+
|                      | Code completion      | Python code          |
|                      |                      | suggestion           |
|                      |                      | `(Bhoopchand et al.  |
|                      |                      | 2016) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?G3SUWZ>`__ |
+----------------------+----------------------+----------------------+
| Code Repair          | Detect bugs          | Detect bugs `(Ray et |
|                      |                      | al.                  |
|                      |                      | 2016) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?sstOuK>`__ |
+----------------------+----------------------+----------------------+
|                      | Detect code          | Code vulnerability   |
|                      | vulnerabilities      | detection `(Russell  |
|                      |                      | et al.               |
|                      |                      | 2018) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?yrCqFW>`__ |
|                      |                      |                      |
|                      |                      | Code smell detection |
|                      |                      | `(Fontana et al.     |
|                      |                      | 2016) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?AP8lNN>`__ |
+----------------------+----------------------+----------------------+
|                      | Repair generation    | Patch generation     |
|                      |                      | `(Long and Rinard    |
|                      |                      | 2016) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?EjSSUc>`__ |
+----------------------+----------------------+----------------------+
| Code Review          | Evaluate code        | Evaluate code        |
|                      | quality              | contribution         |
|                      |                      | `(Hellendoorn,       |
|                      |                      | Devanbu, and         |
|                      |                      | Bacchelli            |
|                      |                      | 2015) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?Q3mRVz>`__ |
+----------------------+----------------------+----------------------+
|                      | Sentiment analysis   | Benchmark study      |
|                      |                      | `(Novielli, Girardi, |
|                      |                      | and Lanubile         |
|                      |                      | 2018) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?n6MLhl>`__ |
+----------------------+----------------------+----------------------+
|                      | Code summarization   | Code summarization   |
|                      |                      | `(Miltiadis          |
|                      |                      | Allamanis, Peng, and |
|                      |                      | Sutton               |
|                      |                      | 2016) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?yLqY7D>`__ |
|                      |                      |                      |
|                      |                      | `Code2seq <https     |
|                      |                      | ://code2seq.org/>`__ |
|                      |                      |                      |
|                      |                      | `code2vec <https     |
|                      |                      | ://code2vec.org/>`__ |
+----------------------+----------------------+----------------------+
|                      | Code clone detection | Code clone detection |
|                      |                      | `(Büch and Andrzejak |
|                      |                      | 2019) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?gcmLV1>`__ |
+----------------------+----------------------+----------------------+
|                      | Code optimization    | Superoptimize code   |
|                      |                      | `(Bunel et al.       |
|                      |                      | 2016) <https:        |
|                      |                      | //www.zotero.org/goo |
|                      |                      | gle-docs/?WvPPm0>`__ |
+----------------------+----------------------+----------------------+

Demo
----

-  `Towards Natural Language Semantic Code
      Search <https://github.blog/2018-09-18-towards-natural-language-semantic-code-search/>`__

-  `How To Create Natural Language Semantic Search for Arbitrary Objects
      With Deep
      Learning <https://towardsdatascience.com/semantic-code-search-3cd6d244a39c>`__
      (`code <https://github.com/hamelsmu/code_search>`__,
      `data <https://github.com/github/CodeSearchNet>`__)

-  `CodeSearchNet Challenge: Evaluating the State of Semantic Code
      Search <https://arxiv.org/abs/1909.09436>`__

-  `Code2vec <https://code2vec.org/>`__

-  `code2seq <https://code2seq.org/>`__

Resources
---------

Literature Review
~~~~~~~~~~~~~~~~~

-  https://github.com/src-d/awesome-machine-learning-on-source-code

-  `Learning from Big Code <http://learnbigcode.github.io/>`__

-  `ML4Code <https://ml4code.github.io/>`__

-  `What is machine learning on
      code? <https://www.kdnuggets.com/2019/11/machine-learning-code-mloncode.html>`__

Research Groups
~~~~~~~~~~~~~~~

-  `MAST <https://mast-group.github.io/>`__ from Edinburgh University

-  `SEAL <https://seal-queensu.github.io/index.html>`__ from Queen’s
      University

Product
~~~~~~~

-  `Aroma <https://ai.facebook.com/blog/aroma-ml-for-code-recommendation/>`__,
      code-to-code search and recommendation tool from Facebook

-  `Codota <https://www.codota.com/>`__, code suggestions tool for ides
      such as idea and bs code

   -  https://blog.codota.com/python-plugins-for-intellij-idea/

   -  TabNine is for python, codota itself does not support python

-  `Deepcode.ai <https://www.deepcode.ai/>`__, vulnerability detection
      and fixing tool

   -  Plugin for vs code and atom only, only work for github/bitbucket

-  `Deepbugs for
      python <https://plugins.jetbrains.com/plugin/12218-deepbugs-for-python>`__

   -  Plugin for idea

People
~~~~~~

-  `Hamel Husain <http://hamel.io/>`__

Machine Learning on Testing (MLonTest)
======================================

There are two major areas of machine learning on testing:

1. How machine learning can help improve the tools of traditional
      software testing?

2. Given that traditional software testing tools may not be effective
      for machine learning models/workflows, what tools can we develop
      to test machine learning models?

.. _summary-1:

Summary 
-------

+----------------+----------------------+-------------------------+
| Area           | Topics               | Applications            |
+================+======================+=========================+
| ML for Testing | Automated testing    | Survey `(Hourani,       |
|                |                      | Hammad, and Lafi        |
|                |                      | 2019) <                 |
|                |                      | https://www.zotero.org/ |
|                |                      | google-docs/?3rAFcw>`__ |
|                |                      |                         |
|                |                      | Generate test c         |
|                |                      | programs for c compiler |
|                |                      | `(Liu et al.            |
|                |                      | 2019) <                 |
|                |                      | https://www.zotero.org/ |
|                |                      | google-docs/?eaYURl>`__ |
|                |                      |                         |
|                |                      | Test case generation    |
|                |                      | `(Kikuma et al.         |
|                |                      | 2019) <                 |
|                |                      | https://www.zotero.org/ |
|                |                      | google-docs/?5boV3h>`__ |
|                |                      |                         |
|                |                      | `Unit test              |
|                |                      | generation <https:/     |
|                |                      | /research.infosupport.c |
|                |                      | om/wp-content/uploads/U |
|                |                      | nit-test-generation-usi |
|                |                      | ng-machine-Master-Thesi |
|                |                      | s-Laurence-Saes.pdf>`__ |
+----------------+----------------------+-------------------------+
| Testing for ML | ML quality assurance | Quality assurance       |
|                |                      | framework on ranking    |
|                |                      | models (Murphy, Kaiser, |
|                |                      | and Arias 2006).        |
+----------------+----------------------+-------------------------+
|                | Adversarial testing  | Adversarial examples    |
|                |                      | `(Goodfellow, Shlens,   |
|                |                      | and Szegedy             |
|                |                      | 2018) <                 |
|                |                      | https://www.zotero.org/ |
|                |                      | google-docs/?0M7btq>`__ |
|                |                      |                         |
|                |                      | `Consistency            |
|                |                      | check <https://deepmi   |
|                |                      | nd.com/blog/article/rob |
|                |                      | ust-and-verified-ai>`__ |
+----------------+----------------------+-------------------------+

.. _resources-1:

Resources 
---------

Course 
~~~~~~

-  `Artificial Intelligence (AI) in Software Testing
      @Udemy <https://www.udemy.com/course/artificial-intelligence-ai-in-software-testing/>`__

.. _research-groups-1:

Research Groups
~~~~~~~~~~~~~~~

-  `OpenAI <https://openai.com/blog/adversarial-example-research/>`__

-  `DeepMind <https://deepmind.com/blog/article/robust-and-verified-ai>`__

Articles
~~~~~~~~

-  `How Machine Learning and AI Bring a New Dimension to Software
      Testing <https://towardsdatascience.com/how-machine-learning-and-ai-bring-a-new-dimension-to-software-testing-7b2b6ea67b61>`__

-  `Machine Learning for Automation
      Testing <https://dzone.com/articles/machine-learning-for-automation-testing>`__

-  `Test Automation in the World of AI &
      ML <https://www.infoq.com/articles/test-automation-ai-ml/>`__

-  `How AI is changing test automation: 5
      examples <https://techbeacon.com/app-dev-testing/how-ai-changing-test-automation-5-examples>`__

-  `What is Artificial Intelligence in Software
      Testing? <https://blog.parasoft.com/what-is-artificial-intelligence-in-software-testing>`__

-  `Machine Learning for Automation
      Testing <https://blog.goodaudience.com/machine-learning-for-automation-testing-698230917082>`__

-  `The top 7 test automation mistakes: How to avoid your next
      fail <https://content.microfocus.com/software-test-automation-tb/top-7-test-automation-mistakes%20?utm_source=techbeacon&utm_medium=techbeacon&utm_campaign=00134846>`__

-  `Turning Testers into Machine Learning
      Engineers <https://medium.com/@jarbon/turning-testers-into-machine-learning-engineers-2f9e990abfef>`__

Products
~~~~~~~~

-  `jtest <https://www.parasoft.com/products/jtest>`__

-  `test.ai <https://www.test.ai/about>`__

-  `TestIM <https://go.testim.io/automated-software-testing-free-trial-a?utm_source=google&utm_medium=cpc&utm_campaign=automated-testing&utm_campaign=automated-testing&utm_term=%2Bmachine%20%2Blearning%20%2Bautomated%20%2Btesting&utm_medium=cpc&utm_source=google&hsa_kw=%2Bmachine%20%2Blearning%20%2Bautomated%20%2Btesting&hsa_mt=b&hsa_grp=68336649071&hsa_tgt=kwd-645617085044&hsa_net=adwords&hsa_cam=1684222079&hsa_ver=3&hsa_acc=6463132548&hsa_src=g&hsa_ad=415944560314&gclid=EAIaIQobChMIhYyYtv2z6AIVKB6tBh1K0gjEEAAYASAAEgI7uvD_BwE>`__

LinkedIn Resources
==================

`go/DeepCodeResource <http://go/DeepCodeResource>`__

Related Works
=============

MLOps
-----

The buzzword MLOps is about the toolings around the life cycle of
machine learning, including data, model and code. The are quite a few
open source tools, and here we want to focus the following:

-  DVC (Data Version Control): for data versioning

-  MLflow for experiment tracking

Some other tools are covered here

-  https://martinfowler.com/articles/cd4ml.html

-  https://towardsdatascience.com/enable-ml-experiments-4ba8c3c8bdc2

-  https://mlops.org/

-  `MLOps on Azure <https://github.com/microsoft/MLOps>`__ enables you
      to track / version / audit / certify / re-use every asset in your
      ML lifecycle and provides orchestration services to streamline
      managing this lifecycle.

-  `Another review about the term
      “MLOps” <https://towardsdatascience.com/the-rise-of-the-term-mlops-3b14d5bd1bdb>`__

-  `Enterprise Readiness, MLOps and Lifecycle Management with Jordan
      Edwards <https://twimlai.com/twiml-talk-321-enterprise-readiness-mlops-and-lifecycle-management-with-jordan-edwards/>`__

Proposal
========

-  `Representation Learning for Source Code <http://go/rl4code>`__

The first step is to understand the semantics of source code. Compared
to previous methods that rely on grammar analysis and string processing,
our approach is to use machine learning techniques, specifically,
embedding and representation learning, to learn the semantics of source
code. We will build an MVP of semantic code search to showcase the
efficacy of our approach.

Toolings for experiment

-  https://colab.research.google.com/drive/10OinT5ZNGtdLLQ9K399jlKgNgidxUbGP

-  

References
==========

`Aggarwal, Karan, Mohammad Salameh, and Abram Hindle. 2015. “Using
Machine Translation for Converting Python 2 to Python 3 Code.” PeerJ
PrePrints. <https://www.zotero.org/google-docs/?aojeE8>`__

`Allamanis, Miltiadis, Hao Peng, and Charles Sutton. 2016. “A
Convolutional Attention Network for Extreme Summarization of Source
Code.” In International Conference on Machine Learning,
2091–2100. <https://www.zotero.org/google-docs/?aojeE8>`__

`Allamanis, Miltiadis, and Charles Sutton. 2014. “Mining Idioms from
Source Code.” In Proceedings of the 22nd ACM SIGSOFT International
Symposium on Foundations of Software Engineering,
472–483. <https://www.zotero.org/google-docs/?aojeE8>`__

`Allamanis, Miltos, Daniel Tarlow, Andrew Gordon, and Yi Wei. 2015.
“Bimodal Modelling of Source Code and Natural Language.” In
International Conference on Machine Learning,
2123–2132. <https://www.zotero.org/google-docs/?aojeE8>`__

`Barone, Antonio Valerio Miceli, and Rico Sennrich. 2017. “A Parallel
Corpus of Python Functions and Documentation Strings for Automated Code
Documentation and Code Generation.” ArXiv Preprint
ArXiv:1707.02275. <https://www.zotero.org/google-docs/?aojeE8>`__

`Bhoopchand, Avishkar, Tim Rocktäschel, Earl Barr, and Sebastian Riedel.
2016. “Learning Python Code Suggestion with a Sparse Pointer Network.”
ArXiv Preprint
ArXiv:1611.08307. <https://www.zotero.org/google-docs/?aojeE8>`__

`Büch, Lutz, and Artur Andrzejak. 2019. “Learning-Based Recursive
Aggregation of Abstract Syntax Trees for Code Clone Detection.” In 2019
IEEE 26th International Conference on Software Analysis, Evolution and
Reengineering (SANER), 95–104.
IEEE. <https://www.zotero.org/google-docs/?aojeE8>`__

`Bunel, Rudy, Alban Desmaison, M. Pawan Kumar, Philip HS Torr, and
Pushmeet Kohli. 2016. “Learning to Superoptimize Programs.” ArXiv
Preprint
ArXiv:1611.01787. <https://www.zotero.org/google-docs/?aojeE8>`__

`Fontana, Francesca Arcelli, Mika V. Mäntylä, Marco Zanoni, and
Alessandro Marino. 2016. “Comparing and Experimenting Machine Learning
Techniques for Code Smell Detection.” Empirical Software Engineering 21
(3): 1143–1191. <https://www.zotero.org/google-docs/?aojeE8>`__

`Goodfellow, Ian J., Jonathon Shlens, and Christian Szegedy. 2018.
“Explaining and Harnessing Adversarial Examples. ArXiv.”
Preprint. <https://www.zotero.org/google-docs/?aojeE8>`__

`Hellendoorn, Vincent J., Premkumar T. Devanbu, and Alberto Bacchelli.
2015. “Will They like This? Evaluating Code Contributions with Language
Models.” In 2015 IEEE/ACM 12th Working Conference on Mining Software
Repositories, 157–167.
IEEE. <https://www.zotero.org/google-docs/?aojeE8>`__

`Hourani, Hussam, Ahmad Hammad, and Mohammad Lafi. 2019. “The Impact of
Artificial Intelligence on Software Testing.” In 2019 IEEE Jordan
International Joint Conference on Electrical Engineering and Information
Technology (JEEIT), 565–570.
IEEE. <https://www.zotero.org/google-docs/?aojeE8>`__

`Kikuma, Kazuhiro, Takeshi Yamada, Koki Sato, and Kiyoshi Ueda. 2019.
“Preparation Method in Automated Test Case Generation Using Machine
Learning.” In Proceedings of the Tenth International Symposium on
Information and Communication Technology,
393–398. <https://www.zotero.org/google-docs/?aojeE8>`__

`Liu, Xiao, Xiaoting Li, Rupesh Prajapati, and Dinghao Wu. 2019.
“Deepfuzz: Automatic Generation of Syntax Valid c Programs for Fuzz
Testing.” In Proceedings of the AAAI Conference on Artificial
Intelligence,
33:1044–1051. <https://www.zotero.org/google-docs/?aojeE8>`__

`Long, Fan, and Martin Rinard. 2016. “Automatic Patch Generation by
Learning Correct Code.” In Proceedings of the 43rd Annual ACM
SIGPLAN-SIGACT Symposium on Principles of Programming Languages,
298–312. <https://www.zotero.org/google-docs/?aojeE8>`__

`Niu, Haoran, Iman Keivanloo, and Ying Zou. 2017. “Learning to Rank Code
Examples for Code Search Engines.” Empirical Software Engineering 22
(1): 259–291. <https://www.zotero.org/google-docs/?aojeE8>`__

`Novielli, Nicole, Daniela Girardi, and Filippo Lanubile. 2018. “A
Benchmark Study on Sentiment Analysis for Software Engineering
Research.” In 2018 IEEE/ACM 15th International Conference on Mining
Software Repositories (MSR), 364–375.
IEEE. <https://www.zotero.org/google-docs/?aojeE8>`__

`Ray, Baishakhi, Vincent Hellendoorn, Saheel Godhane, Zhaopeng Tu,
Alberto Bacchelli, and Premkumar Devanbu. 2016. “On the" Naturalness" of
Buggy Code.” In 2016 IEEE/ACM 38th International Conference on Software
Engineering (ICSE), 428–439.
IEEE. <https://www.zotero.org/google-docs/?aojeE8>`__

`Russell, Rebecca, Louis Kim, Lei Hamilton, Tomo Lazovich, Jacob Harer,
Onur Ozdemir, Paul Ellingwood, and Marc McConley. 2018. “Automated
Vulnerability Detection in Source Code Using Deep Representation
Learning.” In 2018 17th IEEE International Conference on Machine
Learning and Applications (ICMLA), 757–762.
IEEE. <https://www.zotero.org/google-docs/?aojeE8>`__

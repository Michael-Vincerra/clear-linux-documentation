.. _swupd-search: 

Use swupd search to find a bundle
#################################

.. contents:: :local: 
   depth: 2

This illustration shows you how to use `swupd search` as a Developer. We 
assume that you have a base knowledge of: 

* How :ref:`swupd <swupd-guide>` works 
* How :ref:`swupd <swupd-about>` differs from *package managers* in other Linux\* distributions 


.. TODO: This will follow using 'mixer'. Explain the end goal of mixer. 


Scenario 1: Data Science with Python
====================================

We're developing a custom Clear Linux OS for data science with Python. We'll 
develop our own mix, from which we'll create a release image. That image 
will be distributed to data center (DC) clients across the United States  
who need this data to determine DC workload balancing. We need to
create a tool to analyze energy consumption profiles based on population 
statistics and consumption data, whose results are heat-maps showing where 
and when energy consumption peaks in large metropolitan areas. 

.. Given that our project requires `statsmodels` for modeling, 
..  `matplotlib` for charts, as well `numpy` and `pandas` for set analysis, ... we need a sophisticated set of tools.

First, use :command:`swupd search` with a general term like *Python*. 

#. Enter this command and add 'Python' as the search term: 

   .. code-block:: bash

      sudo swupd search -b Python

   .. note::
      
      `swupd search` searches for matching paths in the manifest data. 
      Enter only one term, or one hyphenated term, at a time. 
      Use the command :command:`man swupd` to learn more. 

.. TODO: Add tensorflow and more on machine learning in description. 

#. Results of `swupd search` shows the best match for our use case.

   .. code-block:: console

      Bundle python-data-science	(923 MB to install)
      		/usr/bin/ipython3
      		/usr/bin/ipython

   .. note::

      Result shown above is one of several shown in standard output.  

      If the bundle is already installed, [installed] appears in search results. If it doesn't apppear, the bundle needs to be installed. 

# If you know you want to import a module from a package 
   consider using sed.... Use an example here. 







#. Add the bundle `python-data-science`.

   .. code-block:: bash

      sudo swupd bundle-add python-data-science

#. When prompted, enter your password. 

   .. note:: 

      You should see console data similar to the following: 

   .. code-block:: console 

      Password: 
      Downloading packs...

      Extracting python-data-science pack for version 23710
      ...50%
      Extracting python-extras pack for version 23830
      ...100%
      Starting download of remaining update content. This may take a while...
      ...100%
      Finishing download of update content...
      Installing bundle(s) files...
      ...100%
      Calling post-update helper scripts.
      Successfully installed 1 bundle
FAQ
===

Find answers to these common questions in this section: 

* How do I show all bundles available?
* How do I find the bundles I need?
* How do I use `swupd` search?
* How do I add new bundles? 

.. note:: 
   
   For developers who do not wish to adopt the |CL| Common Tooling Framework (e.g., Autospec, etc.), select the complementary :file:`-dev` bundle in order to successfully build each bundle. 
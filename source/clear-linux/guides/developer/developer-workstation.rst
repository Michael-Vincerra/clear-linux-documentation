.. _developer-workstation:

Developer Workstation
#####################

Workstation Setup
*****************

*Workstation Setup* helps you, the developer, find the tools you need to 
start your project. 

Use the *Clear Linux Developer Profiles* (Table 1) to help you decide which 
bundles, at minimum, you need to set up your developer workstation. 

We recommend using :ref:`swupd-search` to jump-start your skills in using 
fundamental |CL| features like `swupd`. 

:ref:`swupd search <swupd-search>` shows: 

* How to use `swupd` commands
* How to search for bundles (that contain packages)
* How to add bundles

How to use this document
========================

Use Table 1 to identify the *minimum required bundles* you need to get 
started developing based on your role. We recognize that your role may not 
necessarily fit into one of these categories. Use Table 1 as a starting 
point. 

.. list-table:: **Table 1. Clear Linux Developer Profiles**
   :widths: 20, 20, 20, 20
   :header-rows: 1

   * - Clear Linux Bundle
     - *Internet of Things (IoT)* 
     - *System Administrator*
     - *Client/Cloud/Web Developer*
   * - `editors` 
     - ✓
     - ✓
     - ✓

   * - `network-basic`
     - ✓
     - ✓
     - ✓

   * - `openssh-server`
     - ✓
     - ✓
     - ✓
   
   * - `webserver-basic`
     - 
     - ✓
     - ✓   
   
   * - `application-server`
     - 
     - ✓
     - ✓
   
   * - `database-basic`
     - 
     - ✓
     - ✓
   
   * - `desktop-autostart`
     - 
     - ✓
     - ✓

   * - `dev-utils`
     - 
     - 
     - ✓




Core Concepts
=============

We recommend that you understand these core concepts in |CL| *before* 
developing your project. 

* :ref:`Bundles <bundles-about>`
* :ref:`Software update <swupd-about>`
* :ref:`Mixer <mixer-about>`
* :ref:`Autospec <autospec-about>` 

Resources for |CL| developers: 

* `Developer Tooling Framework for Clear Linux`_
* `Clear Linux Bundles`_
*  ???

.. Find correct unicode and replace repeated names above with unicode symbol
.. http://docutils.sourceforge.net/0.7/docs/ref/rst/directives.html#unicode-character-codes
	.. |checkmark| unicode:: 0xE2
	.. Try 2714 / 2713


.. _Clear Linux Bundles: https://github.com/clearlinux/clr-bundles

.. _Developer Tooling Framework for Clear Linux: https://github.com/clearlinux/common




.. Outline
	.. Purpose: This outline provides a framework that anticipates the questions a general Linux developer would have in learning how to use Clear Linux to set up a Developer Workstation for the first time. 



.. Day 0 Day 0: Get Clear Linux running on bare metal or VM.



.. Day 1: Get all of the Developer Tools needed/ Toolchain. 

	.. 1.1	Describe “clr-on-clr” to get all the tools that you need. 
	.. Beth Dean: “I want all the std tools.”
   	 	These are the tools that Beth expects to have:
	   -	Busybox shell
	   -	Ifconfig
	   -	Netsh
	   -	Build environment
	   -	Editor
	   -	Grep 

	.. 1.2	Enable user space

	.. 1.3	(If desired). Final part: Installing a desktop (GDM) 





.. Day 2





.. Day 3
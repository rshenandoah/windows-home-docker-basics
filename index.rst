.. include:: cyverse_rst_defined_substitutions.txt

|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

**Windows Home Quickstart**
===================
Overview
----
The Windows 10 Home operating system (OS) has some subtle differences from the Windows 10 Pro OS that present a stumbling block for setting up virtual machines (VM) and accessing platforms like Docker that support open and reproducible science. Most tutorials and guides for setting up VMs for Windows assume the user is using Windows Pro without making the distinction between the two systems clear or directly linking to alternative guides for Windows Home leaving Home users without sufficient information to quickly determine why their systems are not functioning when they followed the instructions provided. Documentation for Windows Home is buried within the documentatation for platforms such as Docker and not linked to on the main instalation pages. 

*This guide is written and tested for Windows 10. If working with an earlier version of Windows, double check with Microsoft documentation as these instructions may differ.*

Objectives
----
* Enable virtualization on Windows 10 Home OS
* Install Docker Toolbox to connect to Docker via the Toolbox app command line interface or from the Windows Powershell
* Activate Windows Subsystem for Linux to natively run Linux on Windows Home OS



Activities
----
**1. Enable virtualization on Windows 10 Home OS**

Windows Home OS defaults to having virtualization disabled. To work with any VM system in this OS the first step is to enable virtualization. 

**1.1 Check status of virtualization** 

Open Task Manager by pressing the Ctrl+Shift+Esc key together at the same time and go to the "Performance" tab. On the bottom right, look for 'Virtualization'. Next to that, it will show either 'Enabled' or 'Disabled'. If 'Disabled' continue on with these instructions, if 'Enabled' skip to part 2.

**1.2 Enable virtualization** 

In the Windows search box, search for and open “Change advanced startup options”. The next few steps will require a reboot of your computer. At this point, consider sending a link to this tutorial to a different device or make note of the rest of this step. Save any open documents and choose **Restart Now**. 

Your computer will reboot to a blue “Choose an option” screen. Select **Troubleshoot**.

Select **Advanced options**

Select **UEFI Firmware Settings**

Click **restart**. This reboot will automatically launch the Setup Utility. 

Arrow over to the "Configuration" tab. Arrow down to 'Intel Virtual Technology' select it and arrow down and press enter to enable it. Save and exit.

You can now install software supporting VMs and run VMs on your Windows Home OS.


**2. Install Docker Toolbox**

Docker Desktop, the current version of Docker is not compatable with Windows Home. Docker Toolbox continues to be supported for older Windows OS and Windows 10 Home.

Follow the instructions for installing `Docker Toolbox <://docs.docker.com/toolbox/toolbox_install_windows/>`_ provided by Docker. 

**2.1 Test Docker commands in Windows Powershell**

With Docker Toolbox installed and running correctly, you have the option to engage with Docker via the Docker Quickstart Terminal as shown in the Docker tutorial linked above or from Windows Powershell. In Powershell you can use all the Docker commands the same as you would in any other command line interface. Try 
.. code-block:: bash
  $ docker run hello-world
	

**3. Windows Subsystem for Linux**

Windows Subsystem for Linux (WSL) is a compatibility layer for running Linux binary executables natively on Windows 10. This may be useful for other open science applications.

**3.1 Enable WSL**

Open Powershell as administrator and run
.. code-block:: bash
  $ Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

**3.2 Install Linux**

Install your favorite Linux distribution from the Windows App Store, another download source, or if this is your first experience `read some reviews and chose a flavor <https://itsfoss.com/best-linux-beginners/>`_. 

Running Docker via Linux on WSL requires additional set up and configuration. For ease of access, users are advised to access Docker via Docker Toolbox or the Powershell instead. 





Review
----
You have now enabled virtualization to support Docker and other VM dependent systems, installed Docker Toolbox, tested Docker commands on Powershell, and activated WSL to run Linux on your Windows Home OS.


Lets do science!



..
    Short description and links to any reading materials
----
Search for an answer:
|CyVerse Learning Center| or
|CyVerse Wiki|

Post your question to the user forum:
|Ask CyVerse|

----

**Fix or improve this documentation**

- On Github: |Github Repo Link|
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`__





=================
Following is default content from Cyverse quickstart import.
=================


.. include:: cyverse_rst_defined_substitutions.txt

|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

**QUICKSTART NAME**
===================

..
    #### Comment: Use short, imperative titles e.g. Upload and share data, uploading and
    sharing data ####

Goal
----

..
    Avoid covering upstream and downstream steps that are not explicitly and
    necessarily part of the tutorial - write or link to separate quick
    starts/tutorials for those parts

..
    #### Comment: A few sentences (50 words or less) describing the ultimate goal of the steps
    in this tutorial ####

----

.. toctree::
	:maxdepth: 2

	Quickstart home <self>
	Step Two <step2.rst>
	Delete this example guide page <example_directives_delete.rst>
..
	#### Comment:This tutorial can have multiple pages. The table of contents assumes
	you have an additional page called 'Step Two' with content located in 'step2.rst'
	Edit these titles and filenames as needed ####

..
    #### Comment: If you are using the TOC remove the 'summary', 'Additional information,
    help' and 'Fix or improve this tutorial' from all pages except the last page of the
    quickstart ####

-----

Prerequisites
-------------



Downloads, access, and services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need access to the following services/software*


 .. list-table::
   :header-rows: 1

   * - Prerequisite
     - Preparation/Notes
     - Link/Download
   * - CyVerse account
     - You will need a CyVerse account to complete this exercise
     - |CyVerse User Portal|
   * - Atmosphere access
     - You must have access to Atmosphere
     - |CyVerse User Portal|
   * - Cyberduck
     - Standalone software for upload/download to Data Store
     - |Download Cyberduck|

Platform(s)
~~~~~~~~~~~

*We will use the following CyVerse platform(s):*

 ..
   #### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Documentation
      - Quick Start
    * - Data Store
      - GUI/Command line
      - |Data Store|
      - |Data Store Manual|
      - |Data Store Guide|
    * - Discovery Environment
      - Web/Point-and-click
      - |Discovery Environment|
      - |DE Manual|
      - |Discovery Environment Guide|
    * - Atmosphere
      - Command line (ssh) and/or Desktop (VNC)
      - |Atmosphere|
      - |Atmosphere Manual|
      - |Atmosphere Guide|
    * - BisQue
      - Web/Point-and-click and/or Command-line (API)
      - |BisQue|
      - |BisQue Manual|
      - (See Manual)
    * - DNA Subway
      - Web/Point-and-click
      - |DNA Subway|
      - (See Guide)
      - |DNA Subway Guide|
    * - SciApps
      - Command-line (API)
      - |SciApps|
      - (See Guide)
      - |SciApps Guide|
    * - Agave API
      - Command-line (API)
      - |Agave API|
      - |Agave Live Docs|
      - (See Live Docs)

Input and example data
~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this quickstart you will need to have the following inputs prepared*

.. list-table::
    :header-rows: 1

    * - Input File(s)
      - Format
      - Preparation/Notes
      - Example Data
    * -
      -
      -
      -

----


*Get started*
--------------

1. Step one
2. Step two

----



*Summary*
~~~~~~~~~~~


**Next Steps:**

Some common next steps include:

1. Step

2. Step

----

Additional information, help
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..
    Short description and links to any reading materials

Search for an answer:
|CyVerse Learning Center| or
|CyVerse Wiki|

Post your question to the user forum:
|Ask CyVerse|

----

**Fix or improve this documentation**

- On Github: |Github Repo Link|
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`__

.. Comment: Place Images Below This Line
   use :width: to give a desired width for your image
   use :height: to give a desired height for your image
   replace the image name/location and URL if hyperlinked


 .. |Clickable hyperlinked image| image:: ./img/IMAGENAME.png
    :width: 500
    :height: 100
 .. _CyVerse logo: http://learning.cyverse.org/

 .. |Static image| image:: ./img/IMAGENAME.png
    :width: 25
    :height: 25



.. Comment: Place URLS Below This Line

   # Use this example to ensure that links open in new tabs, avoiding
   # forcing users to leave the document, and making it easy to update links
   # In a single place in this document

   .. |Substitution| raw:: html # Place this anywhere in the text you want a hyperlink

      <a href="REPLACE_THIS_WITH_URL" target="blank">Replace_with_text</a>


.. |Github Repo Link|  raw:: html

   <a href="FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX" target="blank">Github Repo Link</a>


.. |Download Cyberduck| raw:: html

   <a href="https://cyberduck.io/" target="blank">Download Cyberduck</a>

#GST 105: Introduction to Remote Sensing
##Lab 3:  Image Composite, Mosaic, Subset
###Objective – Overview of Basic GRASS GIS Raster Functionality inside QGIS 

Document Version: 8/25/2014

**Author:**
Richard Smith, Ph.D.  
Texas A&M University - Corpus Christi

---

Copyright © National Information Security, Geospatial Technologies Consortium (NISGTC)

The development of this document is funded by the Department of Labor (DOL) Trade Adjustment Assistance Community College and Career Training (TAACCCT) Grant No.  TC-22525-11-60-A-48; The National Information Security, Geospatial Technologies Consortium (NISGTC) is an entity of Collin College of Texas, Bellevue College of Washington, Bunker Hill Community College of Massachusetts, Del Mar College of Texas, Moraine Valley Community College of Illinois, Rio Salado College of Arizona, and Salt Lake Community College of Utah.  This work is licensed under the Creative Commons Attribution 3.0 Unported License.  To view a copy of this license, visit http://creativecommons.org/licenses/by/3.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  

---

###1. Introduction

This lab will provide an introduction and overview of some of the basic functionality of GRASS GIS inside QGIS 2.4 for working with raw image data to add and view image data sets.  Students are encouraged to become familiar with working with and finding information on GRASS GIS help topics.  It is also recommended to create screenshots and notes of software and of lecture slides that can make up a student’s “notes.”

This lab includes the following tasks:

+ Task 1 – Learn Basics of GRASS GIS inside QGIS
+ Task 2 – Image Composite
+ Task 3 – Image Mosaic
+ Task 4 – Image Subset
+ Task 5 – Calculate NDVI
+ Task 6 – Challenge: Image Subset with r.patch

###2. Objective: Overview of Basic GRASS Raster Functionality inside QGIS

While QGIS has a large amount of functionality, it only goes so far before its limits are reached.  To extend the functionality of QGIS, the capabilities of GRASS GIS (or simply GRASS), have been made available through the ‘GRASS’ toolbar in QGIS.  GRASS is a free and open source GIS software package containing over 350 modules to display, analyze, and manipulate vector and raster data.  While GRASS is a separate, stand-alone GIS software package, in this lab series, we will only interact with GRASS through QGIS.  

Most students will be already be familiar with the vector-based GIS functions found within QGIS.  This lab introduces the student to the raster analysis functions in GRASS and creating some simple multi-band image composites from existing remotely sensed imagery, creating subsets (clipping) of rasters, and creating a mosaic.

###3. How Best to Use Video Walk Through with this Lab

To aid in your completion of this lab, each lab task has an associated video that demonstrates how to complete the task.  The intent of these videos is to help you move forward if you become stuck on a step in a task, or you wish to visually see every step required to complete the tasks.

We recommend that you do not watch the videos before you attempt the tasks.  The reasoning for this is that while you are learning the software and searching for buttons, menus, etc…, you will better remember where these items are and, perhaps, discover other features along the way.  With that being said, please use the videos in the way that will best facilitate your learning and successful completion of this lab.

###Task 1 - Learn Basics of GRASS GIS inside QGIS

GRASS GIS is installed by default when you install QGIS Desktop. While GRASS is a completely stand-alone GIS software package, its capabilities are made available via a toolbar inside of QGIS.  This task will teach you the basic terminology and concepts of how GRASS manages data, as well as what each button the GRASS Toolbar does.

First, let’s start with some terminology and concepts.  Working with GRASS data is different than how you may be used to working with data using QGIS or other GIS software packages.  Since the storage paradigm is significantly different than what you have seen in prior courses, we will discuss how GRASS stores data first.  Refer to the figure below during the following explaination for a graphic representation of the storage concepts.

In order for GRASS to start a project, it must first connect to a Database (also called a GISDBase).  The Database is simply a folder on your computer that has special sub directories.  Once GRASS connects to a Database, it then needs to access a Location.  A Location is a child directory of the Database and stores the coordinate system or map projection that all enclosed Mapsets will use; think of a Location as a common container for a project.  A Mapset is a child directory of a Location that represents a geographical subset of its parent Location.  Mapsets contain geographic data in their directories.  There are two types of mapsets: Permanent and owner.  A Permanent mapset usually contains read-only geographic data that can be used by anyone.  The Permanent mapset also may contain other information about the Location that is not stored anywhere else, therefore, the Permanent mapset must exist in every Location.  Owner mapsets are user-created and represent specific areas or study sites within the Location.  Think of a mapset as a collection of geographic data that is project or user specific.  Owner mapsets can be named whatever logical name is desired.  Examples of mapset names are ‘user1’ and ‘Nueces County’, where ‘user1’ represents a mapset created by, or created for a user on the system, and ‘Nueces County’ represents a project dealing with Nueces County, Texas. Last, there is the concept of a Region.  A Region is a subset of a Location defined by a rectangular bounding box.  The Region is important for raster operations as it bounds the area (region) that will participate in any raster operations executed in GRASS.  A Region is an operating parameter set when working in GRASS.

If all of the above explaination was a little confusing, don’t worry, with practice in these labs, it will start to make more sense.

![GRASS Storage Paradigm](figures/GRASS_Storage_Paradigm.jpg)

*GRASS Storage Paradigm*

Now let’s talk about how you can access the data and functionality of GRASS inside QGIS.  Inside QGIS, there is a GRASS Toolbar that can be enabled (shown in figure below).

![GRASS Toolbar in QGIS](figures/GRASS_Toolbar_in_QGIS.png)

*GRASS Toolbar in QGIS*


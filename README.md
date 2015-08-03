# GST 105 - Introduction to Remote Sensing - FOSS4G Labs
-----------
**FOSS4G course curriculum for GST 105 - Introduction to Remote Sensing.**

This curriculum currently contains labs written to use FOSS4G software such as QGIS
and GRASS GIS.

### Lab Topics

+ [x] Lab 3 - Image Composite, Mosaic, Subset
+ [x] Lab 4 - Image Rectification
+ [x] Lab 5 - Unsupervised Classification
+ [x] Lab 6 - Supervised Classification
+ [x] Lab 7 - Accuracy Assessment

**Note: There is no Lab 1 or Lab 2**

*Labs with a checkmark are completely converted to Markdown*

### Lab Contents

Each Module folder contains a folder designating which version of the QGIS and GRASS GIS
software it is written for (ex. 'Module 1 Lab\\QGIS 2.4 and GRASS 6.4.4\\...', 'Module 4 Lab\\QGIS 2.8 
GRASS 6.4.4\\...').  The hope is that as new software versions are released, 
the prior lab's version will be updated and stored in a new (appropriately named) folder.

Each lab contains the following four resources:

+ **Module *n* Lab.md** - Markdown file of lab
+ **Module *n* Lab.docx** - MS Word document of the lab
+ **figures** - Folder containing all images reference in the lab
+ **Lab *n* Data** - Folder containing all data referenced in the lab

### Feedback
[Open an issue][7] or [fork and submit a pull request][8] on github, or, email [Richard.Smith@tamucc.edu][6].

### Curriculum Philosophy

This curriculum was developed to bring a complete set of labs using FOSS4G to 
the community.  As educators, we found the amount of ready-made FOSS4G curriculum
lacking, or woefully out of date.  Therefore, with the support of the Department
of Labor, we decided to create the world's first complete FOSS4G curriculum available
for everyone to use, for free.

*We do not want this curriculum to die!*  Therefore, the [ICA-OSGeo][1] [Lab at
Texas A&M University - Corpus Christi][2] is spearheading the continued development
and updating of these labs.

### License: Creative Commons 3.0 License

This work is licensed under the Creative Commons Attribution 3.0 Unported License.  To view a copy of this license, visit <http://creativecommons.org/licenses/by/3.0/>.F

### Curriculum History

FOSS4G Lab Author:
Richard Smith, Ph.D., GISP
Texas A&M University - Corpus Christi

Original Lab Content Author:
Nathan Jennings

The development of the original document was funded by the Department of Labor (DOL) Trade Adjustment Assistance Community College and Career Training (TAACCCT) Grant No.  TC-22525-11-60-A-48; The National Information Security, Geospatial Technologies Consortium (NISGTC) is an entity of Collin College of Texas, Bellevue College of Washington, Bunker Hill Community College of Massachusetts, Del Mar College of Texas, Moraine Valley Community College of Illinois, Rio Salado College of Arizona, and Salt Lake Community College of Utah.  This work is licensed under the Creative Commons Attribution 3.0 Unported License.  To view a copy of this license, visit http://creativecommons.org/licenses/by/3.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.

This document continues to be modified and improved by generous public contributions.heir original form by Richard Smith and continues to be modified and improved by generous public contributions.

### Curriculum Document Format
All curriculum is written in [Markdown][3].  Markdown was chosen for these reasons:

+ [Markdown][3] is easy to learn and contains enough functionality to render the labs.
+ With the lab documents converted to Markdown, GitHub can track all changes
to the document; this is not possible with, say, a Word or PDF document.
+ It is very easy to convert Markdown to multiple other formats using software
such as [PanDoc][4].

Each lab begins with a lab title.

+ Course titles are always size Header 1 `# GST 10X - Course Title` and are the only size 
Header 1 in the lab document.

The lab number and name is listed next.

+ Lab number and titles are always size Header 2 `## Lab n: Lab Title` and are the
only size Header 2 in the lab document.

An attribution block is next as we always want to give proper attribution.

+ This Markdown document contains the attribution block: 
[Attribution Block for Lab Documents.md][5].

An Introduction, Objective, and Video Statement are listed next.

+ These three sections are always size Header 3 `### Introduction` and are always
sections 1, 2, and 3 respectively.

The lab Tasks (logical blocks of content) are next.

+ The Tasks are always size Header 3 `### Task n - Task Title`.  A lab document 
contains as many Tasks deemed appropriate by the authors.
+ The last Task is always a challenge for the students to attempt on their own
without (m)any step-by-step instructions.

The last two sections are Conclusion and Questions.

+ These two sections are always size Header 3 `### Conclusion` and are always
sections 4 and 5 respectively.

When a figure is placed in the lab document, the figure is never provided a number, 
instead, it is referred to by its relative placement to the referring text (ex. 
refer to figure below).  *All figures should be placed within the 'figures' folder 
in the same directory as the Markdown document.

[1]: http://www.geoforall.org/
[2]: http://www.spatialquerylab.com
[3]: http://daringfireball.net/projects/markdown/syntax
[4]: http://johnmacfarlane.net/pandoc/
[5]: Attribution_Block_for_Lab_Documents.md
[6]: mailto:Richard.Smith@tamucc.edu
[7]: https://guides.github.com/features/issues/
[8]: https://guides.github.com/activities/forking/

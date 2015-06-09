.. _Accessibility Best Practices for Course Content Development:

############################################################
Accessibility Best Practices for Developing Course Content
############################################################

EdX is dedicated to creating a platform that is not only itself accessible,
but also enables course content creators to create accessible content. If you
encounter platform issues that you believe might affect your ability to
provide accessible course content, please contact us at accessibility@edx.org.
We welcome any comments and questions.

.. note:: If you use authoring tools other than those provided by edX, your
   course content might not be accessible or might not meet our standards for
   accessibility.

.. contents::
   :local:
   :depth: 1


.. _Make Sure Your Course Content is Perceivable:

************************************************
Make Sure Your Course Content is Perceivable
************************************************

The `WCAG 2.0 <http://www.w3.org/TR/WCAG20/#cc1>`_ guidelines are organized
around several principles, one of which is that web content must be
perceivable. Information and user interface components must be presentable to
users in ways they can perceive. Users must be able to perceive the
information being presented; it cannot be invisible to all of their senses.

To produce content that is perceivable by all learners, follow these
guidelines.

=================================================
Include Text Alternatives for Non-Text Content
=================================================

For any non-text content, provide text alternatives so that thew content can
be changed into other forms that people need, such as large print, braille,
speech, symbols, or simpler language. 

For non-text tests or exercises that would be invalid if presented in text,
provide text alternatives that at least provide descriptions of the non-text
content. Make sure that all images have useful alternative text that screen
readers and other assistive technologies can read. For more information, see
:ref:`Best Practices for Describing Images`.

=================================================
Provide Alternatives for Time-Based Media
=================================================

For time-based media, including pre-recorded audio or video content, provide
alternative equivalent information, such as captions, audio description or
pre-recorded sign language interpretation. For more information, see
:ref:`Creating Accessible Media`.

=================================================
Make Sure Your Content is Adaptable
=================================================

Design your course content so that it can be presented in different ways
without losing information or structure. If your content includes specific
information, structure, and relationships (such as sequence) that is conveyed
through presentation, make sure the same information, structure, and
relationships can be programmatically determined or are available in text.

Make sure your course content does not rely solely on sensory characteristics
such as shape, size, visual location, orientation, or sound, to be understood
by learners.

======================================================
Make It Easier for Learners to See and Hear Content
======================================================

Make the default presentation as easy to perceive as possible, especially by
making it easier for learners to distinguish foreground information from the
background, in both visual and audio elements.

For visual elements, techniques include making sure the fonts you use are
readable, that there is sufficient contrast between the foreground and
background. Do not use color as the sole means of visually distinguishing an
element or conveying critical information. When images contain text, make sure
that the text has a font size of at least 14 points and has good contrast with
the background.

For audio elements, make sure foreground sounds are sufficiently louder than
background sounds.


.. _Make Sure Your Course Content is Readable:

************************************************
Make Sure Your Course Content is Readable
************************************************

Make sure your course content is readable and understandable. EdX courses have
a global and diverse audience, including learners whose native language is not
the language in which you created your course, and learners who have a
disability that affects reading, such as dyslexia or a visual impairment.

Learners will be better positioned to access concepts in your content if you
write in clear, straightforward language and the content is well structured.
Use appropriate terminology to your subject area, but keep it as clear and
unambiguous as possible.

To produce content that is more understandable for all learners, follow these
guidelines.

=========================================
Provide Clear and Consistent Structure
=========================================

Name your course sections, subsections, units, components, and discussion topics in
a consistent way, and make sure the names are useful and easy to skim. Make an
element's name descriptive of its content, and put the important keyword
information first in the name. These names are used in navigation menus, page
headings, and section headings; they are signposts that help learners navigate
your course and read course content.

When you create written learning resources, break text into sections using
HTML elements such as headings, paragraphs, and lists. Long blocks of unbroken
text are a barrier to most readers. Segmented content is more inviting and is
easier to navigate and search. See :ref:`Best Practices for HTML Markup` for
guidance on creating accessible HTML.

When you provide links to external material, use link text that clearly
explains the link destination (for example, "Review the Course Syllabus").
Avoid using constructs such as “Review the Course Syllabus here”, with only
the word "here" serving as link text. For links that point to documents rather
than web pages, include the document type in the link. For example,
"Supplemental Reading for Week 1 (EPUB)").


=========================================
Write Simply and Clearly
=========================================

Avoid jargon. If unfamiliar words or phrases are relevant to the subject,
explain them when they are first used, and include a glossary with your course
materials. When you use an abbreviation or acronym, provide the full phrase
the first time it appears. For example, "World Health Organization (WHO)."

The Center for Plain Language provides detailed resources on writing clearly
and concisely, in language appropriate for your content and target audience.
http://centerforplainlanguage.org/5-steps-to-plain-language/


.. _Best Practices for Describing Images:

************************************************
Use Best Practices for Describing Images
************************************************

Pictures, diagrams, maps, charts, and icons can present information very
effectively. However, some visually impaired students, including people who
use screen reader software, need text alternatives to understand the
information conveyed by these images. The text alternative for an image
depends on the image’s context and purpose, and might not be a simple
description of the image’s visual characteristics. In general, for every
graphic, edX recommends that you provide a text alternative that provides the
equivalent information that a sighted learner would obtain from viewing the
graphic.

Use the following guidelines when you include images in your course.

* Provide a short text description that conveys the purpose of the image,
  unless the image conveys a concept or is the only source for the information
  it presents, in which case provide a long text description. Note that you do
  not need to provide a long description if the information appears elsewhere
  on the page. For example, you do not need to describe a chart if the same
  data appears as text in a data table.
 
 * For a representative image, such as a photograph of the Ponte Vecchio, a
   short description could be “Photo of Ponte Vecchio.” If the photograph’s
   purpose is to provide detailed information about the location, the long
   description should be more specific: “Photo of Ponte Vecchio showing its
   three stone arches and the Arno River.”

 * For a chart, diagram, or illustration, the short description might be
   “Illlustration of Ponte Vecchio.” The long description should include the
   details conveyed visually, such as dimensions and materials used.

 * For a map, a short description might be “Map showing location of Ponte
   Vecchio.” If the map is intended to provide directions to the bridge, the
   long description should provide text directions.
 
 * For icons, the short description should be equivalent to the information
   that the icon provides. For example, for a Course Syllabus link containing
   a PDF icon, the text equivalent for the icon would be “PDF,” which would be
   read as “Course Syllabus PDF.”

 * For an image that serves primarily as a link to another web page, the short
   description should describe the link’s destination, not the image. For
   example, an image of a question mark that serves as a link to a Help page
   should be described as “help,” not “question mark.”

 * Images that do not provide information do not need text descriptions. For
   example, a PDF icon that is followed by link text reading “Course Syllabus
   (PDF)” does not need a description. Another example is a banner graphic
   whose function is purely aesthetic.
 
* Include the short description in the ``alt`` attribute of the HTML image
  element (see :ref:`Add an Image to an HTML Component` for more
  information about adding images). ::

   <img src="image.jpg" alt="Photo of Ponte Vecchio">


* Include an empty ``alt`` attribute for non-informative images. An empty
  ``alt`` attribute tells screen reader software to skip the image. :: 

   <img src="image.jpg" alt="">

  If image elements do not include an ``alt`` attribute at all, screen reader
  software might skip the image, announce the image filename, or, in the case
  of a linked image, announce the link URL. 

* Consider using a caption to display long descriptions so that the
  information is available to all learners. In the following example, the
  image element includes the short description as the ``alt`` attribute and the
  paragraph element includes the long description. ::

   <img src="image.jpg" alt="Photo of Ponte Vecchio">
   <p>Photo of Ponte Vecchio showing its three stone arches and the Arno river</p>
  
* Alternatively, provide long descriptions by creating an additional unit or
  downloadable file that contains the descriptive text and providing a link to
  the unit or file below the image. ::
 
   <img src="image.jpg" alt="Illustration of Ponte Vecchio">
   <p><a href="description.html">Description of Ponte Vecchio Illustration</a></p>


=====================================================
Accessible Images Resources
=====================================================

* A `decision tree <http://www.4syllables.com.au/2010/12/text-alternatives-decision-tree/>`_ for choosing appropriate alternative text for images (Dey Alexander).

* `WebAim <http://webaim.org/techniques/alttext/>`_ provides general guidance
  on the appropriate use of alternative text for images.

* A more detailed description of HTML5 techniques for providing useful
  alternative text for images from `W3C <http://dev.w3.org/html5/alt-
  techniques/>`_.

* `The DIAGRAM Center <http://www.diagramcenter.org/webinars.html>`_,
  established by the US Department of Education (Office of Special Education
  Programs), provides guidance on ways to make it easier, faster, and more
  cost effective to create and use accessible images.
  


.. _Creating Accessible PDFs:

************************************************
Create Accessible PDFs
************************************************

Portable Document Format (PDF) is a common format for course materials,
including textbooks supplied by publishers. However, converting materials to
PDF documents can create accessibility barriers, particularly for learners
with visual impairments. To improve the accessibility of your PDF documents,
review the guidelines below.


.. contents::
   :local:
   :depth: 1


.. _Convert MS Office Documents to PDF:

=============================================
Converting Microsoft Office Documents to PDF
=============================================

The source teaching materials for your course might exist in a variety of
formats. For example, your syllabus might be in MS Word, your presentation
slides in MS PowerPoint, and your textbooks in publisher-supplied PDF.

Use the tools available in the applicable software to create well-structured
source documents before performing any conversion to PDF. This early step
helps to minimize issues that can be difficult or impossible to address after
you have saved the documents as PDFs.


++++++++++++++++++++++++++++
Preparing Word Documents
++++++++++++++++++++++++++++

Keep formatting simple. Use headings, paragraphs, lists, images, and captions,
and tables for tabular data. Do not add unnecessary indents, rules, columns,
blank lines, or typographic variation. The simpler the formatting, the easier
it will be to make an accessible PDF document.

Use standardized styles for formatting your text, such as Normal, Heading 1,
and Heading 2, rather than manually formatting text using boldface and
indents.

Add alternative text to images (see :ref:`Best Practices for Describing
Images`) using the picture formatting options in MS Word.


++++++++++++++++++++++++++++++++
Preparing PowerPoint Documents
++++++++++++++++++++++++++++++++

* To make your content accessible and comprehensible to learners who use screen
  reading software, start in Outline view and include all of your content as
  text. Add design elements and images after completing the outline, and use the
  picture formatting options in MS Powerpoint to include detailed text
  descriptions of images that convey useful information to learners who cannot
  view the images. Avoid adding animations or transitions, as they will not be
  saved with the PDF format.

* Use the **Home > Drawing > Arrange > Selection Pane** option to view the reading
  order of objects on each slide. If the reading order is not logical, change
  the order of the objects.

* Use the **Home > Slides > Reset** option to give each slide a unique and
  informative title. The title can be hidden if you prefer.

* Identify column headers for any data table using the table formatting options
  in MS Powerpoint (**Tables > Table Options > Header Row**), and ensure that
  each header contains informative text describing the data in that column.


++++++++++++++++++++++++++++++++
Preparing Excel Spreadsheets
++++++++++++++++++++++++++++++++

* Use a unique and informative title for each worksheet tab.

* Include text alternatives for images (see :ref:`Best Practices for
  Describing Images`) using Excel’s picture formatting options.

* Identify column headers using Excel’s table formatting options (Table >
  Table Options > Header Row), and include in each header cell informative
  text describing the data in that column.

* Do not use blank cells for formatting.

* Use descriptive link text rather than URLs in data cells.


.. _Convert Word Powerpoint and Excel docs to PDF:

=================================================================
Converting MS Word, MS PowerPoint, and MS Excel documents to PDF
=================================================================

To generate PDFs from Microsoft Office documents, use the **Save as PDF**
option. Make sure the **Document Structure Tags for Accessibility** option is
selected (consult your software documentation for more details).

Note that PDFs generated from Windows versions of MS Office might be more
accessible than those generated from Mac OS versions of MS Office.

.. _Working with PDFs supplied by third parties:

==========================================================
Working With PDFs Supplied by Third Parties
==========================================================

If you control the creation of a PDF, you have greater control over the
document’s accessibility. If you use PDFs provided by third parties, including
textbooks supplied by publishers, the document’s accessibility might be
unknown.

**Asking the right questions about accessible PDFs**

Where possible, ask the supplier of the PDF if the PDF is accessible. If it is
not, ask whether the supplier can provide an accessible version. Here are some
questions you can ask.

* Can screen readers read the document text?
* Do images in the document include alternative text descriptions?
* Are all tables, charts, and math provided in an accessible format?
* Does all media include text equivalents?
* Does the document have navigational aids, such as a table of contents,
  index, headings, and bookmarks?

.. _Updating PDFs for Accessibility:

==========================================================
Updating PDFs for Accessibility
==========================================================

You might need to update your existing teaching materials in PDF format to
improve accessibility. 

PDF documents might have been created by any of the following methods.

* Created by scanning a hard-copy document;
* Generated from a document that was not created with accessibility in mind.
* Generated by a process that does not preserve source accessibility information.

In such cases, you need special software, such as Adobe Acrobat Professional,
to enhance the accessibility of the PDF. 

PDFs that are created from scanned documents require a preliminary Optical
Character Recognition (OCR) step to generate a text version of the document.
The procedure checks documents for accessibility barriers, adds properties and
tags for document structure, sets the document’s language, and adds
alternative text for images.


.. _Accessible PDF Resources:

===============================
Accessible PDF Resources
===============================


* Microsoft provides detailed guidance on generating accessible PDFs from
  Microsoft Office applications, including Word, Excel, and PowerPoint
  http://office.microsoft.com/en-gb/word-help/create-accessible-pdfs-
  HA102478227.aspx

* Adobe provides a detailed accessibility PDF repair workflow using Acrobat
  XI. http://www.adobe.com/content/dam/Adobe/en/accessibility/products/acrobat
  /pdfs/acrobat-xi-pdf-accessibility-repair-workflow.pdf

* Adobe Accessibility (Adobe) is a comprehensive collection of resources on
  PDF authoring and repair, using Adobe’s products.
  http://www.adobe.com/accessibility.html

.. This UWash link is behind a login page. Delete or replace? 

* PDF Accessibility (University of Washington) provides a step-by-step guide
  to creating accessible PDFs from different sources and using different
  applications. http://www.washington.edu/accessibility/pdf/

* PDF Accessibility (WebAIM) provides a detailed and illustrated guide on
  creating accessible PDFs. http://webaim.org/techniques/acrobat/

* The National Center of Disability and Access to Education has a collection
  of one-page “cheat sheets” on accessible document authoring.
  http://ncdae.org/resources/cheatsheets/

* The Accessible Digital Office Document (ADOD) Project provides guidance on
  creating accessible Office documents. http://adod.idrc.ocad.ca/

.. _Best Practices for Math Content:

************************************************
Use Best Practices for Mathematical Content
************************************************

Math in online courses can be challenging to deliver in a way that is
accessible to people with vision impairments.

Do not create images of equations instead of including text equations. Math
images cannot be modified by people who need a larger or high contrast
display, and cannot be read by screen reader software.

EdX uses MathJax (https://www.mathjax.org) to render math content in a format
that is clear, readable, and accessible to people who use screen readers.
MathJax works together with math notation such as LaTeX and MathML to render
mathematical equations as text instead of images. EdX recommends that you use
MathJax to display your math content.

======================================================
Accessible Mathematical Content Resources
======================================================

* The University of Washington’s DO-IT project provides guidance on creating
  accessible math content. 
  http://www.washington.edu/doit/are-there-guidelines-creating-accessible-math?465=

* AccessSTEM provides guidance on creating accessible science, technology,
  engineering and math educational content.
  http://www.washington.edu/doit/programs/accessstem/overview

* MathJax provides guidance on creating accessible pages with their display
  engine. http://www.mathjax.org

* The Design Science News blog shares information about making math
  accessible. http://news.dessci.com/accessible-math


.. _Best Practices for Custom Content Types:

************************************************
Use Best Practices for Custom Content Types
************************************************

Using different content types in your courses can significantly add to the
learning experience for your students. This section covers how to design
several custom content types so that your course content is accessible all
learners.

.. contents::
   :local:


.. _Information Graphics:

=============================================================
Information Graphics (Charts, Diagrams, Illustrations)
=============================================================

Graphics are helpful for communicating concepts and information, but they can
present challenges for people with visual impairments. For example, a chart
that requires color perception or a diagram with tiny labels and annotations
will likely be difficult to comprehend for learners with color blindness or
low vision. All images present a barrier to learners who are blind.

EdX recommends that you follow these best practices for making information
graphics accessible to visually impaired students.

* Avoid using only color to distinguish important features of an image. For
  example, on a line graph, use a different symbol or line style as well as
  color to distinguish the data elements.

* Whenever possible, use an image format that supports scaling, such as .svg,
  so that learners can employ zooming or view the image larger. Consider
  providing a high resolution version of complex graphics that have small but
  essential details.

* For every graphic, provide a text alternative that provides the equivalent
  information that a sighted learner would obtain from viewing the graphic.
  For charts and graphs, a text alternative could be a table displaying the
  same data. See :ref:`Best Practices for Describing Images` for details about
  providing useful text alternatives for images.


.. _Simulations and Interactive Modules:

======================================================
Simulations and Interactive Modules
======================================================

Simulations, including animated or gamified content, can enhance the learning
experience. In particular, they benefit learners who might have difficulty
acquiring knowledge from reading and processing textual content alone.
However, simulations can also present some groups of learners with
difficulties. To minimize barriers to learning, consider the intended learning
outcome of the simulation. Is your goal to reinforce understanding that can
also come from textual content or a video lecture, or is it to convey new
knowledge that other course resources cannot cover? Providing alternative
resources will help mitigate the impact of any barriers.

Although you can design simulations to avoid many accessibility barriers, some
barriers, particularly in simulations supplied by third parties, might be
difficult or impossible to address for technical or pedagogic reasons.
Understanding the nature of these barriers can help you provide workarounds
for learners who are affected.  Keep in mind that attempted workarounds for
simulations supplied by third parties might require the supplier’s consent if
copyrighted material is involved.

Consider the following questions when creating simulations, keeping in mind
that as the course instructor, you enjoy considerable freedom in selecting
course objectives and outcomes. Additionally, if the visual components of a
simulation are so central to your course design, providing alternate text
description and other accommodations might not be practical or feasible.

* Does the simulation require vision to understand? If so, provide text
  describing the concepts that the simulation conveys.

* Is a computer mouse necessary to operate the simulation? If so, provide text
  describing the concepts that the simulation conveys.

* Does the simulation include flashing or flickering content that could
  trigger seizures?

  If so, and if this content is critical to the nature of the
  simulation, take these steps.
 
  * Do not make using the simulation a requirement for a graded assessment
    activity.

  * Provide a warning that the simulation contains flickering or flashing content.


.. _Online Exercises and Assessments:

======================================================
Online Exercises and Assessments
======================================================

For each activity or assessment that you design, consider any difficulties
that learners with disabilities might have in completing it, and consider
using multiple assessment options. Focus on activities that can be completed
and submitted by all learners.

Some students take longer to read information and input responses, such as
students with visual or mobility impairments and students who need time to
comprehend the information. If an exercise has a time limit, consider whether
the allowed time is enough for all learners to respond. Advance planning might
help to reduce the number of students requesting time extensions.

Some online exercise question types, such as the following examples, might be
difficult for students who have vision or mobility impairments.

* Exercises requiring fine hand-eye coordination, such as image mapped input
  or drag and drop exercises, might present difficulties to students who have
  limited mobility. Consider alternatives that do not require fine motor
  skills, unless, of course, such skills are necessary for effective
  participation in the course. For example, instead of a drag and drop
  exercise for mapping atoms to compounds, provide a checkbox or multiple
  choice exercise.

* Highly visual stimuli, such as word clouds, might not be accessible to
  students who have visual impairments. Provide a text alternative that
  conveys the same information, such as an ordered list of words in the word
  cloud.

.. _Third Party Content:

======================================================
Third-Party Content
======================================================

If you include links to third-party content in your course, be mindful of the
accessibility of such resources. EdX recommends that you test any links prior
to sharing them with learners.

You can use the eReader tool or :ref:`Add Files to a Course` to incorporate
third-party textbooks and other publications in PDF format into your course.
You can also incorporate such materials into your course in HTML format. See
:ref:`Creating Accessible PDFs` for guidance on working with third-party
supplied PDFs, and :ref:`Best Practices for HTML Markup` for guidance on
creating accessible HTML.


.. _Accessible Custom Content Resources:

======================================================
Accessible Custom Content Resources
======================================================

* Effective Practices for Description of Science Content within Digital
  Talking Books, from the National Center for Accessible Media, provides best
  practices for describing graphs, charts, diagrams, and illustrations.
  http://ncam.wgbh.org/experience_learn/educational_media/stemdx

* AccessSTEM provides guidance on creating accessible science, technology,
  engineering and math educational content.
  http://www.washington.edu/doit/programs/accessstem/overview

* The National Center on Educational Outcomes (NCEO) provides Principles and
  Characteristics of Inclusive Assessment and Accountability Systems.
  http://www.cehd.umn.edu/nceo/onlinepubs/Synthesis40.html



.. _Creating Accessible Media:

************************************************
Create Accessible Media
************************************************

Media-based course materials help to convey concepts and can bring course
information to life. We require all videos in edX courses to include
interactive transcripts that can be read by screen reader software. This
built-in universal design mechanism enhances your course’s accessibility. When
you create your course, you need to factor in time and resources for creating
these transcripts.


=====================================================
Audio Transcripts
=====================================================

Audio transcripts are essential for presenting the readable equivalent of
audio content to learners who cannot hear. They can also be helpful for
learners whose native languages are languages other than English. Synchronized
transcripts allow learners who cannot hear to follow along with the video and
navigate to a specific section of the video by selecting some location within
the transcript text. In addition, all learners can use transcripts of media-
based learning materials for study and review.

A transcript starts with the text version of a video’s spoken content. If you
created your video using a script, you have a great start on creating the
transcript. Just review the recorded video and update the script as needed.
Otherwise, you will need to transcribe the video yourself or engage someone to
do it. There are many companies that will create timed video transcripts
(transcripts that synchronize the text with the video using time codes) for a
fee.

The edX platform supports the use of transcripts in .srt format. When you
integrate a video file into the platform, you should also upload the .srt file
of the timed transcript for such video. See :ref:`Working with Video
Components` for details on how to add timed transcripts.


=====================================================
Descriptions in Video
=====================================================

When you create video segments, consider how you will convey information to
learners who cannot see what is happening in a video. Even if you have audio
transcripts that can be read by screen readers, actions that are only visible
on screen without any audible equivalent are not accessible to learners who
have visual impairments.

For many topics, you can fully cover concepts in the spoken presentation. If
it is practical to do so, you should audibly describe visual events as they
happen in the video. For example, if you are illustrating dropping a coin and
a feather together from a height, you should consider narrating your actions
as you perform them.


=====================================================
Downloadable Transcripts
=====================================================

For both audio and video transcripts, consider including a text file that
students can download and review using tools such as word processing, screen
reader, or literacy software. The downloadable transcript should be text only,
without time codes.


=====================================================
Accessible Media Resources
=====================================================

Accessible Digital Media Guidelines provides detailed advice on creating
online video and audio with accessibility in mind.
http://ncam.wgbh.org/invent_build/web_multimedia/accessible-digital-media-guide


.. _Best Practices for HTML Markup:

************************************************
Use Best Practices for HTML Markup
************************************************
 
HTML is the best format for creating accessible content. It is well supported
and adaptable across browsers and devices. Also, the information in HTML
markup helps assistive technologies, such as screen reader software, to
provide information and functionality to people with vision impairments.

Most of the problem type templates in edX Studio conform to our recommended
best practices in terms of good HTML markup. You can manually add appropriate
HTML tagging even if it does not exist in the component template. Depending on
the type of component you are adding to your course in edX Studio, the raw
HTML data is available either automatically or by selecting the “Advanced
Editor” or “HTML” views.

Keep the following guidelines in mind when you create HTML content.

* Use HTML tags to describe your content’s meaning rather than its appearance.
  For example, you should tag a title with the appropriate heading level (for
  example ``<h2>``) rather than making the heading simply appear like a heading
  by using visual elements such as bold text and a larger font size. Format
  list items as a list rather than using bullets and indents, so that they are
  related in the code. Using HTML to describe your content's meaning is
  valuable for learners who screen readers, which, for example, can read
  through all headings of a specific level or announce the number of items in
  a list.

* Use HTML heading levels in sequential order to represent the structure of a
  document. Well-structured headings help learners and screen reader users to
  navigate a page and find what they are looking for.

* Use HTML list elements to group related items and make content easier to
  skim and read. HTML offers three kinds of lists.

  *  Unordered lists, where the order of items is not important. Each item is
     marked with a bullet.

  *  Ordered lists, where the order of items is important. Each item is listed
     with a number.

  *  Definition lists, where each item is represented using term and
     description pairs (like a dictionary).

* Use table elements to format information that works best in a grid format,
  and include descriptive row and column headings. Tag row and column headers
  with the ``<th>`` element so screen readers can effectively describe the
  content in the table.

====================================================
HTML Markup Resources
====================================================

* Creating Semantic Structure provides guidance on reflecting the semantic
  structure of a web page in the underlying markup (WebAIM).
  http://webaim.org/techniques/semanticstructure/
 
* Creating Accessible Tables provides specific guidance on creating data
  tables with the appropriate semantic structure so that screen readers can
  correctly present the information (WebAIM).
  http://webaim.org/techniques/tables/data


.. _Universal Design for Learning:

************************************************
Apply Universal Design for Learning
************************************************

Universal Design for Learning focuses on delivering courses in a format so
that as many of your learners as possible can successfully interact with the
learning resources and activities you provide them, without compromising on
pedagogic rigor and quality.

The principles of Universal Design for Learning can be summarized by the
following points.

#. Present information and content in various ways. 
#. Provide more than one way for students to express what they know.
#. Stimulate interest and motivation for learning.

Course teams can apply these principles in course design by following several
guidelines.

* Design resources and activities that can be accessed by learners in
  a variety of ways. For example, if there is a text component, provide the
  ability to enlarge the font size or change the text color. For images and
  diagrams, always provide an equivalent text description. For video, include
  text captions or a transcript as well as an audio track.

* Provide multiple ways for learners to engage with information and
  demonstrate their knowledge. This is particularly important to keep in mind
  as you design activities and assessments.
 
* Identify activities that require specific sensory or physical capability and
  for which it might be difficult or impossible to accommodate the
  accessibility needs of learners. For example, an activity that requires
  learners to identify objects by color might cause difficulties for learners
  with visual impairments. In these cases, consider whether there is a
  pedagogical justification for the activity being designed in that way. If
  there is a justification, communicate these requirements to prospective
  learners in the course description and establish a plan for responding to
  learners who encounter barriers. If there is no justification for the
  requirements, edX recommends that you redesign the learning activities to be
  more flexible and broadly accessible.
 
=======================================
Universal Design for Learning Resources
=======================================

* `Delivering Accessible Digital Learning (JISC Techdis) <http://www.jisctechdis.ac.uk/techdis/resources/accessiblecontent>`_ provides a useful overview of an inclusive approach to course design.

* `The National Center on Universal Design for Learning <http://www.udlcenter.org/implementation/postsecondary>`_ provides a helpful overview on Universal Design for Learning.
  


.. _Poll Tool:

###################
Poll Tool
###################

This section describes how to embed polls in your course. 

.. contents::
   :local:
   :depth: 1

*********
Overview 
*********

You can embed a poll in your course. A poll prompts learners to answer. A
learner sees the poll and selects an appropriate answer.

.. image:: ../../../shared/building_and_running_chapters/Images/poll_tool.png
    :alt: A poll as asking the learner's favorite color
    :width: 400

When learners submit answers, they see results of the poll.

.. image:: ../../../shared/building_and_running_chapters/Images/poll_with_results.png
    :alt: A poll as asking the learner's favorite color
    :width: 400

*******************************************
Enable the Poll Tool
*******************************************

Before you can add a poll to your course, you must enable it in Studio or
OLX.

======================================
Enable the Poll Tool in Studio
======================================

#. From the **Settings** menu, select **Advanced Settings**.

#. In the **Advanced Module List** field, place your cursor between the braces,
   and then type ``"poll"``. If you see other values in this field,
   add a comma after the closing quotation mark for the last value, and then
   type ``"poll"``. 
   
   .. image:: ../../../shared/building_and_running_chapters/Images/survey_poll_advanced_setting.png
    :alt: Advanced modules setting for poll
    :width: 400

#. At the bottom of the page, select **Save Changes**.

======================================
Enable the Poll Tool in OLX
======================================

To enable polls in your course, you edit the XML file that defines
the course structure.

Open the XML file for the course in the ``course`` directory. In the ``course``
element's ``advanced-modules`` attribute, add the string ``poll``.

For example, the following XML code enables polls in a course.

.. code-block:: xml

  <course advanced_modules="[&quot;survey&quot;, 
      &quot;poll&quot;]" display_name="Sample Course" 
      start="2014-01-01T00:00:00Z">
      ...
  </course>

***************************
Add a Poll in edX Studio
***************************

Ensure you enable the poll tool before you add the component.

#. On the Course Outline page, open the unit where you want to add the poll.

#. Under **Add New Component** click **Advanced**, and then select **Poll**.
   
   The new component is added to the unit, with the default poll.

   .. image:: ../../../shared/building_and_running_chapters/Images/poll_studio.png
    :alt: The poll component in Studio
    :width: 600

#. In the new component, select **Edit**.
   
#. In the **Display Name** field, enter the name for the component.

#. In the **Question/Prompt** field, enter text that learners see above the
   poll. You can use Markdown in this field.

#. In the **Feedback** field, enter text that learners see after submitting a
   response. You can use Markdown in this field.

#. In the **Private Results** field, to hide poll results from learners,
   select **True**. If you leave the default value, **False**, learners see
   poll results after submitting answers.

#. In the **Maximum Submissions** field, to allow learners to submit answers
   more than once, change the value. Enter **0** to allow unlimited
   submissions.

   .. note:: 
    If you allow learners to submit answers more than once, you should set
    **Private Results** to **True**.

#. Configure answers for the poll.

   #. In each **Answer** field, enter the answer text that learners see.
      
   #. You must enter either text or an image path, or both, for each answer.
      To use an image, us the :ref:`Studio URL <File URLs>` for the image.

   #. If you use an image, you must enter alternative text in the **Image
      alternate text** field.

   #. The poll template contains three answer fields. To add answers, select
      **Add answer** at the bottom of the editor. New answers are added at the
      bottom of the list.

   #. To change the order of answers, select the up and down buttons next to
      each answer.

   #. To remove an answer, select **Delete** next to the answer.

#. Select **Save**.

***************************
Add a Poll in OLX
***************************

To add a poll XBlock in OLX, you create the ``poll`` element. You can embed
the ``poll`` element in the ``vertical`` element, or you can create the
``poll`` element as a stand-alone file that you reference in the vertical.

The following example shows the OLX definition for a poll with two questions.

.. code-block:: xml

  <poll url_name="f4ae7de0006f426aa4eed4b0b8112da5" xblock-family="xblock.v1" 
    feedback="Feedback" 
    display_name="Poll" 
    private_results="false" 
    question="What is your favorite color?" 
    max_submissions="1" 
    answers="[
               [&quot;R&quot;,  
                 {    
                   &quot;img&quot;: &quot;/static/image.png&quot;,    
                   &quot;img_alt&quot;: &quot;Alt 1&quot;,    
                   &quot;label&quot;: &quot;Red&quot;  
                 }
               ],
               [&quot;B&quot;,  
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,    
                   &quot;img_alt&quot;: &quot;Alt 2&quot;,    
                   &quot;label&quot;: &quot;Blue&quot;  
                 }
               ],
               [&quot;G&quot;,  
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,    
                   &quot;img_alt&quot;: &quot;Alt3&quot;,    
                   &quot;label&quot;: &quot;Green&quot;  
                 }
               ],
               [&quot;O&quot;,  
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,    
                   &quot;img_alt&quot;: &quot;Alt 4&quot;,    
                   &quot;label&quot;: &quot;Other&quot;  
                 }
               ]
             ]
  "/>

==========================
poll Element Attributes
==========================

The following table describes the attribute of the ``poll`` element.

.. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - ``url_name``
       - The unique identifier of the poll.
     * - ``xblock-family``
       - The XBlock version used. Must be ``xblock.v1``.
     * - ``private_results``
       - Whether the poll results are shown to learners (``true``) or not
         (``false``).
     * - ``display_name``
       - The display name for the poll.
     * - ``question``
       - The prompt for the poll.
     * - ``feedback``
       - The text shown to learners after they submit a response.
     * - ``max_submissions``
       - The number of times a learner can submit poll answers.  Use ``0`` to
         allow unlimited submissions. If you use a value other than ``1``, set
         ``private_results`` to ``true``.
     * - ``answers``
       - An array of answers in the poll. Each answer has a unique
         identifier, and a dictionary that defines values for the following
         names.

         * ``img``, the static URL of the answer image.
         * ``img_alt``, the alternative text for the image.
         * ``label``, the answer text.
           
         Each answer must have a value for ``img`` or ``label``, or both.
     

***************************
Polls and Grading
***************************

not working?

***************************
Editing Published Polls
***************************

Do not publish a poll until you have completed and tested it. You want to
avoid changing a poll after learners have begun using it.

If you have to edit a poll after learners have submitted answers:

* If you edit the value an answer, previous submissions are
  associated with the new answer value. This change can cause you
  to get an inaccurate picture of the responses.

* If you change the poll so that previous submissions are invalid, those
  submissions are deleted when learners next view the unit. Those learners are
  permitted to submit new responses. However, those learners do not lose credit
  in their course progress.

***************************
View Poll Results
***************************

not working?

.. _Survey Tool:

###################
Survey Tool
###################

This section describes how to embed surveys in your course. 

.. contents::
   :local:
   :depth: 1

*********
Overview 
*********

You can embed a survey in your course. A survey has multiple answers and
multiple questions. A learner sees the survey and selects appropriate answers.

Screenshot

When learners submit answers, they see results

Screenshot

*******************************************
Enable the Survey Tool
*******************************************

Before you can add a survey to your course, you must enable it in Studio or
OLX.

======================================
Enable the Survey Tool in Studio
======================================

#. From the **Settings** menu, select **Advanced Settings**.

#. In the **Advanced Module List** field, place your cursor between the braces,
   and then type ``"survey"``. If you see other values in this field,
   add a comma after the closing quotation mark for the last value, and then
   type ``"survey"``. 
   
   .. image:: ../../../shared/building_and_running_chapters/Images/survey_poll_advanced_setting.png
    :alt: Advanced modules setting for surveys
    :width: 400

#. At the bottom of the page, select **Save Changes**.

======================================
Enable the Survey Tool in OLX
======================================

To enable surveys in your course, you edit the XML file that defines
the course structure.

Open the XML file for the course in the ``course`` directory. In the ``course``
element's ``advanced-modules`` attribute, add the string ``survey``.

For example, the following XML code enables surveys in a course.

.. code-block:: xml

  <course advanced_modules="[&quot;survey&quot;, 
      &quot;poll&quot;]" display_name="Sample Course" 
      start="2014-01-01T00:00:00Z">
      ...
  </course>

***************************
Add a Survey in edX Studio
***************************

Ensure you enable the survey tool before you add the component.

#. On the Course Outline page, open the unit where you want to add the survey.

#. Under **Add New Component** click **Advanced**, and then select **Survey**.
   
   The new component is added to the unit, with the default survey.

   Screenshot

#. In the new component, select **Edit**.
   
#. In the **Display Name** field, enter the name for the component.

#. In the **Feedback** field, enter text that learners see after submitting
   answers.

#. In the **Private Results** field, to hide survey results from learners,
   select **True**. If you leave the default value, **False**, learners see
   survey results after submitting answers.

#. In the **Maximum Submissions** field, to allow learners to submit answers
   more than once, change the value. Enter **0** to allow unlimited
   submissions.

   .. note:: 
    If you allow learners to submit answers more than once, you should set
    **Private Results** to **True**.

#. Configure answers for the survey. Each answer is displayed to learners as a
   column, which a radio button they can select. The answers apply to all
   survey questions.

   #. In each **Answer** field, enter the answer text that learners see as the
      column heading.

   #. The survey template contains three answer fields. To add answers, select
      **Add answer** at the bottom of the editor. New answers are added at the
      bottom of the list.

   #. The top answer in the list is displayed to learners as the left-most
      answer column in the survey, and the bottom answer is displayed in the
      right-most column.  To change the order of answers, select the up and
      down buttons next to each answer.

   #. To remove an answer, select **Delete** next to the answer.

#. Configure questions for the survey. Each question is displayed to learners
   in the left-most column.

   #. You must enter either text or an image path, or both, for each question.
      To use an image, us the :ref:`Studio URL <File URLs>` for the image.

   #. The survey template contains three questions. To add questions, select
      **Add question** at the bottom of the editor. New questions are added at
      the bottom of the list.
   
   #. If you use an image, you must enter alternative text in the **Image
      alternate text** field.

   #. Questions are displayed to learners as rows in the order you configure
      them. To change the order of questions, select the up and down buttons
      next to each question.

   #. To remove a question, select **Delete** next to the question.

#. Select **Save**.

***************************
Add a Survey in OLX
***************************

To add a survey XBlock in OLX, you create the ``survey`` element. You can embed
the ``survey`` element in the ``vertical`` element, or you can create the
``survey`` element as a stand-alone file that you reference in the vertical.

The following example shows the OLX definition for a survey with two questions.

.. code-block:: xml

  <survey 
    url_name="unique identfier for the survey" 
    xblock-family="xblock.v1" 
    questions="[  
                 [&quot;unique code for question 1&quot;,
                   {
                     &quot;img&quot;: &quot;Static URL to image&quot;,      
                     &quot;img_alt&quot;: &quot;Alternative text for image&quot;,      
                     &quot;label&quot;: &quot;Text of question 1&quot;    
                   }  
                 ],  
                 [&quot;unique code for question 2&quot;,    
                   {
                     &quot;img&quot;: &quot;Static URL to image&quot;,      
                     &quot;img_alt&quot;: &quot;Alternative text for image&quot;,      
                     &quot;label&quot;: &quot;Text of question 2&quot;    
                    }  
                  ]
                ]" 
    feedback="Feedback displayed to learner after submission" 
    private_results="false" 
    block_name="Display name for survey" 
    max_submissions="1" 
    answers="[  
              [
                &quot;Unique identifier for answer 1&quot;,    
                &quot;Answer text&quot;  
              ],  
              [   
                &quot;Unique identifier for answer 2&quot;,    
                &quot;Answer text&quot;  
              ] 
            ]"
  />

==========================
survey Element Attributes
==========================

The following table describes the attribute of the ``survey`` element.

.. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - ``url_name``
       - The unique identifier of the survey.
     * - ``xblock-family``
       - The XBlock version used. Must be ``xblock.v1``.
     * - ``questions``
       - An array of questions in the survey. Each question has a unique
         identifier, and a dictionary that defines values for the following
         names.

         * ``img``, the static URL of the question image.
         * ``img_alt``, the alternative text for the image.
         * ``label``, the question text.
           
         Each question must have a value for ``img`` or ``label``, or both.
     * - ``answers``
       - An array of answers in the survey. Each answer and answer text.
     * - ``feedback``
       - The text shown to learners after they submit a response.
     * - ``private_results``
       - Whether the survey results are shown to learners (``true``) or not
         (``false``).
     * - ``block_name``
       - The display name for the survey.
     * - ``max_submissions``
       - The number of times a learner can submit survey answers.  Use ``0`` to
         allow unlimited submissions. If you use a value other than ``1``, set
         ``private_results`` to ``true``.

***************************
Surveys and Grading
***************************

not working?

***************************
Editing Published Surveys
***************************

Do not publish a survey until you have completed and tested it. You want to avoid changing a survey after learners have begun using it.

If you have to edit a survey after learners have submitted answers:

* If you edit the value a question or answer, previous submissions are
  associated with the new question or answer value. This change can cause you
  to get an inaccurate picture of the responses.

* If you change the survey so that previous submissions are invalid, those
  submissions are deleted when learners next view the unit. Those learners are
  permitted to submit new responses. However, those learners do not lose credit
  in their course progress.

***************************
View Survey Results
***************************

not working?


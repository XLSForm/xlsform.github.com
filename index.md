---
layout: page
---
{% include JB/setup %}

## Getting started

This document will help you author surveys for ODK Collect using xlsform syntax.
ODK Collect is a powerful tool to rapidly gather complex data types in the field using Android smartphones.
The software is free, the source code is open, and the community is very active.
Using ODK Collect with Formhub requires the creation of an Excel file that contains the questions,
formatting instructions and data validation conditions that will allow enumerators collect data on smartphones.
The following module will cover all the syntax elements you will need to author basic and advanced surveys.


Here are the steps involved in writing a survey with the XLSform format and getting it quickly deployed on formhub.


Write a survey using the XLSform syntax described below and save it as an .xls file.

Upload your .xls file into formhub.

Link ODK Collect to your formhub account, download forms, and start collecting data!
Basic Survey Authoring

### Your first question

Survey authoring in Excel is a simple process once you understand the basic XLSform syntax.

To make your learning process smoother a generic household survey example will be used across the training modules.
This sample survey is a subset of the CDC Household Water Use and Health Survey for a Water Safety Plan.
You can download the full Excel survey file form Formhub University, the name of the form is household_survey.


![](/assets/img/getting_started_1.png)


1. We will save the survey with the file name household_survey.xls.
2. There is a single worksheet name 'survey' this is where all questions should be located (each row in this worksheet is a question in your survey).
3. There are three columns 'type', 'name', and 'label'. The 'type' column describes the question type (text, number, photo, ...). The 'name' column assigns a unique variable name that will serve as a reference to the survey question (the name must be unique, must begin with a letter, and can only contain letters, numbers, dashes (-) and underscores (_)). The 'label' column contains the text that will actually be presented on the Android smartphone .
4. The survey pictured above has one basic questions which asks "What is your full name?" (the ‘label’) and presents a text input box (as specified in the ‘type’ column) to the surveyor.Once data has been collected and sent to the server the data results Excel file that can be downloaded from Formhub will have a column called ‘respondent_name’ (the identifier for this question as specified in the ‘name’ column)
5. This file is saved in the 'Excel 97-2004 Workbook (.xls)' format.

This form would look like the following on your Android smartphone:

![](/assets/img/getting_started_string.png)

Important rules to remember:

1. Make sure your file is saved in the .xls format and contains no spaces or special characters (‘-’ and ‘_’ are allowed).
2. Make sure that your column headers are in lowercase (i.e. “label” or “name”, not “Label” or “Name”)
3. Make sure that your sheet names are appropriately named (i.e. “survey” not “Sheet 1”, “Survey” or “surveys”)
4. Make sure that the question names are unique and do not contain spaces or special characters (‘-’ and ‘_’ are allowed).

Now let’s start populating the survey questionnaire. The first section will likely include basic information such as the respondent’s name, age of the respondent, household number, etc.  We already know how to collect the name. For age, household number, and other fields, ODK lets us specify the “type” of the information to be entered (numbers, dates, etc). This will help us reduce data entry errors. To do this we can use a different question ‘type’, ODK Collect has defined a number question types to support all data types that surveys usually collect.  Here we present some of the most basic types ODK Collect supports (you’ll see the full list later).

| type | label |
| ---- | ----- |
| text | Text input |
| integer | Integer (ie, whole number) input. |
| decimal | Decimal input. |

Let’s add the household id and respondent’s age as numeric integer fields
and the respondent’s name as a simple alphanumeric field.
This will require the use of the ‘type’ ‘text’ and the ‘type’ ‘integer’.


![](/assets/img/getting_started_2.png)

An integer field would look like this on the Android smartphone.


![](/assets/img/getting_started_int.png)

Notice how the numeric keypad appears automatically and the alphabetic keyboard is deactivated.
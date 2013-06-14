---
published: true
layout: page
title: New Data Types
tags: [ types, beginner ]
category: intro
---

{% include JB/setup %}

For those of you coming from paper surveys,
you will appreciate that Android smartphones can help us collect “new” kinds of data,
like GPS co-ordinates, images, audio, video, and information encoded in barcodes and QR codes.
For now, we’ll introduce you to two of these question types: ‘geopoint’ and ‘image’.


**geopoint** - Collect GPS coordinates.

![geopoint](/assets/img/collect_geopoint.png)

**image** - Take a photograph.

![capture image](/assets/img/collect_image.png)

Let’s collect the gps coordinates and a picture of the household using the following XLSform.
To make this tutorial easier to read we will switch from the Excel file screenshots to a tabular notation.


Excel 'survey' worksheet

| type | name | label |
| ---- | ---- | ----- |
| text | interviewer | A.1.0 Interviewer name |
| integer | hh_id | A.1.1 Enter the household number |
| geopoint | hh_location | A.1.2 Collect the GPS coordinates of this household |
| image | hh_photo | A.1.3 Take a picture of the structure where the household lives |
| text | respondent_name | A.1.4 Enter the full name of the respondent |
| integer | respondent_age | A.1.5 Enter the age of the respondent |

Notice how the Excel ‘a_worksheet_name’ worksheet preceding the table specifies on
which worksheet of the workbook we are working on (we have been working on the Excel ‘survey’ worksheet
for now but other worksheets will be added as we develop a more advanced survey).




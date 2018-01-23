## Table description

The Desk Tracker patron counts are entered by some branch libraries at varying intervals, often hourly but it may vary. 
They are really a sub query from a larger table.

## Fields

**response_set:** <integer> The unique id of the response set. A response set includes all of the
                             data submitted on a data entry page. For example, if you fill out "Contact Type" 
                             and "Purpose of Visit" fields on your "Activity" page*, the generated file would 
                             contain one row for each of the two responses, each with the same response_set value. 
                             The response_set column allows you to group your responses by page submission.

**response_id:** <integer> 	The unique id of the response. Each row will have a different value in the response_id field.

**parent_response_id:** <integer> For followup responses only. The parent_response_id corresponds to the response_id of 
                              the question which triggered the followup. Use this field to link an initial data submission 
                              with all of the subsequent followup data. **UNUSED**

**date_time:** <datetime> The time and date of the data entry. The time value reflects your timezone. Remember, 
                              the timestamp is determined by the Desk Tracker server, and is not related to the 
                              clock settings on the local computer. **Format: _MM/DD/YYYY HH:MM_**
                              
**page:** 	<string> The name of the data entry page, or tab, by which the data was submitted. They will all be patron count. Not useful.

**question:** <string> Further categorization. Three values: **_Patron Count_**, **_Patron Count for Access Services_**, 
                           and **_Patron Count by Location_**. 
                           
**response:** <string> Provides the location. **RENAME: _location_**.

**optional_text:** <integer> The number of patrons counted. **RENAME: _count_**.

**user:** <string> The email prefix of the person entering the data.

**branch:** <string> The branch where the data was submitted. Along with **response/location** provides a more 
                               specific location for the data.
                               
**desk:** <string> The desk where the data was entered. Not too useful as the count does not really pertain to the desk.

**library:** <string> 	The library where the data was submitted. Not too useful. Always Pennsylvania State University






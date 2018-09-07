Date Range Batch Search
=======
You can use this tool to search for resources added to OCLC
within a given date range (for example, everything with
"mice" in the title added since last October). This can be
useful for when a patron would like to do an exhaustive search
of WorldCat, repeated over time, and the resources added are
likely to be older (making restriction by publication date
less useful).

### 1. Build your query (without the date aspect)

 To run your query in batch, you will need to know how to enter
 it as a command line search using the
 [OCLC keyword indexes](https://help.oclc.org/Librarian_Toolbox/Searching_WorldCat_Indexes). 

 Examples: 
 * ``am:uknowledge ti:science`` -- records with "uknowledge" in a URL in 856$u and "science" in a title field
 * ``kw:sanborn w map`` -- records containing "sanborn map" (in keyword indexed fields)

 Index codes for many fields appear on the drop-down menu when
 you use them to search in OCLC Connexion:

 ![](images/DRBS-OclcIndexTI.PNG?raw=true)

 Note that adding ``ll:eng`` or similar to your query is useful if you want
 to retrieve only records with a given language of cataloging (note that 
 this is different from the language of the cataloged work).

### 2. Create your batch query file

 On the [Date Range Batch Search](https://ukcts.org/Connexion/DateRangeBatchSearch.html?beg=20180801&end=20180825&query=kw%3Achange+ti%3Aparable) page, 
 choose the start and end date for your date range from the date pickers:

 ![](images/DRBS-DatePickers.PNG?raw=true)

 Enter the search query you created and notice that it create a list of
 queries, one for each date in your range (dm: is the date the MARC
 record was created in OCLC)

 ![](images/DRBS-Search.PNG?raw=true)

 Click the Download button to download your list of search queries
 as a text file. Make a note of where you save it -- you'll need
 this file in a few steps.

### 3. Change (or confirm) your Connexion settings

 In Connexion, click Options -> Preferences and go to the Batch tab.
 Set max number of records to 150 (the highest it will go).

 ![](images/DRBS-settings150.PNG?raw=true)

### 4. Create a local file to hold the search results.

 In Connexion, open the local file manager with File -> Local File
 Manager...

 ![](images/DRBS-LocalFile.PNG?raw=true)

 Click "Create File..." and type in a name for your search results
 (like "Sanborn") and click "Open" to create the file. 

 The file you just created should now appear on the file list, so
 double-click it to set it as the default file. A red check should
 now appear next to it.

 ![](images/DRBS-RedCheck.PNG?raw=true)

 Click the Close button.

### 5. Enter bibliographic search keys.

 In Connexion, click Batch -> Enter Bibliographic Search Keys...

 ![](images/DRBS-EnterKeys.PNG?raw=true)

 Confirm that the file you just created appears in the Local file box.

 Set the default index to "None".

 Click Import to import the text file you created in Step 2.

 When prompted, don't delete the original file (unless you really want to).

 Click Save and then Close to go to the next step.

### 6. Run the batch query

 In Connexion, click Batch -> Process Batch...

 Check the box in the row with your file in it. It should already have a
 red checkmark next to it. 

 ![](images/DRBS-ProcessBatch.PNG?raw=true)

 Check the box in the Process area for Online Searches. Click OK to
 start the search.

 Depending on the date range, this may take a while! You can see the
 progress as the queries scroll by and it downloads the records it
 finds into your local save file.

### 7. Address any errors

 In the batch search results, most searches will likely result in
 a "No records found for your search" error -- this is expected!
 A report of your actual results are below these in the "Successful
 searches" section.

 If you see other type of errors, like a search timing out, or 
 having more than 150 results, you'll have to run that query by
 hand to add in the search results.

 Go to the regular search box (Cataloging -> Search -> Worldcat...) and
 paste the query that had an error into the top Command Line Search
 box and clicking OK.

 ![](images/DRBS-Error.PNG?raw=true)

 If there are any results, select them from the search results list
 and click Action -> Save Record to Local File to save all selected
 records to your local file.

 Your local save file should now contain all results of your query
 added to Worldcat between the specified dates.

 ***NOTE:*** It appears that for certain kinds of OCLC records, the
 Date Entered can change. Your results from this process might include
 records that have been re-loaded in some way by OCLC, keeping their
 OCLC numbers but gaining fresh creation dates. Not sure how common
 this is, but you might get some oldies in your search. Hopefully not
 too many!

Copyright Kathryn Lybarger and distributed under CC-BY-SA.

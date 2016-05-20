#DigitalGlobe GBDX AnswerFactory Help#
----------

#Web Client Help#
[Logging In](#logging-in) <br>
[Create Project Page Layout](#create-project) <br>
[Open Project Page Layout](#open-project) <br>
[Project Information](#project-information) <br>
[Answers](#answers) <br>
<br><br>
##Logging In##
Logging in retrieves a GBDX token. <br>
![Login page image](/images/ui_helpdoc/loginbox.png "Login Box for login page") <br>
Enter your GBDX credentials. If you do not have GBDX credentials, [click here](https://gbdx.geobigdata.io/account/self_registration/). <br>
To see the release notes, click on the What's New button.
<br><br><br>
##Page Layout##
###Create Project###
![Create Project page layout image](/images/ui_helpdoc/createproject-pagelayout.png "Create Project page layout") <br>
<br>
___
![Open Project button image](/images/ui_helpdoc/openbutton.png "Open Project button") Click to switch to Viewing projects.
___
![Create Project button image](/images/ui_helpdoc/createbutton.png "Create Project button") Click to switch to Creating projects.
___
![Log out button image](/images/ui_helpdoc/logoutbutton.png "Log out button") Click to log out of AnswerFactory.
___
![Zoom in/out button image](/images/ui_helpdoc/zoombuttons.png "Zoom In/Out buttons") Click to zoom in or out on the map. The mouse wheel can also be used to zoom.
___
![Legend icon image](/images/ui_helpdoc/legendicon.png "Legend icon") Hover over icon to see the layer list. Layers may be toggled on and off, and basemap may be changed here. There are currently two possible basemaps.
___
![Help button image](/images/ui_helpdoc/helpicon.png "Help icon") Click to reach the help pages.
___
![Upload shapefile button image](/images/ui_helpdoc/uploadbutton.png "Upload shapefile button") Click to open your computer directory to upload a **zipped** shapefile (including all necessary components of .dbf, .prj, .shp, and .shx); this shapefile will serve as your aoi, and the map will automatically snap to the shapefile once upload is complete. Aoi(s) display in *pink*.
___
![Draw button image](/images/ui_helpdoc/draw.png "Draw button") Click to activate draw capability. Single click on map to drop the vertices of your aoi, and double-click to complete an aoi. Draw remains active, and you may draw any number of aois. Once you have completed drawing aois, click Draw button again to deactivate continued drawing capability. Aoi(s) display in *pink*.
___
<br>
Once an aoi is added or created, more functionality is exposed. <br>
![Create Project with aoi present page layout image](/images/ui_helpdoc/createproject-pagelayout2.png "Create Project with aoi present page layout") <br>
<br>
___
**Project name** - Text field to enter a name for your project.
___
**Buffer size** - Text field to enter a value for a buffer around your aoi(s), in meters.
___
![Compute button image](/images/ui_helpdoc/computebutton.png "Compute button") Click to compute and add the buffer surrounding the aoi(s). The buffer will display in *orange*.
___
**Feature name field** - Dropdown is *only populated with uploaded aois*. Select the field that aois will be grouped by.
___
**Available answers** - Dropdown holds the list of answers that may be added to the project. More than one answer may be added to a single project.
___
![Add Answer button image](/images/ui_helpdoc/addanswerbutton.png "Add Answer button") Click to add the selected answer to the project. Answers added to the project will appear on the right of the screen.
___
![Reset project button image](/images/ui_helpdoc/resetbutton.png "Reset project button") Click to clear all layers and answers to start over from scratch.
___
![Save button image](/images/ui_helpdoc/savebutton.png "Save button") Click to save the project once you have set all of your specifications.
___

###Open Project###
![Open Project page layout image](/images/ui_helpdoc/openproject-pagelayout.png "Open Project page layout") <br>
<br>
___
![Open Project button image](/images/ui_helpdoc/openbutton.png "Open Project button") Click to switch to Viewing projects.
___
![Create Project button image](/images/ui_helpdoc/createbutton.png "Create Project button") Click to switch to Creating projects.
___
![Log out button image](/images/ui_helpdoc/logoutbutton.png "Log out button") Click to log out of AnswerFactory.
___
![Zoom in/out button image](/images/ui_helpdoc/zoombuttons.png "Zoom In/Out buttons") Click to zoom in or out on the map. The mouse wheel can also be used to zoom.
___
![Legend icon image](/images/ui_helpdoc/legendicon.png "Legend icon") Hover over icon to see the layer list. Layers may be toggled on and off, and basemap may be changed here. There are currently two possible basemaps.
___
![Help button image](/images/ui_helpdoc/helpicon.png "Help icon") Click to reach the help pages.
___
![Show projects toggle image](/images/ui_helpdoc/myprojectstoggle.png "Show my projects toggle") Toggle on viewing solely projects you have created, or leave toggled off to view all projects created in *your account*.
___
![Refresh button image](/images/ui_helpdoc/refreshbutton.png "Refresh button") Click to force refresh the project list manually. Project list automatically updates once a minute.
___
![Search bar image](/images/ui_helpdoc/searchbar.png "Search Bar") Type text to dynamically filter project list by project name.
___
![Project list page navigation image](/images/ui_helpdoc/pagenavigation.png "Project list page Navigation") There are several ways to move through the pages of the list of projects in your account. Click on the arrows to jump forward or back through pages. Click on the visible numbers to jump to that page. Click on the dropdown to select any specific page to jump to.
___
<br>
Once you have found your desired project, click on the project in the list to view it and update the visible functionality. The map will automatically snap to the project aoi, and the IDAHO imagery that encompasses the aoi will be overlaid on top of the basemap. IDAHO imagery may be toggled off from the Legend.
<br>
![Viewing Project page layout image](/images/ui_helpdoc/openproject-pagelayout2.png "Viewing a project page layout") <br>
<br>
___
![minimize button image](/images/ui_helpdoc/minimizeicon.png "Minimize button") Click to minimize the window. Click again to bring the window back to full view.
___
<br>
####Project Information####
![Project Info image](/images/ui_helpdoc/projectinfo.png "Project information window")
<br>
Project window lists the information for the selected project, including the answers that are currently associated with the project. You may add and remove answers from the project from this window.
___
![Return to Project List icon image](/images/ui_helpdoc/returntolist.png "Return to project list icon") Click to return to the list of projects.
___
![Remove answer button image](/images/ui_helpdoc/removeanswer.png "Remove answer button") Click to remove an answer from the project. *Note: you must click the Update button to update the project after altering it.*
___
**Available answers** - Dropdown holds the list of answers that may be added to the project. More than one answer may be added to a single project.
___
![Add Answer button image](/images/ui_helpdoc/addanswerbutton.png "Add Answer button") Click to add the selected answer to the project. Answers added to the project will appear on the right of the screen.
___
![Delete project button image](/images/ui_helpdoc/deletebutton.png "Delete project button") Click to delete project from AnswerFactory.
___
![Update button image](/images/ui_helpdoc/updatebutton.png "Update button") Click to save any changes made to the project.
___
<br>
####Answers####
![Answers List image](/images/ui_helpdoc/answerslist.png "Answers List")
<br>
The answer results are displayed here. If an answer is still processing, it will display as "Currently running..." Any completed answers will display as "Show..." To view a completed answer, click on it.
<br>
![Answer table image](/images/ui_helpdoc/answertable.png "Answer Table")
<br>
A table will appear to display the results. Each row represents an aoi. Clicking on a cell in the table will query the results to display on the map. *With exception to cells in "Query & Summarize" answers, which are non-clickable.*
<br>
![Table with answers displayed on map image](/images/ui_helpdoc/viewanswers.png "Answers viewed in both table and on map")
<br>
You can hover over vectors on the map to view metadata.
<br>
___
![Item Type button image](/images/ui_helpdoc/itemtypes.png "Item types button example") When the results have different types, the various types display in the table. Click on a specific type to see only those results in the table, or click on total to see all of them.
___
![Column visibility column options image](/images/ui_helpdoc/columnoptions.png "Column visibility column options") Click on column visibility to display the column options, and click on the options to turn them on or off.
___
![Copy button image](/images/ui_helpdoc/copybutton.png "Copy button") Click to copy table row(s) to clipboard.
___
![Print button image](/images/ui_helpdoc/printbutton.png "Print button") Click to print table.
___
![CSV button image](/images/ui_helpdoc/csvbutton.png "CSV button") Click to save table in CSV format.
___
![PDF button image](/images/ui_helpdoc/pdfbutton.png "PDF button") Click to save table in PDF format.
___
![Table entries display option image](/images/ui_helpdoc/tableentryreturn.png "Number of entries displayed in the table") Click the dropdown to select the number of rows visible in the table at a time.
___
![Table search bar image](/images/ui_helpdoc/tablesearch.png "Table search bar") Type to dynamically search the table when looking for a specific aoi.
___
![Show All Results button image](/images/ui_helpdoc/showallbutton.png "Show All Results button") Click to display all the results for the given answer for the project over all of the aois.
___
![Table page navigation image](/images/ui_helpdoc/tablenavigation.png "Table page navigation") Click on the arrows to move between pages, or click on a specific page number to jump to the page.
___
<br><br><br>

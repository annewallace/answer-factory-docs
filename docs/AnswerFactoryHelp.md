#DigitalGlobe GBDX AnswerFactory Help#
----------

#Contents#
[Logging In](#logging-in) <br>
[AnswerFactory Overview](#answerfactory-overview)<br>
[Open Project Page Layout](#open-project-page-layout) <br>
[View Project Page Layout](#view-project-page-layout)<br>
[Project Information](#project-information) <br>
[Answers](#answers) <br>
[Create Project Page Layout](#cp-page-layout) <br>
[Answer Types](#answer-types) <br>
<br><br>

#Logging In#
If you already have GBDX credentials, [log in to AnswerFactory](https://vector.geobigdata.io/answer-factory/login). If you do not have GBDX credentials, create an account with GBDX by using our [online registration tool](https://gbdx.geobigdata.io/account/self_registration/). Note that if your company already has an account, your account administrator will need to add you as a user to the account. If you are an account administrator, see the guide for [adding users to your account](http://gbdxdocs.digitalglobe.com/docs/video-lesson-how-to-add-users-to-your-account). <br>
Once you have reached the login screen, you may check the release notes by clicking on the What's New button, or you may simply enter your GBDX credentials and continue into AnswerFactory. <br>
![Login page image](../images/ui_helpdoc/loginbox.PNG "Login Box for login page")

<br><br><br>

#AnswerFactory Overview#
There are two main components in the AnswerFactory web application. <br><br>
___
Open Project - From the Open Project page, you can find previously created projects and view the answer results or check on the progress of the answers being processed.
___
Create Project - From the Create Project page, you can target your area of interest and choose the answers you want to see for your aoi.
___
<br><br>
In both components, you will see some universal tools. <br><br>
___
![Open Project button image](../images/ui_helpdoc/openbutton.PNG "Open Project button") Click to switch to Viewing projects.
___
![Create Project button image](../images/ui_helpdoc/createbutton.PNG "Create Project button") Click to switch to Creating projects.
___
![User Info dropdown image](../images/ui_helpdoc/userinfobase.PNG "User Info Dropdown") Shows the user currently logged in. Click to see the menu options available to the user. There are currently two available options: View your **Account Usage** stats or **Log Out** of AnswerFactory.
___
![Zoom in/out button image](../images/ui_helpdoc/zoombuttons.PNG "Zoom In/Out buttons") Click to zoom in or out on the map. The mouse wheel can also be used to zoom.
___
![Legend icon image](../images/ui_helpdoc/legendicon.PNG "Legend icon") Hover over icon to see the layer list. Layers may be toggled on and off, and basemap may be changed here. There are currently two possible basemaps.
___
![Help button image](../images/ui_helpdoc/helpicon.PNG "Help icon") Click to reach the help pages.
___
<br><br>

##Open Project##
Upon login, you will first be directed to the Open Project page.

###Open Project Page Layout###
![Open Project page layout image](../images/ui_helpdoc/openproject-pagelayout.PNG "Open Project page layout")

<br><br>
___
![Show my projects toggle image](../images/ui_helpdoc/myprojectstoggle.PNG "Show my projects toggle") Toggle on viewing solely projects you have created, or leave toggled off to view all projects created in your group account.
___
![minimize button image](../images/ui_helpdoc/minimizeicon.PNG "Minimize button") Click to minimize the window. Click again to bring the window back to full view.
___
![Refresh button image](../images/ui_helpdoc/refreshbutton.PNG "Refresh button") Click to force refresh the project list manually. Project list automatically updates once a minute.
___
![Search bar image](../images/ui_helpdoc/searchbar.PNG "Search Bar") Type text to dynamically filter project list by project name.
___
![Project list page navigation image](../images/ui_helpdoc/pagenavigation.PNG "Project list page Navigation") There are several ways to move through the pages of the list of projects in your account. Click on the arrows to jump forward or back through pages. Click on the visible numbers to jump to that page. Click on the dropdown to select any specific page to jump to.
___
<br><br>
To get started, find the project you would like to view and click on it in the project listing. This will drill down to the View Project level.
<br><br>

###View Project Page Layout###
Once you have entered your desired project, you will notice a change in the accessible functionality on the page. The map will automatically snap to the project aoi, and the IDAHO imagery that encompasses the aoi will be overlaid on top of the basemap. IDAHO imagery may be toggled off from the Legend.
<br>
![Viewing Project page layout image](../images/ui_helpdoc/openproject-pagelayout2.PNG "Viewing a project page layout")
<br><br>

####Project Information####
![Project Info image](../images/ui_helpdoc/projectinfo.PNG "Project information window")
<br>
Project window lists the information for the selected project, including the answers that are currently associated with the project. You may add and remove answers from the project from this window.
___
![Return to Project List icon image](../images/ui_helpdoc/returntolist.PNG "Return to project list icon") Click to return to the list of projects.
___
![minimize button image](../images/ui_helpdoc/minimizeicon.PNG "Minimize button") Click to minimize the window. Click again to bring the window back to full view.
___
![Remove answer button image](../images/ui_helpdoc/removeanswer.PNG "Remove answer button") Click to remove an answer from the project. *Note: you must click the Update button to update the project after altering it.*
___
**Available answers** - Dropdown holds the list of answers that may be added to the project. More than one answer may be added to a single project. For a list of possible answers and their descriptions, [go here](#answer-types).
___
![Add Answer button image](../images/ui_helpdoc/addanswerbutton.PNG "Add Answer button") Click to add the selected answer to the project. Answers added to the project will appear on the right of the screen.
___
![Delete project button image](../images/ui_helpdoc/deletebutton.PNG "Delete project button") Click to delete project from AnswerFactory.
___
![Update button image](../images/ui_helpdoc/updatebutton.PNG "Update button") Click to save any changes made to the project.
___
<br>

####Answers####
![Answers List image](../images/ui_helpdoc/answerslist.PNG "Answers List")
<br>
The answer results are displayed here. If an answer is still processing, it will display as "Currently running..." Any completed answers will display as "Show..." To view a completed answer, click on it.
<br>
![Answer table image](../images/ui_helpdoc/answertable.PNG "Answer Table")
<br>
A table will appear to display the results. Each row represents an aoi. Clicking on a cell in the table will query the results to display on the map.
<br>
![Table with answers displayed on map image](../images/ui_helpdoc/viewanswers.PNG "Answers viewed in both table and on map")
<br>
You can hover over vectors on the map to view metadata.
<br>
___
![Item Type button image](../images/ui_helpdoc/itemtypes.PNG "Item types button example") When the results have different types, the various types display in the table. Click on a specific type to see only those results in the table, or click on total to see all of them.
___
![Column visibility column options image](../images/ui_helpdoc/columnoptions.PNG "Column visibility column options") Click on column visibility to display the column options, and click on the options to turn them on or off.
___
![Copy button image](../images/ui_helpdoc/copybutton.PNG "Copy button") Click to copy table row(s) to clipboard.
___
![Print button image](../images/ui_helpdoc/printbutton.PNG "Print button") Click to print table.
___
![CSV button image](../images/ui_helpdoc/csvbutton.PNG "CSV button") Click to save table in CSV format.
___
![PDF button image](../images/ui_helpdoc/pdfbutton.PNG "PDF button") Click to save table in PDF format.
___
![Table entries display option image](../images/ui_helpdoc/tableentryreturn.PNG "Number of entries displayed in the table") Click the dropdown to select the number of rows visible in the table at a time.
___
![Table search bar image](../images/ui_helpdoc/tablesearch.PNG "Table search bar") Type to dynamically search the table when looking for a specific aoi.
___
![Show All Results button image](../images/ui_helpdoc/showallbutton.PNG "Show All Results button") Click to display all the results for the given answer for the project over all of the aois.
___
![Table page navigation image](../images/ui_helpdoc/tablenavigation.PNG "Table page navigation") Click on the arrows to move between pages, or click on a specific page number to jump to the page.
___
<br><br>

##Create Project##
###Create Project Page Layout###
![Create Project page layout image](../images/ui_helpdoc/createproject-pagelayout.PNG "Create Project page layout")

<br><br>
___
![minimize button image](../images/ui_helpdoc/minimizeicon.PNG "Minimize button") Click to minimize the window. Click again to bring the window back to full view.
___
![Upload shapefile button image](../images/ui_helpdoc/uploadbutton.PNG "Upload shapefile button") Click to open your computer directory to upload a **zipped** shapefile (including all necessary components of .dbf, .prj, .shp, and .shx); this shapefile will serve as your aoi, and the map will automatically snap to the shapefile once upload is complete. Aoi(s) display in *pink*.
___
![Draw button image](../images/ui_helpdoc/drawbutton.PNG "Draw button") Click to activate draw capability. Single click on map to drop the vertices of your aoi, and double-click to complete an aoi. Draw remains active, and you may draw any number of aois. Once you have completed drawing aois, click Draw button again to deactivate continued drawing capability. Aoi(s) display in *pink*.
___
<br>
Once an aoi is added or created, more functionality is exposed. <br>
![Create Project with aoi present page layout image](../images/ui_helpdoc/createproject-pagelayout2.PNG "Create Project with aoi present page layout")

<br><br>
___
**Project name** - Text field to enter a name for your project.
___
**Buffer size** - Text field to enter a value for a buffer around your aoi(s), in meters.
___
![Compute button image](../images/ui_helpdoc/computebutton.PNG "Compute button") Click to compute and add the buffer surrounding the aoi(s). The buffer will display in *orange*.
___
**Feature name field** - Dropdown is *only populated with uploaded aois*. Select the field that aois will be grouped by.
___
**Available answers** - Dropdown holds the list of answers that may be added to the project. More than one answer may be added to a single project. For a list of possible answers and their descriptions, [go here](#answer-types).
___
![Add Answer button image](../images/ui_helpdoc/addanswerbutton.PNG "Add Answer button") Click to add the selected answer to the project. Answers added to the project will appear on the right of the screen.
___
![Reset project button image](../images/ui_helpdoc/resetbutton.PNG "Reset project button") Click to clear all layers and answers to start over from scratch.
___
![Save button image](../images/ui_helpdoc/savebutton.PNG "Save button") Click to save the project once you have set all of your specifications.
___
<br><br>

##Answer Types##
The following is a list of possible answers that you may add to projects.
___
**Extract Aircrafts** - Runs an algorithm over a raster acquisition to identify aircrafts in the image and generate vectors with information on and to notate where the aircrafts are. There are three subtypes of aircraft currently being detected: Airliner, Fighter, and Helicopter. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Aircrafts.JPG). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/bi50oss7bz).
___
**Extract Aircrafts Change** - Runs Extract Aircrafts algorithm over multiple time series raster acquisitions and then compares the resulting vector outputs, displaying the difference.
___
**Extract Built-Up Areas** - Runs an algorithm over a raster acquisition to identify areas with man-made structures in the image and generate vectors with information on and to notate where the structures are. Note that discovering built-up areas is not synonymous with extracting individual buildings; an entire city may generate a single vector as a "built-up area." To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/BuiltUp_Areas.jpg). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/48718t7mal).
___
**Extract Built-Up Areas Change** - Runs Extract Built-Up Areas algorithm over multiple time series raster acquisitions and then compares the resulting vector outputs, displaying the difference.
___
**Extract Foliage** - Runs an algorithm over a raster acquisition to identify foliage in the image and generate vectors with information on and to notate where the foliage is. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Foliage1.jpg). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/vvkyb4a4jn).
___
**Extract LULC** - Standing for Land Use Land Cover, this runs an algorithm over a raster acquisition to identify various LULC types, such as Barren Soil, in the image and generate vectors with information on and to notate where the various types of LULC are. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/LULC.JPG).
___
**Extract LULC Change** - Runs Extract LULC algorithm over multiple time series raster acquisitions and then compares the resulting vector outputs, displaying the difference.
___
**Extract Oilfields** - Runs an algorithm over a raster acquisition to identify oilfields in the image and generate vectors with information on and to notate where the oilfields are. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/OilFields.JPG). 
___
**Extract Rivers** - Runs an algorithm over a raster acquisition to identify rivers in the image and generate vectors with information on and to notate where the rivers are. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Rivers.JPG). 
___
**Extract Roads** - Runs an algorithm over a raster acquisition to identify roads in the image and generate vectors with information on and to notate where the roads are. There are three subtypes of aircraft the user may detect on: Dirt Urban, Suburban, and Trails. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Roads.JPG). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/1lmngax11l).
___
**Extract Soil** - Runs an algorithm over a raster acquisition to identify areas with bare soil exposed in the image and generate vectors with information on and to notate where the bare areas are. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Soils.jpg).
___
**Extract Soil Change** - Runs Extract Soil algorithm over multiple time series raster acquisitions and then compares the resulting vector outputs, displaying the difference.
___
**Extract Urban Change** - Runs an algorithm over a set of raster acquisitions for change detection, to identify changes between the images and generate vectors with information on and to notate where the changes are. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/ChangeDetection.JPG). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/mga2l31emk).
___
**Extract Urban Change Over Time** - Runs an algorithm over several sets of raster acquisitions for change detection, to identify changes between grouped images (eg, comparing images A/B, B/C, C/D) and generate vectors with information on and to notate where the changes are. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/ChangeDetection.JPG). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/mga2l31emk).
___
**Extract Vegetation** - Runs an algorithm over a raster acquisition to identify areas with vegetation in the image and generate vectors with information on and to notate where the vegetation is. "Vegetation" in this case is defined as any type of flora with healthy chlorophyll content. Note that discovering vegetation is not synonymous with extracting individual plants; an entire forest may generate a single vector as vegetation. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Vegetation.jpg). To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/p88g3k6yre).
___
**Extract Vegetation Change** - Runs Extract Vegetation algorithm over multiple time series raster acquisitions and then compares the resulting vector outputs, displaying the difference. To view a demo of the answer, [click here](https://digitalglobe.wistia.com/medias/p88g3k6yre).
___
**Extract Water** - Runs an algorithm over a raster acquisition to identify areas with water in the image and generate vectors with information on and to notate where the water is. To view a slide describing the recipe for the answer, [click here](../images/Answer%20Definitions/Water.jpg).
___
**Extract Water Change** - Runs Extract Water algorithm over multiple time series raster acquisitions and then compares the resulting vector outputs, displaying the difference.

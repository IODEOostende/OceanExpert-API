
# OceanExpert PPC API Docs

This is the documentation for the OceanExpert PPC API.

[Search](#search) 
[Experts](#expert)    
[Institutions](#institution)    
[Events](#event)    
[Documents](#document)    
[Groups](#groups-of-people)    
[Reports](#reports)   
[OceanExpert Login](#login-api)




## Search

### Basic Search

API to get the basic search results

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/advanceSearch/search.json  | List Group members  | query (Query String)<br />action(browse)<br/>type(all,experts,institutions,events)<br />limit<br/>page  | [https://www.oceanexpert.net/api/v1/advanceSearch/search.json?action=browse&type=experts&query=peter+pissierssens](https://www.oceanexpert.net/api/v1/advanceSearch/search.json?action=browse&type=experts&query=peter+pissierssens)

### Advanced Search

API to get the advanced search results

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/advanceSearch/search.json  | List Group members  | keywords<br />action<br/>type\[\]<br />filter<br />toggle<br />limit<br/>page  | [https://www.oceanexpert.net/api/v1/advanceSearch/search.json?type[]=experts&filter[]=Name+contains&keywords[]=peter&toggle[]=AND&type[]=experts&filter[]=Email+contains&keywords[]=peter&action=advSearch](https://www.oceanexpert.net/api/v1/advanceSearch/search.json?type[]=experts&filter[]=Name+contains&keywords[]=peter&toggle[]=AND&type[]=experts&filter[]=Email+contains&keywords[]=peter&action=advSearch)

#####Parameters:
keywords => any keywords in search

action = advance (for advance search)

type[] => may contain multiple type (experts, institutions, events)

filter[] => filter related to search types. Following filters can be applied for each types.

Expert| Institutions | Events
------|--------------|-------
First name contains | Current address contains | Title contains |
Last name contains | Current/Previous addresses contain | eType is |
Current address contains | Country is | Summary contains |
Current/Previous addresses contain | Sea regions of study is | Keywords contain |
Phone/Fax contains | Type is | Address contains |
Email contains | Activities contains | Country is |
Website URL contains | Tel/Fax contains | Date between |
Country is | Website URL contains | Updated |
Sea regions of study is | EDMO Code is | Created |
Member of group or sub-group | Updated | |
Job type is | Created | |
Job title contains | | |
Department contains | | |
Institution name contains | | |
Subject Area is | | |
Activites include | | |
Working languages includes | | |
Degree contains | | |
Is retired | | |
Is deceased | | |
Is quality checked | | |
Quality last checked | | |
Updated | | |
Created | | | 

toggle[] => conditions for each type and filters

limit => result limit

page => pagination page numbers.


## Expert

### Expert Details

API to get the details of expert

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/institution/{idExpert}.json  | List Group members  | limit<br/>offset  | [https://www.oceanexpert.net/api/v1/expert/27036.json](https://www.oceanexpert.net/api/v1/expert/27036.json)



## Institution

API to display institution details and associated members.

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/institution/{idInstitution}.json  | List Group members  | limit<br/>offset<br />orderby  | [https://www.oceanexpert.net/api/v1/institution/6860.json](https://www.oceanexpert.net/api/v1/institution/6860.json)



## Event

#### Calendar Events:
This API displays all the events for the group. (for eg. IOC is having group id 31) 

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
api/v1/getEventCalendar/{idGroup}.json  | List all the events in the Website Groups  | start<br/> end  | [https://www.oceanexpert.net/api/v1/getEventCalendar/31.json?start=2018-03-01&end=2018-06-30](https://www.oceanexpert.net/api/v1/getEventCalendar/31.json?start=2018-03-01&end=2018-06-30) 

#### Upcoming Events:
This Api list the upcoming event for the group.

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
api/v1/getUpcomingEvents/{idGroup}.json  | List all the Upcoming event in the Website Groups  | limit  | [https://www.oceanexpert.net/api/v1/getUpcomingEvents/31.json](https://www.oceanexpert.net/api/v1/getUpcomingEvents/31.json)


#### Event Record:
API to get the event data
	
Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/event/viewEventRecord/{idEvent}.json  | List event overview  | -  | [https://www.oceanexpert.net/api/v1/event/viewEventRecord/1879.json](https://www.oceanexpert.net/api/v1/event/viewEventRecord/1879.json)

#### Event Agenda:

API to list Event Agenda items

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/event/viewEventAgenda/{idEvent}.json  | List event Agenda items  | -  | [https://www.oceanexpert.net/api/v1/event/viewEventAgenda/1879.json](https://www.oceanexpert.net/api/v1/event/viewEventAgenda/1879.json)

#### Event Documents
API to list all the event documents including agenda documents

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/event/viewEventDocs/{idEvent}.json  | List event Documents  | -  | [https://www.oceanexpert.net/api/v1/event/viewEventDocs/1879.json](https://www.oceanexpert.net/api/v1/event/viewEventDocs/1879.json)

#### Event Participants
API to list all the participants in the event

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/event/viewEventParticipants/{idEvent}.json  | List event participants | -  | [https://www.oceanexpert.net/api/v1/event/viewEventParticipants/1879.json](https://www.oceanexpert.net/api/v1/event/viewEventParticipants/1879.json)

## Documents
#### Document details by ID
API to get document details by ID

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/document/viewDocumentRecord/{idDocument}.json  | List document details | -  | [https://www.oceanexpert.net/api/v1/document/viewDocumentRecord/19058.json](https://www.oceanexpert.net/api/v1/document/viewDocumentRecord/19058.json)

#### Document download links
API to get document download links

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/document/viewDocFilesPopup/{idDocument}.json  | List document details | -  | [https://www.oceanexpert.net/api/v1/document/viewDocFilesPopup/19058.json](https://www.oceanexpert.net/api/v1/document/viewDocFilesPopup/19058.json)

#### view all document lists
API to get all document list in group

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/document/doclists/{idGroup}.json  | view all document List in group | -  | [https://www.oceanexpert.net/api/v1/document/doclists/31.json](https://www.oceanexpert.net/api/v1/document/doclists/31.json)

#### view document list details
API to get document list details

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/document/viewDoclistRecord/{idDoclist}.json  | view document List details | -  | [https://www.oceanexpert.net/api/v1/document/viewDoclistRecord/90.json](https://www.oceanexpert.net/api/v1/document/viewDoclistRecord/90.json)


## Groups of People

#### Group tree
API to list the groups in tree view

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/grouptree/{idGroup}.json  | List group tress  | -  | [https://www.oceanexpert.net/api/v1/grouptree/31.json](https://www.oceanexpert.net/api/v1/grouptree/31.json)

#### Group members
API to list the groups members.

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/group/{idGroup}.json  | List Group members  | limit<br/>offset<br />orderby  | [https://www.oceanexpert.net/api/v1/group/31.json](https://www.oceanexpert.net/api/v1/group/31.json)


## Country reports

### Country List

API to get all the countries

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/getCountryList/list.json  | List all countries  | -  | [https://www.oceanexpert.net/api/v1/getCountryList/list.json](https://www.oceanexpert.net/api/v1/getCountryList/list.json)

API to list all the coutry participation reports

#### Country Reports
Subsidiary body membership (type = 1)  
Official meeting participants (type = 2)  
Training course participants (type = 3)  
Grants (type = 4)
Expert assistance (type = 5)  
Assistance provided (type = 6)  
Assistance received (type = 7)

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/countryReports/{idGroup}.json?reportType={type}  | Subsidiary body membership reports  | reportType year   | [https://www.oceanexpert.net/api/v1/countryReports/31.json?reportType=3&year=2017 ](https://www.oceanexpert.net/api/v1/countryReports/31.json?reportType=3&year=2017)


## Login API
#### OceanExpert Login (Post method only)

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/login_check  | Login API  | username<br />password   | [https://www.oceanexpert.net/api/login_check](https://www.oceanexpert.net/api/login_check)  
<span style="color:red"><u>Note:</u> Login API requests MUST include a valid [User-Agent header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent). Requests with no User-Agent header will be rejected and throws error as <code>406 Not Acceptable</code>.</span>


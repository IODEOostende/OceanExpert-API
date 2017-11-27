# OceanExpert-AP# OceanExpert PPC API Docs    


This is the documentation for the OceanExpert PPC API.

[Experts](#expert)    
[Institutions](#institution)    
[Events](#event)    
[Documents](#document)    
[Groups](#groups-of-people)    
[Reports](#reports)    


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
This API displays all the events for the group. (for eg. IOC is having group id 32) 

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
api/v1/getEventCalendar/{idGroup}.json  | List all the events in the Website Groups  | start<br/> end  | [https://www.oceanexpert.net/api/v1/getEventCalendar/32.json?start=2018-03-01&end=2018-06-30](https://www.oceanexpert.net/api/v1/getEventCalendar/32.json?start=2018-03-01&end=2018-06-30) 

#### Upcoming Events:
This Api list the upcoming event for the group.

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
api/v1/getUpcomingEvents/{idGroup}.json  | List all the Upcoming event in the Website Groups  | limit  | [https://www.oceanexpert.net/api/v1/getUpcomingEvents/32.json](https://www.oceanexpert.net/api/v1/getUpcomingEvents/32.json)


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
/api/v1Ostend/event/viewEventParticipants/{idEvent}.json  | List event participants | -  | [https://www.oceanexpert.net/api/v1/event/viewEventParticipants/1879.json](https://www.oceanexpert.net/api/v1/event/viewEventParticipants/1879.json)


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

API to list all the coutry participation reports

#### Country List

List all countries in the system

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/countries/list.json  | List all countries in OceanExpert  | country  | [https://www.oceanexpert.net/api/v1/countries/list.json ](https://www.oceanexpert.net/api/v1/countries/list.json)

#### by Country

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/countryReports/bycountry/{idGroup}.json?country={idCountry}  | List reports by country  | country  | [https://www.oceanexpert.net/api/v1/countryReports/bycountry/31.json?country=74 ](https://www.oceanexpert.net/api/v1/countryReports/bycountry/31.json?country=74)

#### Subsidiary body membership (type = 1)

#### Official meeting participants (type = 1)

#### Training course participants (type = 1)

#### Grants (type = 1)

Url  | Description | Parameters | Examples 
------------- | ------------- | ------------ | ----------
/api/v1/countryReports/{idGroup}.json?reportType={type}  | Subsidiary body membership reports  | -  | [https://www.oceanexpert.net/api/v1/countryReports/{idGroup}.json?reportType={type} ](https://www.oceanexpert.net/api/v1/countryReports/{idGroup}.json?reportType={type})

I

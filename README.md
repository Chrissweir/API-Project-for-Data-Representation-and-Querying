# Dublin Wheel Chair Access Guide

## Data Representation and Querying Project 2015

### Christopher Weir - G00309429

## Introduction
This project provides the design and documentation for the dataset "Dublin Wheel Chair Access Guide
" which is available at https://data.gov.ie/dataset/dublin-wheel-chair-access-guide

The data is only based on information from Dublin City Council. I would suggest to data.gov.ie to upload other datasets of all major cities and towns throughout Ireland and to particularly include other datasets of all countrywide public building wheelchair access points.

I would imagine that the type of people to use this app would be those who are either confined to a wheelchair or look after someone in a wheelchair.

### About the data

This dataset was received in Comma Separated Values (CSV) format, and was downloaded from https://data.gov.ie/dataset/dublin-wheel-chair-access-guide.
The CSV file contains 814 rows, the first being a header row with the names of each field.
There are six values on each line, which are as follows:

Field | Description
------|------------
**Venue** | The name of the venue 
**Address1** | The first part of the venue address
**Address2** | The second part of the venue address
**Address3** | The third part of the venue address
**Phone** | The phone number of the venue
**Web** | The website of the venue

##Design

The app should be simple and very user friendly, I think two windows will be sufficient to fullfill the requirements of the app.

###Main Menu

The app should open onto the main menu page with two options. Here is a link to a template I have designed: https://github.com/Chrissweir/ApiProject/blob/master/Main%20Menu.png

> ####Venue

This section would contain a drop down list of all the venues in the dataset sorted into alphabetical order. The user could select any of these venues to find out the wheelchair access information for that particular venue. In the template that I designed I aim to show the simple layout with just the one dropdown menu available. Here is a link to the template I have designed: https://github.com/Chrissweir/ApiProject/blob/master/Venue%20Menu.png

> ####Map

This section would be a map that using gps, could find the users current location and inform them of wheelchair accessible ares in the current vicinity and show those locations on the map along with directions. Here is a link to a template I have designed: https://github.com/Chrissweir/ApiProject/blob/master/Map%20Menu.png

##HTTP Requests and GET METHOD

#####List of access points on a given street
This will give you a list of access points on a particular street, including the name of the venue and its full address.
```markdown
*http://dublinwheelchairaccessguide.ie/street/[street]*
where you replace [street] with the street name.
For example, the URL:
*http://dublinwheelchairaccessguide.ie/street/Clarian Quay*
will return a list of access points on this particular street.
```
**JSON Example**
```json
{
        "Venue": "Clarion Hotel IFSC",
        "Address 1": "IFSC",
        "Address 2": "Clarion Quay",
        "Address 3": "Dublin 1",
        "Phone": "01 4338800",
        "Web": "www.clarionhotelifsc.com"
  { ... },
  { ... }
}```

#####List of access points at a given venue
This will give you a list of access points at a given Venue, including the location of these access points and the name of the venue and its full address.
```markdown
*http://dublinwheelchairaccessguide.ie/venue/[venue]*
where you replace [venue] with the venue name.
For example, the URL:
*http://dublinwheelchairaccessguide.ie/venue/ArlingtonHotel*
will return a list of access points at this particular venue.
```

#####Number of access points at a given venue
This will give you the number of access points at a particular venue, including the name of the venue and its full address.
```markdown
*http://dublinwheelchairaccessguide.ie/venue/[venue]number*
where you replace [venue] with the venue name.
For example, the URL:
*http://dublinwheelchairaccessguide.ie/venue/ArlingtonHotel-Number*
will return the number of access points at this particular venue.
```

###**If the dataset was modified to include other towns and cities then these urls could be used!**###

#####Location of access points in a given city
This will give you the location of access points in a given city, including the name of the venue and its full address.
```markdown
*http://dublinwheelchairaccessguide.ie/[city]*
where you replace [city] with the city name.
For example, the URL:
*http://dublinwheelchairaccessguide.ie/Galway*
will return the location of access points in this particular city.
```

#####Location of access points in a given town
This will give you the location of access points in a given town, including the name of the venue and its full address.
```markdown
*http://dublinwheelchairaccessguide.ie/[town]*
where you replace [town] with the town name.
For example, the URL:
*http://dublinwheelchairaccessguide.ie/Ballina*
will return the location of access points in this particular town.
```


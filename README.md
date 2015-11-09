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
There are seven values on each line, which are as follows:

> * **id**: The id of the row // primary key?
> * **Venue**: The name of the venue // primary key?
> * **Address1**: The first part of the venue address
> * **Address2**: The second part of the venue address
> * **Address3**: The third part of the venue address
> * **Phone**: The phone number of the venue
> * **Web**: The website of the venue

##Design##

The app should be simple and very user friendly, I think two windows will be sufficient to fullfill the requirements of the app.

###Main Menu###

The app should open onto the main menu page with two options. Here is a link to a template I have designed: https://github.com/Chrissweir/ApiProject/blob/master/Main%20Menu.png

> ####Venue####

This section would contain a drop down list of all the venues in the dataset sorted into alphabetical order. The user could select any of these venues to find out the wheelchair access information for that particular venue.

> ####Map####

This section would be a map that using gps, could find the users current location and inform them of wheelchair accessible ares in the current vicinity and show those locations on the map along with directions.




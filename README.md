# rmls-search-app-python
Project to browse MLS homes. Users are allowed to browse homes, Admins are allowed to CRUD homes. 


## Purpose
Create a basic realtor web site that will allow a secured User to Add, Edit and Delete a
House.

## Architecture

Project will be based on a modern Django platform: https://www.djangoproject.com/

Data System:
SQLLite 

Auth:
https://docs.djangoproject.com/en/2.2/topics/auth/

Overview:
* Authorized Users will be able to create Houses via the /admin/createHouse endpoint and UX. 
* Authorized == (ListingAgent, Admin)
* All home data is public and contains no sensitive information
* App endpoints, '/' will present all users with a UX allowing for the search of Houses. 
* Searching will be implemeted in accordance with the business logic section.

## Data Model

**House**
* MLS # (Unique number) - string()
* Street1 - string()
* Street2 - string()
* City - string()
* State - string()
* Zipcode - string()
* Neighborhood - string()
* SalesPrice - float()
* DateListed - datetime()
* Bedrooms - int()
* Photos - string()
* Bathrooms - int()
* Garage Size - int()
* Square Feet - int()
* LotSize - int()
* Description - string()

**User**
* UserID # (Unique number) - id()
* RoleID - int([1=Guest,2=ListingAgent,3=Admin)
* Name - string()

# Business Logic
Public search page MUST find houses based on these fields:
* MLS#
* City
* State
* Zipcode
* Bedrooms
* Bathrooms
* SquareFeet


# Time Estimations
* Creating App Framework - 1hr
* Creating Data Models Migrations - 30 minutes
* Creating Public View - 1 hr
* Creating Admin Crud - 1 hr
* BONUS - Create DataSeeders and Unit Test - 2 hrs
* 
* Total: 5.5 hrs 
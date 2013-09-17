synchronize-webservice
======================

The synchronize webservice is a simple REST-api and return JSON results.

Resources
---------

|Resource    | Methods    | Description        |
|------------|------------|--------------------|
|Categories  | POST       | Get all categories |
|Files       | POST       | Get all files      |

All calls to the API must contain a `username` and `password` for the requesting user in the POST body.

JSON Results
------------

### Categories
An array of json objects: 

**{**  
&emsp;&emsp; "id": *unique ID*  
&emsp;&emsp; "name": *category name*  
&emsp;&emsp; "image": *category image*  
&emsp;&emsp; "parentId": *parent category, or 0 for root*  
**}**

### Files
An array of json objects:

**{**  
&emsp;&emsp; "id": *unique ID*  
&emsp;&emsp; "name": *name to show*  
&emsp;&emsp; "file": *URL to download the file*  
&emsp;&emsp; "version": *file version*  
&emsp;&emsp; "author": *author of file*  
&emsp;&emsp; "category": *category ID*  
&emsp;&emsp; "description": *file description*  
&emsp;&emsp; "tags": *array of tags*  
&emsp;&emsp; "language": *file language*
&emsp;&emsp; "preview": *URL to preview*  
&emsp;&emsp; "icon": *URL to icon*  
&emsp;&emsp; "image": *URL to image*  
**}**

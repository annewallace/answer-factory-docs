# AnswerFactory Project API

AnswerFactory supports managing projects via REST API.  Projects can be created, retrieved, updated, and deleted.  In addition, projects for a user's account/group can be retrieved as a list.

# Table of Contents

* [Project JSON](#project-json)
  * [Project Metadata](#project-metadata)
  * [Original Base Geometries](#original-base-geometries)
  * [Buffered AOI geometries](#buffered-aoi-geometries)
  * [Answer Configurations](#answer-configurations)
  * [Example Project JSON](#example-project-json)
* [Project REST API](#project-rest-api)
  * [Error responses](#error-responses)
  * [Create a project](#create-a-project)
  * [Delete a project](#delete-a-project)
  * [Update a project](#update-a-project)
  * [Retrieve a project](#retrieve-a-project)
  * [Retrieve a listing of projects for the current user's account](#retrieve-a-listing-of-projects-for-the-current-users-account)
  * [Check availability of project endpoints](#check-availability-of-project-endpoints)


## Project JSON

An AnswerFactory project consists of four main parts:

* project metadata
* a set of geometries defining the original base geometries for a project
* a set of geometries defining a buffered area of interest (AOI) around those geometries
* a set of configurations for building "answers" for the project

### Project metadata

Project metadata includes the following fields:

* id (String)
* name (String)
* owner (String)
* accountId (String)
* createDate (DateTime)
* updateDate (DateTime)

### Original Base Geometries

The initial geometries for a project are represented as GeoJSON in a field named 'originalGeometries'.  Any valid GeoJSON geometries are supported.

### Buffered AOI geometries

The buffered AOI geometries for a project are represented in two fields:

* 'aois': a list of GeoJSON objects based on a buffer distance around the original geometries used to compute various spatial relationships for the project
* 'namedBuffers': a list of JSON objects which assign a human-readable name to individual geometries within the buffered geometry collection, used for things like meaningful table-based displays for answers.  A named buffer consists of a String name and a GeoJSON geometry.

### Answer configurations

Projects are used mainly for discovering different kinds of information and relationships among different kinds of data.  AnswerFactory allows users to configure "recipes" for discovering those answers.  These configurations are listed in a field named 'recipeConfigs'.  A recipe configuration consists of the following fields:

* recipeId: the ID of the recipe to run
* recipeName: the human-readable name of the recipe for display purposes
* configurationDate: the DateTime when the recipe was configured for the project
* startDate: the earliest time for which data will be returned
* endDate: the latest time for which data will be returned
* parameters: a list of recipe config parameters, each consisting of a name, a value, and a type, which correspond to the recipe being configured (see the recipe API documentation for more detail)

### Example Project JSON
```
{
  "id" : "uuid",
  "owner" : "user@mycompany.com",
  "name" : "rio-inet-cafes",
  "accountId" : "uuid",
  "recipeConfigs" : [ {
    "recipeId" : "generate-random-vectors",
    "recipeName" : "Generate Random Vectors",
    "configurationDate" : "2016-06-24T11:43:23.080Z",
    "startDate" : null,
    "endDate" : null,
    "parameters" : [ {
      "name" : "num_vectors",
      "value" : "500",
      "type" : "string"
    } 
  }
  ],
  "originalGeometries" : [ {
    "type" : "FeatureCollection",
    "features" : [ {
      "type" : "Feature",
      "properties" : {
        "item_fea_1" : "6da9618b26cc48ad53b0985614a49635",
        "item_NAME_" : "SR Café"
      },
      "geometry" : {
        "type" : "Point",
        "coordinates" : [ -43.17770923, -22.906254234 ]
      }
    }, {
      "type" : "Feature",
      "properties" : {
        "item_fea_1" : "6da9618b26cc48ad53b0985614a49635",
        "item_NAME_" : "Saraiva Megastore"
      },
      "geometry" : {
        "type" : "Point",
        "coordinates" : [ -43.176339265, -22.956997275 ]
      }
    }, {
      "type" : "Feature",
      "properties" : {
        "item_fea_1" : "6da9618b26cc48ad53b0985614a49635",
        "item_NAME_" : "Lan House Free Jack",
      },
      "geometry" : {
        "type" : "Point",
        "coordinates" : [ -43.175016051, -22.964182431 ]
      }
    }
  ] } 
  ],
  "aois" : [ {
    "type" : "MultiPolygon",
    "coordinates" : [ . . . elided . . . ]
   } 
  ],
  "namedBuffers" : [ {
    "name" : "SR Café",
    "buffer" : {
      "type" : "Polygon",
      "coordinates" : [ . . . elided . . . ]
    }
  }, {
    "name" : "Saraiva Megastore",
    "buffer" : {
      "type" : "Polygon",
      "coordinates" : [ . . . elided . . . ]
    }
  }, {
    "name" : "Lan House Free Jack",
    "buffer" : {
      "type" : "Polygon",
      "coordinates" : [ . . . elided . . . ]
    }
  }
  ],
  "createDate" : "2016-04-28T16:05:46.610Z",
  "updateDate" : "2016-04-28T16:05:46.610Z"
}
```

## Project REST API

### Error responses

For all requests, if an error occurs, the response body will consist of JSON formatted like this:
```
{ "error" : "message" }
```
The HTTP response code will depend on the error.



### Create a project

Request:
```
POST /answer-factory-project/api/project

Headers:
   Content-Type: application/json

Body:
   {
    ... project definition (see above) ...
   }
```

Response (success):
```
202 Accepted
```

### Delete a project

Request:
```
DELETE /answer-factory-project/api/project/{projectId}

Headers:
    None

Params:
    projectId: the ID of the project to delete
```

Response (success):
```
200 OK
```

### Update a project

Request:
```
PUT /answer-factory-project/api/project/{projectId}

Headers:
  Content-Type: application/json

Params:
  projectId: the ID of the project to update

Body:
  { ... project JSON (see above) ... }
```

Response (success):
```
202 Accepted
```

### Retrieve a project

Request:
```
GET /answer-factory-project/api/project/{projectId}

Headers:
  Accept: application/json

Params:
  projectId: the ID of the project to retrieve
```

Response (success):
```
200 OK

Body:
{ ... Project JSON (see above) ... }
```

### Retrieve a listing of projects for the current user's account

Request:
```
GET /answer-factory-project/api/project

Headers:
  Accept: application/json
```

Response (success):
```
200 OK

Body:
[ 
  { ... project JSON ... },
  { ... project JSON ... },
  { ... project JSON ... },
  ...
]
```

### Check availability of project endpoints

Request:
```
GET /answer-factory-project/api/project/heartbeat
```

Response:
```
200 OK
```

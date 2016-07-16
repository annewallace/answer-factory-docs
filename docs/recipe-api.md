# AnswerFactory Recipe API

AnswerFactory supports managing recipes via REST API.  Recipes can be created, updated, and retrieved, and updated.

# Table of Contents

* [Recipe JSON](#recipe-json)
  * [Recipe metadata](#recipe-metadata)
  * [Recipe type metadata](#recipe-type-metadata)
  * [Recipe parameters](#recipe-parameters)
  * [Recipe properties](#recipe-properties)
  * [Example Recipe JSON](#example-recipe-json)
* [Recipe REST API](#recipe-rest-api)
  * [Error responses](#error-responses)
  * [Create a recipe](#create-a-recipe)
  * [Update a recipe](#update-a-recipe)
  * [Retrieve a recipe](#retrieve-a-recipe)


## Recipe JSON

An AnswerFactory recipe consists of four main parts:

* recipe metadata
* recipe type metadata
* a set of parameters that will ultimately be configurable by an AnswerFactory user
* a set of properties specific to the recipe that are not part of the general metadata

### Recipe metadata

Recipe metadata includes the following fields:

* **_id_** (String)
* **_name_** (String)
* **_description_** (String)
* **_owner_** (String)
* **_accountId_** (String)
* **_createDate_** (DateTime)
* **_updateDate_** (DateTime)

### Recipe type metadata

Recipe type metadata defines the input, output, system, and definition for the recipe:

* **_inputType_**: name of the input to the recipe
* **_outputType_**: name of the output to the recipe; determines how the result of the recipe will be displayed 
* **_recipeType_**: name of the system utilized to execute the recipe
* **_definition_**: string or JSON object that describes how the specified system should execute the recipe

### Recipe parameters

Recipe parameters are typed key-value pairs, where the values are determined by users of AnswerFactory applications when the recipe is added to their recipe. Each paramter contains the following fields:

* **_name_** (String)
* **_description_** (Stirng)
* **_type_** (String)
* **_required_** (Boolean)
* **_allowedValues_**: optional list of enumerated values that an AnswerFactory user must selected from

### Recipe properties

Recipe properties are key-value pairs that determine specific details about how the execution of this recipe should differ from others of the same type. 

### Example Recipe JSON
```json
{
  "id": "extract-urban-change-series",
  "name": "Extract Urban Change Over Time",
  "description": "Extracts urban change vectors from the intersection of two acquisitions and write to GBDX Vector Service.",
  "definition": " ... ",
  "recipeType": "workflow",
  "inputType": "acquisitions",
  "outputType": "vector-service",
  "validators": [],
  "parameters": [
    {
      "allowedValues": [
        "1 month ago",
        "1 year ago"
      ],
      "name": "start_date",
      "description": "Start Date",
      "type": "string",
      "required": "true"
    }
  ],
  "properties": {
    "image_bands": "Pan_MS1, Pan_MS1_MS2",
    "num_acquisitions": "2"
  }
}
```

## Recipe REST API

### Error responses

For all requests, if an error occurs, the response body will consist of JSON formatted like this:
```json
{ "error" : "message" }
```
The HTTP response code will depend on the error.



### Create a recipe

For this version of the recipe creation API call, the recipe definition parameter (see the recipe type metadata section above) must be a string
which the specified recipe type can understand.  The next API endpoint supports using a JSON object for the recipe definition.

Request:
```
POST /answer-factory-recipe-service/api/recipe

Headers:
   Content-Type: application/json

Body:
  { ... recipe JSON (see above) ... }
```

Response (success):
```
202 Accepted
```

### Create a recipe with JSON object for recipe definition

For this version of the recipe creation API call, the recipe definition parameter (see the recipe type metadata section above) must be a JSON object
which the specified recipe type can understand.  The previous API endpoint supports using a string for the recipe definition.

Request:
```
POST /answer-factory-recipe-service/api/recipe/json

Headers:
   Content-Type: application/json

Example Body:
  {
    "id": "skynet-counts-test-1",
    "name": "Test Query & Summarize Object Detection (One Year)",
    "description": "Aggregates the skynet item_types by item_date and doc_count.",
    "definition": {
        "index": "vector-skynet-*",
        "beginTime": "now-1y",
        "endTime": "now",
        "interval": "month",
        "queryType": "agg-by-type-and-time"
    },
    "recipeType": "es-query",
    "inputType": "none",
    "outputType": "es-query-service"
  }
```

Response (success):
```
202 Accepted
```

### Update a recipe

For this version of the recipe update API call, the recipe definition parameter (see the recipe type metadata section above) must be a string
which the specified recipe type can understand.  The next API endpoint supports using a JSON object for the recipe definition.

Request:
```
PUT /answer-factory-recipe-service/api/recipe/{recipeId}

Headers:
  Content-Type: application/json

Params:
  recipeId: the ID of the recipe to update

Body:
  { ... recipe JSON (see above) ... }
```

Response (success):
```
202 Accepted
```

### Update a recipe with JSON object for recipe definition

For this version of the recipe update API call, the recipe definition parameter (see the recipe type metadata section above) must be a JSON object
which the specified recipe type can understand.  The previous API endpoint supports using a string for the recipe definition.

Request:
```
PUT /answer-factory-recipe-service/api/recipe/json/{recipeId}

Headers:
  Content-Type: application/json

Params:
  recipeId: the ID of the recipe to update

Example Body:
  {
    "id": "skynet-counts-test-1",
    "name": "Test Query & Summarize Object Detection (One Year)",
    "description": "Aggregates the skynet item_types by item_date and doc_count.",
    "definition": {
        "index": "vector-skynet-*",
        "beginTime": "now-1y",
        "endTime": "now",
        "interval": "month",
        "queryType": "agg-by-type-and-time"
    },
    "recipeType": "es-query",
    "inputType": "none",
    "outputType": "es-query-service"
  }
```

Response (success):
```
202 Accepted
```

### Retrieve a recipe

Request:
```
GET /answer-factory-recipe-service/api/recipe/{recipeId}

Headers:
  Accept: application/json

Params:
  recipeId: the ID of the recipe to retrieve
```

Response (success):
```
200 OK

Body:
{ ... recipe JSON (see above) ... }
```

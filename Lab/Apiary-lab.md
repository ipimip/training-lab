# Apiary Hands-On Lab

You will have been assigned a particular service to work on for the following exercises, throughout this document it will be referred to as `your service`.

The following exercises are designed to provide a basic understanding of how Apiary and the API Design-First process work here at IPIM-IP.

If you encounter any issues during the following exercises please ask one of the on-site support team for help.

## Table of Contents

- [Apiary Hands-On Lab](#Apiary-Hands-On-Lab)
  - [Table of Contents](#Table-of-Contents)
  - [Setup](#Setup)
    - [Required Tools](#Required-Tools)
    - [Useful URLs](#Useful-URLs)
  - [Section 1 - Introduction to Apiary](#Section-1---Introduction-to-Apiary)
    - [Documentation Tab](#Documentation-Tab)
      - [Trying a Resource](#Trying-a-Resource)
    - [Exercise 1: Mock Server](#Exercise-1-Mock-Server)
      - [Exercise 1 - Required Tools](#Exercise-1---Required-Tools)
      - [Exercise 1 - Task](#Exercise-1---Task)
      - [Exercise 1 - Success Criteria](#Exercise-1---Success-Criteria)
  - [Section 2 - The Editor Tab](#Section-2---The-Editor-Tab)
    - [Document Format and Host](#Document-Format-and-Host)
    - [Document Information](#Document-Information)
    - [Logical Groups](#Logical-Groups)
    - [Specific Requests](#Specific-Requests)
      - [Specific Request Parameters](#Specific-Request-Parameters)
        - [Query Parameters](#Query-Parameters)
        - [Path Parameters](#Path-Parameters)
        - [Parameters](#Parameters)
    - [Exercise 2: Adding New Parameters](#Exercise-2-Adding-New-Parameters)
      - [Exercise 2 - Required Tools](#Exercise-2---Required-Tools)
      - [Exercise 2 - Task](#Exercise-2---Task)
      - [Exercise 2 - Success Criteria](#Exercise-2---Success-Criteria)
  - [Section 3 - Data Structures](#Section-3---Data-Structures)
    - [Simple Objects](#Simple-Objects)
    - [Complex Objects](#Complex-Objects)
    - [Exercise 3: Adding a Data Structure](#Exercise-3-Adding-a-Data-Structure)
      - [Exercise 3 - Required Tools](#Exercise-3---Required-Tools)
      - [Exercise 3 - Task](#Exercise-3---Task)
      - [Exercise 3 - Success Criteria](#Exercise-3---Success-Criteria)
  - [Section 4 - Request and Response Bodies](#Section-4---Request-and-Response-Bodies)
    - [Specific Request Bodies](#Specific-Request-Bodies)
    - [Specific Response Bodies](#Specific-Response-Bodies)
    - [Exercise 4.1: Modifying Request & Response Bodies](#Exercise-41-Modifying-Request--Response-Bodies)
      - [Exercise 4.1 - Required Tools](#Exercise-41---Required-Tools)
      - [Exercise 4.1 - Task](#Exercise-41---Task)
      - [Exercise 4.1 - Success Criteria](#Exercise-41---Success-Criteria)
    - [Exercise 4.2: Adding Request and Response Bodies](#Exercise-42-Adding-Request-and-Response-Bodies)
      - [Exercise 4.2 - Required Tools](#Exercise-42---Required-Tools)
      - [Exercise 4.2 - Task](#Exercise-42---Task)
      - [Exercise 4.2 - Success Criteria](#Exercise-42---Success-Criteria)
  - [Section 5 - Tying Everything Together](#Section-5---Tying-Everything-Together)
    - [Exercise 5: Adding New Endpoints](#Exercise-5-Adding-New-Endpoints)
      - [Exercise 5 - Required Tools](#Exercise-5---Required-Tools)
      - [Exercise 5 - Task](#Exercise-5---Task)
      - [Exercise 5 - Success Criteria](#Exercise-5---Success-Criteria)

## Setup

After logging in to your provided virtual machine you should see your service downloaded to the machine along with suitable development tools such as Postman, Visual Studio Code, Notepad++ etc.

### Required Tools

For the following exercises, the following tools are required:

- Internet Browser (Google Chrome)

### Useful URLs

- [Apiary Lab (This Document)](https://git.build.ingka.ikea.com/IPIM-IP/training-lab/blob/master/Lab/Apiary-lab.md)
- [Apiary](https://apiary.io/)
- [Apiary Documentation](https://help.apiary.io/)
- [Microservices workbench](https://confluence.build.ingka.ikea.com/display/II/%28Micro%29services+Knowledge+Base)

> _Note: Please **only use the below link for your service** as other people will be working on their services._

- [Bedroom Service](https://traininglabbedroomservice.docs.apiary.io/)
- [Kitchen Service](https://traininglabkitchenservice.docs.apiary.io/)
- [Living Room Service](https://traininglablivingroomservice.docs.apiary.io/)
- [Storage Service](https://traininglabstorageservice.docs.apiary.io/)
- [Office Space Service](https://traininglabofficespaceservice.docs.apiary.io/)

## Section 1 - Introduction to Apiary

You should have received an invitation to work on your apiary service, please follow the instructions in that email to create your account if you do not already have one.

The Apiary application has a menu section located at the top of the page, the two key tabs are **Documentation** and **Editor**

> ![alt text][apiary_menu_toolbar]

### Documentation Tab

The documentation tab contains the rendered API Design documentation, this is the document that any potential API Consumer would look at in order to understand how your API works, due to this reason it is extremely important to ensure the documentation is accurate and up-to-date otherwise it can have a negative impact on whether your API is to be consumed in the future.

The document contains a high level introduction followed by one or logical groups, with each logical groups potentially containing multiple API resources.

> ![alt text][apiary_desc_and_group]

#### Trying a Resource

If you want to drill into a particular API resource, you can select one of the named resources in the document and it opens the right hand panel, often referred to as the Example area.

> ![alt text][apiary_example_area]

The example area allows a consumer to see the URI of the request, any applicable parameters (Query or Path) along with example request (if applicable) and response bodies.

> ![alt text][apiary_example_area_populated]

You are able to switch the panel on the right hand side from Example to Console, a key feature of this is the Mock Server setting, this feature allows you to test out the API design as though it was a real API, using your favourite API Client or the Apiary application you can call the end-point and see the example responses you have created be returned. This is one of the key features of the API Design first approach as it allows consumers to call the Mock Server in order to get a response payload that matches what the real service will return, using the Mock Server allows consumers to **not** be dependant on the development of the service as they are able to consume the API as soon as the design is completed.

In order to open the Mock Server you can click _Try_ via the Example screen or _Call Resource_ in the Console screen.

> ![alt text][apiary_console_mock_server]
>
> ![alt text][apiary_example_mock_server]

The remainder of the document in Apiary's documentation tab contains all of the resources your API exposes, as this is the consumer documentation it is important that all of the possible resources are documented.

> ![alt text][apiary_doc_resources]
>
> _Note: The colour of the resource determines the type, Green = GET, Blue = POST, Grey = PUT, RED = DELETE and Brown = PATCH_

### Exercise 1: Mock Server

This exercise is designed to familiarise yourself with the Mock Server aspect of the Apiary application - As further exercises require you to edit the Apiary document for your service, please use the below Apiary document for this exercise:

- [Example Poll API Document](https://ikeapollexample.docs.apiary.io/#)

The various resources in the Apiary document look like the below image:

> ![alt text][apiary_documentation_endpoints_highlighted]

#### Exercise 1 - Required Tools

- Internet Browser

#### Exercise 1 - Task

Within Apiary, on the documentation tab, try all of the available resources that the Polls API has exposed.

Pay attention to the request and response sections for the different HTTP Methods in the document.

> _Tip: Check the `Body` section when making a POST request_

#### Exercise 1 - Success Criteria

- [ ] Try the `List All Questions` resource
- [ ] Try the `Create a New Question` resource
- [ ] Familiar with the Apiary Documentation tab

## Section 2 - The Editor Tab

The editor tab consists of two panels, the left panel contains the raw, un-processed API design document, within Apiary this can either be an API Blueprint or Swagger/OAS document, whilst the right panel is what you would see if you clicked on the documentation tab.

> _Note: For the exercises in this lab we will be using API Blueprint notation as in our experience we have found it easier to work with when you're new to API Design._

### Document Format and Host

On the left panel, the first thing you will see is the FORMAT and HOST properties, the FORMAT should be set to `1A` for API Blueprint whilst the HOST field should be set to the real-life API gateway URL including the API base path, see the example below:

> ![alt text][apiary_editor_format_and_host]

### Document Information

With the Format and Host being set the next item you enter is the API Document title, this uses Markdown syntax which uses `#` characters to decide on the heading size, the largest heading is `#` whereas the smallest heading is `#####`, each API document should contain **one** `#` level heading or **two** `#` level headings if using the [MSON syntax](#data-structures), these are usually the first and last items in the API document.

After the document title you are able to enter a description/overview of the API document if you wish to do so, this isn't mandatory but it usually sets the background picture for any API consumer looking over your documentation.

> ![alt text][apiary_editor_heading_level_1]

### Logical Groups

After the document title and description has been set, you are now free to create logical groups of resources, a logical group of resources is where the URI remains the same for all operations, in the example below, the GET and POST methods are all executed on the same endpoint which therefore makes it logical to group them together.

When defining a logical group, you are also required to enter the URI endpoint that should be called for this group, the endpoint is denoted by being placed inside square brackets `[]`.

> _Note: A logical group can be defined using the `##` notation_
>
> ![alt text][apiary_editor_logical_group_1]

### Specific Requests

Within a logical group, you are able to define specific requests that can be called on the endpoint, for each request defined you must also specify the http method used to invoke the request by placing the method name in square brackets `[]`.

> _Note: One request can be defined using the `###` notation._

After you have specified the name and method type of the request you can choose to enter a description for the specific resource.

> ![alt text][apiary_editor_request_1]

You are required to specify additional information required in order to call the specific resource, the additional information is often but is not limited to:

- Parameters
- Request Bodies
- Response Bodies

#### Specific Request Parameters

Certain URIs require parameters to be included as part of the request url, there are two main types of parameters, Query and Path.
Within Apiary it is possible to include Path and Query parameters in the same request if required.

##### Query Parameters

A `Query Parameter` is included at the end of the URL following a `?` character.

> /resource`?query-parameter-1=ABC&query-parameter-2=DEF`

The above URI contains two query parameters, named `query-parameter-1` and `query-parameter-2`, the values of these query parameters are `ABC` and `DEF` respectively.

> ![alt text][apiary_editor_request_query_parameter]
>
> The notation above shows how you can enter query parameters in the Apiary document, in this particular example the query parameters both contain a `-` character therefore the HTTP representation `%2D` is used to ensure it is rendered correctly on the right hand panel.
>
> ![alt text][apiary_editor_request_query_parameter_example]

##### Path Parameters

A `Path Parameter` can be included at any point in the URI and is often used to provide context.

> /vehicle/`{vehicle-id}`/drivers/`{driver-id}`

The above URI contains two path parameters, named `vehicle-id` and `driver-id`, the values of the path parameters are set when you call the URI, the first parameter is used to retrieve a specific vehicle based on it's vehicle ID from a list of vehicles, the second parameter is used to retrieve a specific driver based on the `driver-id` from a list of drivers that are associated to one specific vehicle (The one identified by `vehicle-id`).

> ![alt text][apiary_editor_request_path_parameter]
>
> The notation above shows how you can enter path parameters in the Apiary document, in this particular example their is only one path parameter `{id}` at the end of the URI although it is possible to include multiple path parameters.
>
> ![alt text][apiary_editor_request_path_parameter_example]

##### Parameters

For both query and path parameters, you have to include a specific parameter section inside the specific request, this can be achieved using the `+ Parameters` notation. Each parameter should be on it's own line and be indented by **four spaces** or **one TAB** character.

> _Note: The names of the parameters should match the ones defined in the URI_
>
> ![alt text][apiary_editor_parameters]
>
> ![alt text][apiary_editor_parameters_example]

### Exercise 2: Adding New Parameters

This exercise will introduce you to editing the Apiary document by adding new query parameters for the `Query` resource, by the end of this exercise you should be familiar with editing the Apiary document and also the parameters section.

> _Note: **Please use your services API Document for this and subsequent exercises - You will also need to switch to the Editor tab**:_

- [Bedroom Service](https://traininglabbedroomservice.docs.apiary.io/)
- [Kitchen Service](https://traininglabkitchenservice.docs.apiary.io/)
- [Living Room Service](https://traininglablivingroomservice.docs.apiary.io/)
- [Storage Service](https://traininglabstorageservice.docs.apiary.io/)
- [Office Space Service](https://traininglabofficespaceservice.docs.apiary.io/)

> _Note: Refer back to the [Specific Request Parameters Section](#specific-request-parameters) for more information on Apiary parameters_

#### Exercise 2 - Required Tools

- Internet Browser

#### Exercise 2 - Task

Currently the `Query` resource allows you to search for a particular furniture item using the `Type` field, your task is to change the `Query` resource so that you are now able to query on the `Type` and `Name` fields.

> _Tip: Remember to add the new parameter in two places_

#### Exercise 2 - Success Criteria

- [ ] Add new query parameter `Name`
- [ ] Try the updated `Query` resource
- [ ] Familiar with the Apiary Editor tab
- [ ] Remove comments related to this exercise



## Section 3 - Data Structures
The following exercises are using the MSON (Markdown Syntax for Object Notation) Syntax.

MSON is a plain-text, human readable way of documenting data structures and therefore is a great choice if you're new to API Design as it compliments your existing business knowledge without becoming too technical.

The data structures are usually placed at the end of the document in order to help a user understand the various schema.

Each object should contain various fields, each field should have a name and type as a minimum although it could contain a default value, sample value and description denoted using the following syntax:

> `- fieldName: fieldDefaultValue/fieldSampleValue (type, [required/optional],  [sample]) - fieldDescription`
>
> e.g. `- furnitureName: A long dark door (string, required) - The name of the furniture item`
>
> _Note: To escape certain field names or values in the document surround the value using the \` character i.e. \`24-10-2019\` escapes the `-` character_

### Simple Objects

The primitive list of types for Apiary are:

- boolean - true/false
- string - Any string
- number - Any number

Each data structure you create can be declared as an object itself by adding `(object)` to the name of the data structure. This is discussed in further detail in the [Complex Objects section](#complex-objects).

> ```markdown
> ## Furniture (object)
>
> - id: 5da429b5308a95c204db6454 (string, optional, sample) - The ID of the furniture item
> - name: KULLABERG (string, required, sample) - The name of the furniture item
> - type: Desk (string, required, sample) - The type of the furniture item
> - price: 1500.00 (number, required, sample) - The price of the furniture item
> ```

The above example shows a data structure called Furniture being created, this new structure contains four fields and each of the fields contains the relevant associated information.

> _Note: If the API defaults a value if none is provided for a specific field then **do not** include the `sample` type on the field and the value after the field name will be used as the default value as opposed to a sample value_

### Complex Objects

Often the data structures that should be returned from an API are complex and could contain special fields like an array, Apiary currently supports the following structure types:

- array - List of items
- enum - Exclusive list of possible values
- object - A structure containing fields/members

For example, using the Furniture object above, it could be extended to include an Array type for one of it's fields.

> ```markdown
> ## Furniture (object)
>
> - id: 5da429b5308a95c204db6454 (string, optional, sample) - The ID of the furniture item
> - name: KULLABERG (string, required, sample) - The name of the furniture item
> - type: Desk (string, required, sample) - The type of the furniture item
> - price: 1500.00 (number, required, sample) - The price of the furniture item
> - colour: red, green (array[string], optional, sample) - The colour(s) of the furniture item
> ```

Another common use case is to have nested objects, an object residing inside another object, using the furniture example above, you can add a materials field that contains an array of Material objects.

> ```markdown
> ## Furniture (object)
>
> - id: 5da429b5308a95c204db6454 (string, optional, sample) - The ID of the furniture item
> - name: KULLABERG (string, required, sample) - The name of the furniture item
> - type: Desk (string, required, sample) - The type of the furniture item
> - price: 1500.00 (number, required, sample) - The price of the furniture item
> - colour: red, green (array[string], optional, sample) - The colour(s) of the furniture item
> - materials (array[Material], required) - The materials used to make the furniture item
>
> ## Material (object)
> - id: 123456789 (number, required, sample) - The id of the material component
> - type: wood (string, required, sample) - The type of the material
> - length: 100 (string, required, sample) - The length of the material in mm
> ```

Now the Material object has been created and the Furniture object uses this in it's materials field which contains an array of type `Material`, when rendered in the documentation this is how it would look.

> ![alt text][apiary_editor_complex_object_example]

The final example of complex types is where a type inherits the fields from another type, for example if you have a set of fields that are often re-used across multiple objects then those fields can be placed into their own object and can be inherited.

> ```markdown
> ## Furniture (AuditFields)
> - id: 5da429b5308a95c204db6454 (string, optional, sample) - The ID of the furniture item
> - name: KULLABERG (string, required, sample) - The name of the furniture item
> - type: Desk (string, required, sample) - The type of the furniture item
> - price: 1500.00 (number, required, sample) - The price of the furniture item
> - colour: red, green (array[string], optional, sample) - The colour(s) of the furniture item
>
> ## AuditFields (object)
> - creationDate: `29-09-2019` (string, required, sample) - The creation date of the object
> - createdBy: user1 (string, required, sample) - The user id who created the object
> - lastUpdatedDate: `14-10-2019` (string, required, sample) - The date the object was last updated
> - lastUpdatedBy: user2 (string, required, sample) - The user id who last updated the object
> ```

Now you can see that the Furniture object inherits all of the fields on the AuditFields object, it's worth noting that any field inherited using the above approach will always appear at the start of the object, i.e. the AuditFields fields will be rendered before the Furniture fields.

> ![alt text][apiary_editor_complex_object_inheritance_example]

More detailed documentation can be found on the [MSON GitHub repository](https://github.com/apiaryio/mson).

### Exercise 3: Adding a Data Structure

This exercise will introduce you to the Data Structure sections of the Apiary document.

#### Exercise 3 - Required Tools

- Internet Browser

#### Exercise 3 - Task

Currently the Data Structures section of the document does not contain a Furniture object, you need to create a furniture object so it can be re-used across multiple resources.

The entire furniture object contains the fields and all fields are required:

- id
- name
- type
- price

Remember to add a sample value for each field.

> _Tip: The basic primitive types in Apiary are `string` and `number`_

#### Exercise 3 - Success Criteria

- [ ] New data structure named "Furniture"
- [ ] Appropriate data types chosen for the four fields
- [ ] Remove comments related to this exercise

## Section 4 - Request and Response Bodies

### Specific Request Bodies

In order to start the request section, you use the notation `+ Request`, any information on lines after this will be treated as part of the request body.

You are also able to specify the request content-type if the request body contains data, this is done by adding `(content-type)` to the end of the `+ Request` line.

> _For Example: `+ Request (application/json;charset=UTF-8)` means a Request Body with Content-Type `application/json;charset=UTF-8`_
>
> ![alt text][apiary_editor_request_content_type]

If the request body contains any data/attributes then you include these in the line underneath `+ Request`, for API blueprint to be rendered properly, the data/attributes should be indented by **four spaces** or **one TAB** character and is denoted using the `Attributes` field.

> ![alt text][apiary_editor_request_attributes]

Additionally you are able to specify any additional headers to be used on the request, for IPIM-IP we often include as a minimum an _api-key_ which is required to be passed for any API call, to add custom headers in the Apiary document they should be indented by **twelve spaces** or **three TAB** characters from the `+ Request` heading and the headers are denoted using the `Headers` field.

> ![alt text][apiary_editor_request_headers]

### Specific Response Bodies

In order to start the response section, you use the notation `+ Response`, any information on lines after this will be treated as part of the response body. Along with declaring the start of the response section, you also have to specify the [HTTP status code](https://www.restapitutorial.com/httpstatuscodes.html) that the response should return.

You are also able to specify the response content-type if the response body contains data, this is done by adding `(content-type)` to the end of the `+ Response` line.

> _For Example: `+ Response 200 (application/json;charset=UTF-8)` means a Response Body with Content-Type `application/json;charset=UTF-8` that returns HTTP Status 200_
>
> ![alt text][apiary_editor_response_content_type]

If the response body contains any data structures then you include these in the line underneath `+ Response`, for API blueprint to be rendered properly, the data/attributes should be indented by **four spaces** or **one TAB** character and is denoted using the `Attributes` field.

> ![alt text][apiary_editor_response_attributes]
>
> _Note: The response can be an Array of objects, a single object or no objects, be sure to choose the appropriate response type and http status code for your resource_

Sometimes, you want to include multiple responses for a single request, this is useful when the resource could return a custom error such as `ID Not Found`, to create multiple responses you simple create another `+ Response` section.

> ![alt text][apiary_editor_response_multiple]
>
> _Note: If your response **does not** use a data structure then you can omit the `Attributes` declaration and use the `Body` declaration instead to reference the JSON_

Additionally you are able to specify any additional headers to be sent on the response, to add custom headers in the Apiary document they should be indented by **twelve spaces** or **three TAB** characters from the `+ Response` heading and the headers are denoted using the `Headers` field.

> ![alt text][apiary_editor_response_headers]
> 
### Exercise 4.1: Modifying Request & Response Bodies

This exercise will introduce you to the Request and Response sections of the Apiary document.

> _Note: Refer back to the [Specific Request Bodies](#specific-request-bodies) and [Specific Response Bodies](#specific-response-bodies) sections for more information._

#### Exercise 4.1 - Required Tools

- Internet Browser

#### Exercise 4.1 - Task

Currently the `Create` resource does not send or receive any fields as part of the request/response body, your task is to alter the request and response by adding the `Attributes` field so that the entire furniture object is passed in the request/response using the data structure you created in [Exercise 3: Adding a Data Structure](#exercise-3-adding-a-data-structure).

> _Tip: Remember the differences in syntax when using a `Data Structure` as opposed to a `JSON Object`_

#### Exercise 4.1 - Success Criteria

- [ ] Updated `Create` resource, `Request` section to include the entire Furniture object
- [ ] Updated `Create` resource, `Response` section to include the entire Furniture object
- [ ] Using the Console, ensure the request and response bodies contains the entire Furniture object
- [ ] Remove comments related to this exercise

### Exercise 4.2: Adding Request and Response Bodies

This exercise introduces you to the concept of multi-request and multi-response resources.

#### Exercise 4.2 - Required Tools

- Internet Browser

#### Exercise 4.2 - Task

The `Create` resource currently showcases the "happy" path of an API, where the request is accepted and processed before returning with an object in the response. This exercise includes adding a un-happy path for a "bad" request that returns a particular error response.

In your service, it should return an error to the user if all of the fields of a Furniture object are not sent in the request.

Based on this requirement, your Request body should be missing the `id` and `name` fields, which should return a `Bad Request` error in the response with a suitable message/status combination.

#### Exercise 4.2 - Success Criteria

- [ ] New request body containing subset of the fields
- [ ] New response body containing message and status fields
- [ ] Bad Request response status code
- [ ] Using the Console, test out the new "un-happy" path for the `Create` resource
- [ ] Remove comments related to this exercise

## Section 5 - Tying Everything Together
### Exercise 5: Adding New Endpoints

In this final exercise, you will combine your learnings from the previous set of exercises in order to add a whole new endpoint to the Apiary document that includes request/response bodies with a new data structure.

#### Exercise 5 - Required Tools

- Internet Browser

#### Exercise 5 - Task

Based on your knowledge gained from earlier Exercises and the Introduction to Apiary section, your task is to create a new endpoint that handles the `Get By Id` resource.

This new endpoint should include a Path Parameter for the ID variable along with both a "happy" and "un-happy" path, an un-happy request can be classified if the ID of the furniture item is not found.

> _Tip: Don't forget to add the URI for the Get Furniture By Id resource_

#### Exercise 5 - Success Criteria

- [ ] New path parameter for ID
- [ ] "Happy" path Request and a suitable `OK` Response
- [ ] "Un-Happy" path Request and a suitable `Not Found` Response
- [ ] Understanding of how Apiary documents work
- [ ] Remove comments related to this exercise

<!-- ## Appendix -->

<!-- TODO -->

<!-- ## Frequently Asked Questions -->

<!-- The section below contains a list of common questions along with their corresponding answers people often ask whilst working with the tools used in this lab. -->

<!-- ### Q: Are you able to add dynamic responses based on the query/path parameters?

  A: The simple answer is no. Arguably, from a consumers perspective this is not required so long as the mock response contains an example showing every available field. -->


<!-- - [TODO](#todo) -->
<!-- - [TODO 2](#todo-2) -->

<!-- --- -->

<!-- ### Q: TODO -->

<!-- A: TODO -->

<!-- --- -->

<!-- ### Q: TODO 2 -->

<!-- A: TODO -->

[apiary_menu_toolbar]: images/apiary_menu_toolbar.png "Apiary Menu Toolbar"
[apiary_console_mock_server]: images/apiary_console_mock_server.png "Apiary Console Mock Server"
[apiary_desc_and_group]: images/apiary_desc_and_group.png "Apiary Description and Group"
[apiary_example_area_populated]: images/apiary_example_area_populated.png "Apiary Example Area - Populated"
[apiary_example_area]: images/apiary_example_area.png "Apiary Example Area"
[apiary_example_mock_server]: images/apiary_example_mock_server.png "Apiary Example Area - Mock Server"
[apiary_doc_resources]: images/apiary_doc_endpoints.png "Apiary Documentation Resources"
[apiary_editor_format_and_host]: images/apiary_editor_format_and_host.png "Apiary Editor - Format and Host"
[apiary_editor_heading_level_1]: images/apiary_editor_heading_level_1.png "Apiary Editor - Heading Level 1"
[apiary_editor_logical_group_1]: images/apiary_editor_logical_group_1.png "Apiary Editor - Logical Group 1"
[apiary_editor_request_1]: images/apiary_editor_request_1.png "Apiary Editor - Request 1"
[apiary_editor_request_content_type]: images/apiary_editor_request_content_type.png "Apiary Editor - Request Content Type"
[apiary_editor_request_attributes]: images/apiary_editor_request_attributes.png "Apiary Editor - Request Attributes"
[apiary_editor_request_headers]: images/apiary_editor_request_headers.png "Apiary Editor - Request Headers"
[apiary_editor_response_content_type]: images/apiary_editor_response_content_type.png "Apiary Editor - Response Content Type"
[apiary_editor_response_attributes]: images/apiary_editor_response_attributes.png "Apiary Editor - Response Attributes"
[apiary_editor_response_multiple]: images/apiary_editor_response_multiple.png "Apiary Editor - Multiple Responses"
[apiary_editor_response_headers]: images/apiary_editor_response_headers.png "Apiary Editor - Response Headers"
[apiary_editor_request_query_parameter]: images/apiary_editor_request_query_parameter.png "Apiary Editor - Request Query Parameters"
[apiary_editor_request_query_parameter_example]: images/apiary_editor_request_query_parameter_example.png "Apiary Editor - Request Query Parameters Example"
[apiary_editor_parameters]: images/apiary_editor_parameters.png "Apiary Editor - Parameters"
[apiary_editor_parameters_example]: images/apiary_editor_parameters_example.png "Apiary Editor - Parameters Example"
[apiary_editor_request_path_parameter]: images/apiary_editor_request_path_parameter.png "Apiary Editor - Request Path Parameters"
[apiary_editor_request_path_parameter_example]: images/apiary_editor_request_path_parameter_example.png "Apiary Editor - Request Path Parameters Example"
[apiary_editor_complex_object_example]: images/apiary_editor_complex_object_example.png "Apiary Editor - Complex Object Example"
[apiary_editor_complex_object_inheritance_example]: images/apiary_editor_complex_object_inheritance_example.png "Apiary Editor - Complex Object Inheritance Example"
[apiary_documentation_endpoints_highlighted]: images/apiary_documentation_endpoints_highlighted.png "Apiary Documentation - Endpoints Highlighted"

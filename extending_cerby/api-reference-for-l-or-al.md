---
description: "This document describes how to consume the certification and naming field endpoints from the Cerby API, which enable obtaining corporate account information."
intercom_id: 13366156
hidden: true
noIndex: true
---

# API reference for L'Oréal

The Cerby API implements a set of rules and protocols that enable L'Oréal’s custom applications to communicate with Cerby. To interact with the API, you must send a request to a specific endpoint, which our API processes to return a JSON-encoded response.

The following are the data collections available in our API exclusive to L'Oréal:

* [Certifications](api-reference-for-l-or-al.md#recertification)
* [Account naming fields](api-reference-for-l-or-al.md#naming-fields-(smart-collections))
* [Collection naming fields](api-reference-for-l-or-al.md#list-the-naming-fields-of-a-corporate-collection)

For the public Cerby API endpoints, refer to the documentation in [Cerby's Developer Portal](https://developer.cerby.com/).

* * *

## Authentication

The Cerby API uses the X-API-Key parameter in the header of each API request. To generate and retrieve the value of the key, you must follow the instructions in the article [Generate an API key](https://help.cerby.com/en/articles/9450943-generate-an-api-token) and select the required scopes for the endpoint you plan to use.

**IMPORTANT:**

  * If the API key is expired or does not have the correct scopes, the Cerby API returns a `401` error.
  * Your API keys are sensitive resources because they grant access to the data stored in your workspace. Avoid sharing them in public repositories or client-side code.

---

* * *

## URL structure

The full URL of an endpoint in the Cerby API is the following:

    https://{my-workspace}.cerby.com/api/v1/{resource}/{path-parameter}?{query-parameter}={custom-value}

The following is the structure of the URL:

  * **Protocol:** The secure communication method to transmit data is HTTPS.
  * **Domain:** The base URL is `{my-workspace}.cerby.com/api/v1`. You must replace `{my-workspace}` with the name of your workspace.
  * **Resource:** The specific Cerby resource being accessed.
  * **Parameter:** The additional data to specify the resource you want to access, filter, paginate, or sort in the response. The Cerby API includes the following parameter types:
    * **Path parameter:** Path parameters specify the resource you want to access with the endpoint. In the Cerby API, path parameters are embedded in the URL.
    * **Query parameter:** Query parameters paginate, filter, or sort the results of the request. In the Cerby API, query parameters are appended to the URL after a question mark character (`?`) and separated by ampersands (`&`).
* * *

## Recertification

L'Oréal’s recertification process is based on the company’s security review process to ensure account security and adherence to internal policies. The criteria for recertifying accounts reflect L'Oréal’s standards for account access and management.

A `certification` object contains information about the recertified account, its status, the date when the account was recertified, and who recertified it, as well as when the next recertification date is.

The `certification` object is created in Cerby for the following L'Oréal social media accounts:

  * Meta (Instagram and Facebook)
  * TikTok
  * Pinterest
  * X (Twitter)
  * Snapchat
  * YouTube

The `certification` object is created in Cerby for the following L'Oréal business hub accounts:

  * Meta Business
  * TikTok for Business
  * Pinterest Business
  * Snapchat Business

To learn more about L'Oréal’s recertification process, refer to the following articles on the Cerby Help Center:

  * [Simplify your account recertification process with Cerby](https://help.cerby.com/en/articles/10707843-recertify-your-social-organic-accounts-and-business-hubs)
  * [Recertify your social organic accounts and Business Hubs](https://help.cerby.com/en/articles/10707843-recertify-your-social-organic-accounts-and-business-hubs)
  * [Recertification criteria for L'Oréal](https://help.cerby.com/en/articles/10228345-recertification-criteria-for-l-oreal)

### The certification object

The following table describes the attributes of a `certification` object:

**Attributes**| **Description**
---|---
`attributes` _object_|  The attributes of the certification.

  * `accountId` _string_

|  The unique identifier of the certified account.

  * `certificationDueAt` _string_

|  The date the certification is due in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).

  * `certificationPeriodDays` _integer_

|  The length of the certification period in days.

  * `certifiedAt` _string_

|  The date on which the certification was completed in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).

  * `certifiedById` _string_

|  The unique identifier of the user who completed the certification.

  * `certifiedByName` _string_

|  The name of the user who completed the certification.

  * `createdAt` _string_

|  The date when the certification record was created in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).

  * `lastCertifiedAt` _string_

|  The date when the account was last recertified in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).

  * `nextCertificationDate` _string_

|  The next scheduled recertification date in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).

  * `status` _string_

|  The certification status. The possible values are:

  * `todo`
  * `completed`
  * `expired`
  * `tasks` _array_

|  The list of recertification tasks completed for the account. Each object in this array has the following characteristics:

  * **`data`** (_array_): The objects of completed tasks for recertification. The criterion for each account depends on whether it is an organic or business hub account.
    * **Organic accounts:**
      * `managedEmailCreated`**** and****`validateEmail`
      * `managedPhoneCreated`**** and `validatePhone`
      * `managed2FACreated` and `validate2FA`
      * `validatePasswordRotation`
      * `verifyOwners` and `verifyUsers`
      * `businessHubComment` and `businessHubLinked`
      * `verifiedByPlatform`
      * `agencySetup`
    * **Business hubs:**
      * `agencySetup`
      * `platform2FA`
      * `onboardedUsers`**,**`verifyOwners`**,** and****`verifyUsers`
      * `thirdPartyAccess`
  * **`name`** (_string_): The name of the recertification criteria.
  * **`status`** (_string_): The status of the recertification criteria. The possible values are: `completed` and `todo`.
  * **`updatedAt`** (_string_): The date when the criteria was last updated.
  * **`updatedById`** (_string_): The ID of the user or system that last updated the criteria.
  * **`updatedByType`** (_string_): The type of user or system that updated the criteria.
  * `updatedAt` _string_

|  The date when the certification record was last updated in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).
`id` _string_|  The unique identifier of the certification.
`type` _string_|  The item type is always `account_certification`.

### The links object

The `links` object provides the related URLs that can be helpful for navigation.

The following table describes the attributes of a `links` object:

**Attribute**| **Description**
---|---
`links` _object_|  The attributes of the links object.

  * `next` _string_

|  The next page of results.

  * `previous` _string_

|  The previous page of results.

  * `self` _string_

|  The self reference to the endpoint you are calling.

### The meta object

The meta object contains metadata about the response that provides additional context or information about the data object.

The following table describes the attributes of a meta object:

**Attribute**| **Description**
---|---
`meta` _object_|  The attributes of the meta object.

  * `page` _object_

|  The attributes of the page in the response.

  * `maxSize` _number_

|  The maximum number of items that can be returned per page.

  * `total` _number_

|  The total number of items available across all pages.

### List account recertifications

With the `GET` request to the `/certifications` endpoints, you can retrieve the list of account certifications visible to the API key holder.

**IMPORTANT:** The API scope required to use this endpoint is: **Read accounts**.
---

#### Query parameters

The following table describes the query parameters of a request:

**Parameter**| **Required**| **Description**
---|---|---
`page[number]`_integer_| `false`| The page number to retrieve in a paginated list. The default and minimum value is 1.
`page[size]`_integer_|  false| The number of items to display per page. The default value is 20; the maximum is 100.
`filter[accountId]`_string_|  false| The comma-separated list of account IDs to get the recertification status.
`filter[status]`_string_|  false| The comma-separated list of certification statuses to include. The possible values are:

  * `todo`
  * `completed`
  * `expired`

`filter[ownerId]`_string_|  false| The comma-separated list of account owner IDs.

#### Response

The following table describes the response status and messages:

**Status**| **Response**| **Description**| **Schema**
---|---|---|---
`200`| `OK`| The requested recertification JSON object.|

  * An array of [Certification objects](api-reference-for-l-or-al.md#the-certification-object)
  * [Links](api-reference-for-l-or-al.md#the-links-object)
  * [Meta](api-reference-for-l-or-al.md#the-meta-object)

`400`| `Bad request`| The server could not understand the request due to invalid syntax or missing parameters.Review your request and correct it.|

    {
      "errors": [
          {
        "code": "validation_error",
        "detail": "field required",
        "meta": {
           "loc": [
                "data"
            ],
            "msg": "field required",
            "type": "value_error.missing"
         },
         "status": "400",
         "title": "validation_error"
       }
     ]
    }

`403`| `Forbidden`| The API key does not have permission to perform the request.Verify that your API key has the required scopes.|

    {
        "errors": [
        {
          "code": "forbidden",
          "detail": "User is not authorized to perform the request.",
           "meta": null,
           "status": "403",
           "title": "forbidden"
         }
       ]
    }

#### Example

##### Request

The following is an example of a request to the endpoint:

    https://{my-workspace}.cerby.com/api/v1/certifications

**cURL:**

    curl --location 'https://{my-workspace}.cerby.com/api/v1/certifications' \
    --header 'x-api-key: {api-key}'

**HTTPS:**

    GET /api/v1/certifications HTTP/1.1
    Host: {my-workspace}.cerby.com
    x-api-key: {api-key}

**Javascript:**

    // WARNING: For GET requests, body is set to null by browsers.

    var xhr = new XMLHttpRequest();
    xhr.withCredentials = true;

    xhr.addEventListener("readystatechange", function() {
      if(this.readyState === 4) {
        console.log(this.responseText);
      }
    });

    xhr.open("GET", "https://{my-workspace}.cerby.com/api/v1/certifications");
    xhr.setRequestHeader("x-api-key", "{api-key}");

    xhr.send();

**Python:**

    import http.client

    conn = http.client.HTTPSConnection("{my-workspace}.cerby.com")
    payload = ''
    headers = {
      'x-api-key': '{api-key}'
    }
    conn.request("GET", "/api/v1/certifications", payload, headers)
    res = conn.getresponse()
    data = res.read()
    print(data.decode("utf-8"))

##### Response

The following is an example of the response object:

    {
        "data": [
            {
                "attributes": {
                    "accountId": "85ff51cf-0bea-4416-811e-8a8aa2aa8ff1",
                    "certificationDueAt": "2025-07-18T16:41:00+00:00",
                    "certificationPeriodDays": -185,
                    "certifiedAt": null,
                    "certifiedById": null,
                    "certifiedByName": "certified_by_id not provided",
                    "createdAt": "2025-05-27T17:49:05.964000+00:00",
                    "lastCertifiedAt": null,
                    "nextCertificationDate": "2026-01-18T16:41:00+00:00",
                    "status": "expired",
                    "updatedAt": "2025-07-08T00:52:32.704000+00:00"
                },
                "id": "5fc3b263-0e6f-4167-872b-28baf955ce94",
                "type": "account_certification"
            }
        ],
        "links": {
            "next": null,
            "previous": null,
            "self": "/api/v1/certifications?page%5Bnumber%5D=1&page%5Bsize%5D=20"
        },
        "meta": {
            "page": {
                "maxSize": 100,
                "total": 1
            }
        }
    }

* * *

## Naming fields (Smart collections)

L'Oréal's naming fields are a structured, automated way to organize accounts and collections in the workspace using predefined tags (naming fields), replacing manual, inconsistent collection management.

The `naming-fields` object contains information about a corporate account and collection tags, including its name and value, as well as the date the field was added and updated.

The `naming-fields` object is created when a new corporate account is created in the L’Oréal workspace, or when a collection is updated with tags. To learn more about L'Oréal’s naming fields (smart collections), refer to the article [Explore Smart Collections](https://help.cerby.com/en/articles/9422854-explore-smart-collections) on the Cerby Help Center.

### The naming fields object

The following table describes the attributes of a certification object:

**Attributes**| **Description**
---|---
`attributes` _object_|  The attributes of the naming fields.

  * `fields` _array_

|  The list of the naming fields for the account or collection.

  * `name` _string_

|  The name of the naming field.

  * `value` _string_

|  The value associated with the naming field.

  * `createdAt` _string_

|  The date when the naming field was created in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).

  * `updatedAt` _string_

|  The date when the naming field was last updated in the [ISO 8610 format](https://www.iso.org/iso-8601-date-and-time-format.html).
`id` _string_|  The unique identifier of the naming fields.
`type` _string_|  The resource type is always `naming-fields`.

### List the naming fields (tags) of a corporate account

With the `GET` request to the `/accounts/{account_id}/naming-fields` endpoints, you can retrieve the naming fields associated with an account by its ID.

**IMPORTANT:** The API scope required to use this endpoint is: **Read accounts**.
---

#### Path parameters

The following table describes the path parameters of a request:

**Parameter**| **Required**| **Description**
---|---|---
`id` _string_|  true| The unique identifier of the account.

#### Response

The following table describes the response status and messages:

**Status**| **Response**| **Description**| **Schema**
---|---|---|---
`200`| `OK`| The requested naming field JSON object.| The [naming fields object](api-reference-for-l-or-al.md#the-naming-fields-object)
`403`| `Forbidden`| The API key does not have permission to perform the request.Verify that your API key has the required scopes.|

    {
      "errors": [
      {
         "code": "forbidden",
         "detail": "User is not authorized to perform the request.",
          "meta": null,
          "status": "403",
          "title": "forbidden"
       }
     ]
    }

**`404`**| `Not found`| Not found. The requested resource could not be found.|

    {
      "errors": [
        {
          "code": "not_found",
          "detail": "Resource not found.",
          "meta": null,
          "status": 404,
          "title": "not_found"
        }
      ]
    }

#### Example

##### Request

The following is an example of a request to the endpoint:

    https://{my-workspace}.cerby.com/api/v1/accounts/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields

**cURL:**

    curl --location 'https://{my-workspace}.cerby.com/api/v1/accounts/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields' \
    --header 'x-api-key: {api-key}'

**HTTPS:**

    GET /api/v1/accounts/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields HTTP/1.1
    Host: {my-workspace}.cerby.com
    x-api-key: {api-key}

**Javascript:**

    // WARNING: For GET requests, body is set to null by browsers.

    var xhr = new XMLHttpRequest();
    xhr.withCredentials = true;

    xhr.addEventListener("readystatechange", function() {
      if(this.readyState === 4) {
        console.log(this.responseText);
      }
    });

    xhr.open("GET", "https://{my-workspace}.cerby.com/api/v1/accounts/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields");
    xhr.setRequestHeader("x-api-key", "{api-key}");

    xhr.send();

**Python:**

    import http.client

    conn = http.client.HTTPSConnection("{my-workspace}.cerby.com")
    payload = ''
    headers = {
      'x-api-key': '{api-key}'
    }
    conn.request("GET", "/api/v1/accounts/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields", payload, headers)
    res = conn.getresponse()
    data = res.read()
    print(data.decode("utf-8"))

##### Response

The following is an example of the response object:

    {
      "data": {
        "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
        "type": "naming-fields",
        "attributes": {
          "fields": [
            {
              "name": "social_media_type",
              "value": "organic"
            },
            {
              "name": "additionalInformation",
              "value": "test_info"
            }
          ],
          "createdAt": "2026-01-02T04:21:22.158Z",
          "updatedAt": "2026-01-02T04:21:22.158Z"
        }
      }
    }

### List the naming fields of a corporate collection

With the `GET` request to the `/collections/{id}/naming-fields` endpoints, you can retrieve the naming fields associated with a collection by its ID.

**IMPORTANT:** The API scope required to use this endpoint is **Read items**.
---

### Path parameters

The following table describes the path parameters of a request:

**Parameter**| **Required**| **Description**
---|---|---
`id` _string_| `true`| The unique identifier of the collection.

### Response

The following table describes the response status and messages:

**Status**| **Response**| **Description**| **Schema**
---|---|---|---
`200`| `OK`| The requested naming field JSON object.| The [naming fields object](https://docs.google.com/document/d/16aoERgcl3kmXxwCD97J2txoZr6zxQkEzOmCKn1MROrE/edit?tab=t.0#heading=h.dwj8g1n4zmsd)
`403`| `Forbidden`| The API key does not have permission to perform the request.Verify that your API key has the required scopes.|

    {
     "errors": [
     {
       "code": "forbidden",
       "detail": "User is not authorized to perform the request.",
       "meta": null,
       "status": "403",
       "title": "forbidden"
      }
     ]
    }

`404`| `Not found`| Not found. The requested resource could not be found.|

    {
     "errors": [
     {
       "code": "not_found",
       "detail": "Resource not found.",
       "meta": null,
       "status": 404,
       "title": "not_found"
      }
     ]
    }

### Example

### Request

The following is an example of a request to the endpoint:

    https://{my-workspace}.cerby.com/api/v1/collections/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields

**cURL:**

    curl --location 'https://{my-workspace}.cerby.com/api/v1/collections/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields' \
    --header 'x-api-key: {api-key}'

**HTTPS:**

    GET /api/v1/collections/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields HTTP/1.1
    Host: {my-workspace}.cerby.com
    x-api-key: {api-key}

**Javascript:**

    // WARNING: For GET requests, body is set to null by browsers.

    var xhr = new XMLHttpRequest();
    xhr.withCredentials = true;

    xhr.addEventListener("readystatechange", function() {
      if(this.readyState === 4) {
        console.log(this.responseText);
      }
    });

    xhr.open("GET", "https://{my-workspace}.cerby.com/api/v1/collections/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields");
    xhr.setRequestHeader("x-api-key", "{api-key}");

    xhr.send();

**Python:**

    import http.client

    conn = http.client.HTTPSConnection("{my-workspace}.cerby.com")
    payload = ''
    headers = {
      'x-api-key': '{api-key}'
    }
    conn.request("GET", "/api/v1/collections/989165cc-112c-4112-a877-e047ffe9abcd/naming-fields", payload, headers)
    res = conn.getresponse()
    data = res.read()
    print(data.decode("utf-8"))

### Response

The following is an example of the response object:

    {
        "data": {
            "attributes": {
                "createdAt": "2026-01-21T15:43:38.088000+00:00",
                "fields": [
                    {
                        "name": "brand",
                        "value": "skinbetter_sciences"
                    },
                    {
                        "name": "division",
                        "value": "ldb"
                    },
                    {
                        "name": "market",
                        "value": "co"
                    },
                    {
                        "name": "social_media_type",
                        "value": "paid"
                    },
                    {
                        "name": "zone",
                        "value": "latam"
                    }
                ],
                "updatedAt": "2026-01-21T15:43:38.088000+00:00"
            },
            "id": "4772920a-1bc2-4376-a9f3-6e9a3f96b9f8",
            "type": "naming_fields"
        }
    }

# API endpoints reference

**Description:** This article describes the endpoints available in the Cerby Read API to retrieve information saved in your workspace.

The Cerby Read API has endpoints tailored to retrieve information about the
accounts and members in your Cerby workspace. This reference article describes
the purpose of each endpoint, its intended usage, parameter specifications,
and request and response formats.

  * Accounts

  * Members

The following sections contain the description of each available endpoint.

* * *

# Accounts

The following are the endpoints available for accounts:

  * Get all accounts

  * Get the information of an account by ID

The following sections describe each endpoint.

## **Get all accounts**

With a `GET` request to the `/v1/accounts` endpoint, you can retrieve a list
of all your accounts in Cerby.

## Request

The following is the HTTP request method for the endpoint:

  * **Request URL:** `https://api.cerby.com/v1/accounts`

  * **Method:** `GET`

  * **Query parameters:**

    * `limit` (Number): Indicates the number of account objects returned in the accounts array

    * `startIndex` (Number): Indicates the starting index within the response array from which results are displayed

    * `search` (String): Returns accounts with full or partial matches for the value sent in this parameter

    * `status` (String): Indicates the status of the account. Possible values: 

      * `pending`

      * `provision`

      * `success`

      * `enabled`

      * `disabled`

    * `type` (String): Indicates the account type. Possible values: 

      * `identity`

      * `resource`

      * `secret`

      * `integration`

    * `role` (String): Indicates the user role on the account. Possible values: 

      * `account_owner`

      * `account_manager`

      * `account_collaborator`

    * `app` (String): Returns the list of accounts that belong to the provided comma-separated app IDs

    * `collections` (String): Returns the list of accounts that belong to the provided comma-separated collection IDs

    * `ids` (String): Returns the list of accounts that match the provided comma-separated account IDs

    * `teamIds` (String): Returns the list of accounts that belong to the provided comma-separated team IDs

    * `sortBy` (String): Sorts the results in one of the following orders and values:

      * `sorting_query_by_recently_used`: Recently used account 

      * `sorting_query_by_alpha_asc`: Ascending in alphabetical order, from A to Z 

      * `sorting_query_by_alpha_desc`: Descending in alphabetical order, from Z to A 

      * `sorting_query_by_newest_created`: Newest created accounts

      * `sorting_query_by_oldest_create`: Oldest created accounts 

    * `provider` (String): Returns the list of accounts that belong to the provided comma-separated application or service provider IDs

    * `filterHidden` (Boolean): true to filter results and only include hidden accounts; else, false

    * `connectedAccounts` (Boolean): true if this is an account with access to the secrets of another account; else, false

    * `proxyAccounts` (Boolean): true if this is an account used to access the assets of a SaaS, business hub, or paid social app; else, false

    * `pendingAccounts` (Boolean): true if this is an account pending to be connected to an app integration; else, false

    * `applicationTypes` (String): Indicates the type of application. Possible values:

      * `tenant`

      * `connected _account`

    * `applicationTypesToExclude` (String): Indicates the type of application to exclude from the request. It has the same possible values as `applicationTypes`

    * `excludeBusinessAssets` (Boolean): true to filter results and exclude business hub assets; else, false

    * `includePendingActions` (Boolean): true to filter results and include only accounts with pending actions; else, false

    * `domain` (String): Returns the domain of the application or service provider

## Response

The response JSON object has the following main keys:

  * startIndex (Number): Indicates the starting index within the response array from which results are displayed

  * limit (Number): Indicates the number of account objects returned in the accounts array. The default value is 20

  * totalResults (Number): Indicates the number of accounts returned, which must be the same number of accounts you see in your workspace

  * accounts (Array): Contains the account objects. The returned accounts must correspond to the accounts in your workspace

## Example

The following is an example of a request to the endpoint:

`https://api.cerby.com/v1/accounts?excludeBusinessAssets=True&limit=30&sortBy=used&startIndex=1`

The following is an example of the response object:

    
    
    {  
      "limit": 20,  
      "startIndex": 1,  
      "totalResults": 15  
      "accounts": [  
        {account}  
      ]  
    }

## **Get the information of an account by ID**

With a `GET` request to the `/v1/accounts/{id}` endpoint, you can retrieve the
information of a particular account by providing its ID.

## Request

The following is the HTTP request method for the endpoint:

  * **Request URL:** `https://api.cerby.com/v1/accounts/{id}`

  * **Method:** `GET`

  * **Path parameters:**

    * `id` (String): The ID of the account you want to retrieve.

## Response

The response is an [account](https://help.cerby.com/en/articles/9451004-data-
definitions#h_954a0c969f) object.

## Example

The following is an example of a request to the endpoint:

`https://api.cerby.com/v1/accounts/55d3a51f-9181-46b9-9f43-cbb915155c66`

* * *

# Members

## **Get the list of all members**

With a `GET` request to the `/v1/admin/users` endpoint, you can retrieve a
list of all the members in your Cerby workspace.

## Request

The following is the HTTP request method for the endpoint:

  * **Request URL:** `https://api.cerby.com/v1/admin/users`

  * **Method:** `GET`

  * **Path parameters:**

    * `search` (String): Returns the members with full or partial matches of their names or emails with the value of this parameter

    * `startIndex` (Number): Indicates the starting index within the response array from which results are displayed. The default value is 1

    * `count` (Number): Indicates the number of member objects returned in the accounts array. The value by default is 20

    * `userIds` (String): Returns the list of members that match the provided comma-separated member IDs

    * `onlyInIdp` (Boolean): true to get the list of used that belong to the identity provider but not in the Cerby workspace; else, `false`

    * `status` (String): Indicates the status (es) of the member (more than one status can be sent using commas). Possible values: live, pending, disabled

    * `isGuest` (Boolean): true if the member is a guest user; else, `false`

## Response

The response JSON object has the following main keys:

  * `totalResults` (Number): Indicates the total number of members returned, which must be the same number of members you see in your workspace in total.

  * `itemsPerPage` (Number): Indicates the number of member objects returned per page in the response

  * `startIndex` (Number): Indicates the starting index within the response array from which results are displayed

  * `resources` (Array): Contains the [member](https://help.cerby.com/en/articles/9451004-data-definitions#h_c491e2e26d) objects. The members returned must correspond to the members you have in your workspace.

## Example

The following is an example of a request to the endpoint:

`https://api.cerby.com/v1/admin/users`

The following is an example of the response:

    
    
    {  
        "totalResults": 152,  
        "itemsPerPage": 20,  
        "startIndex": 1,  
        "resources": [  
            {member}  
        ]  
    }

## **Get the list of accounts corresponding to a member**

With a `GET` request to the `/v1/users/{id}/accounts` endpoint, you can
retrieve the list of accounts a specific user has created or has shared access
to.

## Request

The following is the HTTP request method for the endpoint:

  * **Request URL:** `https://api.cerby.com/v1/users/{id}/accounts`

  * **Method:** `GET`

  * **Path parameters:**

    * `id` (String): The ID of the Cerby member whose accounts you want to retrieve

## Response

The response JSON is an array of
[account](https://help.cerby.com/en/articles/9451004-data-
definitions#h_954a0c969f) objects that belong to the member.

## Example

The following is an example of a request to the endpoint:

`https://api.cerby.com/v1/users/e43ea05c-9c4b-4eb3-9fa6-960fc34ac9b1/accounts`

The following is an example of the response:

    
    
    [  
        {account}  
    ]


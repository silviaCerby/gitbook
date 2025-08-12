# Explore the Cerby Read API

**Description:** This article describes the capabilities and request methods of the Cerby Read API to retrieve user and account data from Cerby.

Cerby has built a public application programming interface (API) that enables
you to retrieve information about workspace users and accounts stored in the
platform.

The Cerby Read API follows RESTful principles and the [OpenAPI 3.0
Specifications](https://spec.openapis.org/oas/latest.html), and communicates
over HTTPS for secure data transmission.

To authorize your requests, you must provide an API token or bearer that can
only be generated and retrieved from the Cerby web app after authenticating
into your corporate identity provider, such as Okta or Entra ID.

The Cerby Read API supports the following HTTP request methods:

  * GET requests to the following endpoints to retrieve information about the accounts stored in the Cerby platform:

    * `/v1/accounts`

    * `/v1/accounts/{id}`

  * GET requests to the following endpoints to retrieve information about the members of a Cerby workspace and the accounts they have access to:

    * `/v1/admin/users`

    * `/v1/users/{id}/accounts`

* * *

# Authorization

All requests to the Cerby Read API must be authorized using a valid API token
generated via the Cerby web app or a bearer token. API tokens must be included
in the **X-API-Key** header of each API request, whereas bearer tokens must be
in the **Authorization** header.

When performing a request, the Cerby Read API first tries to authorize it via
the API token. If the API token is not present, authorization is via a bearer
token. The Cerby Read API returns a 401 error if none of these tokens are
present.

For more information on how to generate and retrieve a token, read the
articles [Generate an API
token](https://help.cerby.com/en/articles/9450943-generate-an-api-token) and
[Retrieve a bearer token](https://help.cerby.com/en/articles/9450993-retrieve-
a-bearer-token).

* * *

# Related articles

The following articles contain more information about how to use the Cerby
Read API:

  * [Explore the API and bearer tokens](https://help.cerby.com/en/articles/9450922-explore-the-api-and-bearer-tokens)

  * [Generate an API token](https://help.cerby.com/en/articles/9450943-generate-an-api-token)

  * [Retrieve a bearer token](https://help.cerby.com/en/articles/9450993-retrieve-a-bearer-token)

  * [Data definitions](https://help.cerby.com/en/articles/9451004-data-definitions)

  * [API endpoints reference](https://help.cerby.com/en/articles/9451123-api-endpoints-reference)


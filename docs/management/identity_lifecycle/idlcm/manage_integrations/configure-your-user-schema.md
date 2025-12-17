---
description: "This article describes how to configure a custom user schema for your IdLCM integration."
intercom_id: 11644390
---

# Configure your user schema

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Owner** , **Super Admin** , or **Admin** , you can configure a custom user schema for your IdLCM integration to connect disconnected apps to Cerby.

Configuring a custom user schema in Cerby ensures that user profiles and access controls are properly aligned with the requirements of each external app. This enables more accurate provisioning and seamless integration with your organization’s identity and access policies.

For each external app available in the app catalog of IdLCM integrations, Cerby provides a default user schema that you can update to perform one of the following actions:

* [Add custom attributes](configure-your-user-schema.md#add-custom-attributes)
* [Add custom roles](configure-your-user-schema.md#add-custom-roles)

The following sections describe each action.

* * *

## Add custom attributes

Cerby supports the definition of custom attributes to extend the default user schema. The goal is to tailor user profiles to your organization's specific requirements by adding fields that are not part of the standard schema.

{% hint style="danger" %}


**IMPORTANT** : When you create a custom attribute for a user schema, you must define the new attributes and its corresponding mapping within your Identity Provider (IdP). For instructions, read the official documentation of your IdP:

  * **Okta:**
    * [Add custom attributes to apps, directories, and identity providers](https://help.okta.com/oie/en-us/content/topics/users-groups-profiles/usgp-add-custom-attribute.htm)
    * [Map app attributes on the Provisioning page](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-map-attributes-provisioning.htm)
​**NOTE:** Okta only supports **urn:ietf:params:scim:schemas:extension:enterprise:2.0:User** namespace for schema extensions.


{% endhint %}

You can define a custom attribute using the following JSON structure:

    attributes: [
            {
                    validator: {
                            type: 'cerby:json-schema',
                            spec: {
                                    type: 'string',
                            },
                    },
                    label: 'CustomField',
                    type: 'cerby:user-schema-attribute',
                    dataClassification: 'plain',
                    allowEmptyInSync: true,
                    primaryIdentifier: false,
                    required: true,
                    returned: 'always',
                    multiValued: false,
            },
    ]

The following table provides a description of each JSON field used for defining a custom user schema attribute:

**Fields**| **Description**| **Type**
---|---|---
**`validator.type`**|  Specifies the validation method used. For Cerby, use **`cerby:json-schema`**|  String
**`validator.spec.type`**|  Defines the data type of the attribute.  | String
**`label`**|  Contains the human-readable name of the attribute.| String
**`type`** | Indicates the constant value **`cerby:user-schema-attribute`**|  String
**`dataClassification`**|  Indicates the sensitivity level of the data. The valid values are the following:

  * **`plain`**
  * **`encrypted`**

|  String
**`allowEmptyInSync`**|  Indicates if the attribute can be empty when syncing user data between systems.| Boolean
**`primaryIdentifier`**|  Indicates if this field serves as a unique identifier for the user.| Boolen
**`required`**|  Indicates if the attributes must be provided when creating or updating a user.| Boolean
**`returned`**|  Indicates when the field is included in responses. The valid values are the following:

  * **`always`**
  * **`never`**
  * **`default`**
  * **`request`**

|  String
**`multiValued`**|  Indicates if the attribute supports multiple values.| Boolean

**Table 1.** Descriptions of the user schema custom attributes fields

* * *

## Add custom roles

Cerby supports the creation of custom roles in the user schema, enabling you to define role attributes that align with how your connected apps manage access. By defining a custom role attribute, you can automatically assign the right role to each user when their account is created or updated.

{% hint style="danger" %}


**IMPORTANT** : After defining custom roles in your IdLCM integrations, you must configure the mapping within your IdP to ensure role information is included correctly during user provisioning. For instructions, read the official documentation of your IdP:

  * **Okta:**
    * [Map app attributes on the Provisioning page](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-map-attributes-provisioning.htm)


{% endhint %}

You can define a custom role using the following JSON structure by adding a new entry to the **`roles.options`** array in the user schema:

    {
            "description": "Custom role",
            "displayName": "Custom Role",
            "incompatibleRoles": [],
            "ranking": 1,
            "type": "cerby:role-option",
            "value": "custom-role"
     },
    ...

The following table provides a description of each JSON field used to define a custom role within the**`roles.options`** array:

**Fields**| **Description**| **Type**
---|---|---
**`description`**|  Describes what the role represents or is used for.| String
**`displayName`**|  Indicates the name of the role as it appears in the UI.| String
**`incompatibleRoles`**|  Defines a list of role values that are not allowed to be assigned with this role.| Array
**`ranking`** | Defines the role prioritization, especially when multiple roles are available| Integer
**`type`**|  Identifies the element as a role option. For Cerby, use **`cerby:role-option`.**| String
**`value`**|  Defines the internal value or ID of the role.| String

**Table 2.** Descriptions of the user schema custom roles fields

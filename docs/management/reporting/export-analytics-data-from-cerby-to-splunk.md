---
description: This article describes how to set up the integration to export analytics data from Cerby to Splunk.
intercom_id: 9663721
---

# Export analytics data from Cerby to Splunk

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* This is a beta feature currently available to a limited number of workspaces


{% endhint %}

With Cerby, you can export the analytics data of your workspace to a security information and event management (SIEM) solution like Splunk via an integration. This is a feature that customers can request to be enabled by the Cerby Customer Support team.

The integration leverages an HTTP Event Collector, where Cerby exports the logs of analytic events in JSON format every minute as long as Cerby has registered events. The [Appendix: Analytic events format](export-analytics-data-from-cerby-to-splunk.md#id-appendix-analytic-events-format) section details the JSON object structure.

{% hint style="info" %}


**NOTE:** Email your request to enable this feature to the Customer Support team at [support@cerby.com](mailto:support@cerby.com). You must also send a URI as part of step [1. Create and set up an HTTP Event Collector in Splunk](export-analytics-data-from-cerby-to-splunk.md#id-1.-create-and-set-up-an-http-event-collector-in-splunk).


{% endhint %}

This article describes how to set up the analytics data export to Splunk.

* * *

## Set up the analytics data export to Splunk

To set up the export of the analytics data that Cerby registers and stores for a workspace, you must complete the following main steps:

  1. [Create and set up an HTTP Event Collector in Splunk](export-analytics-data-from-cerby-to-splunk.md#id-1.-create-and-set-up-an-http-event-collector-in-splunk)
  2. [Search for Cerby analytic events via the Splunk Search app](export-analytics-data-from-cerby-to-splunk.md#id-2.-search-for-cerby-analytic-events-via-the-splunk-search-app)

The following sections describe each main step.

### 1\. Create and set up an HTTP Event Collector in Splunk

To create and configure an HTTP Event Collector in Spunk, complete the following steps:

  1. Create a Splunk HTTP Event Collector for receiving events by following the instructions in the [Getting Data In](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2209/Data/UsetheHTTPEventCollector?ref=hk) official documentation.

  **IMPORTANT:** When creating the Event Collector token, disable the Enable indexer acknowledgement checkbox.

  2. Share the HTTP Event Collector token and URI with the Cerby Customer Support team. The following is an example of the URI: `https://demouri.splunkcloud.com:8088/services/collector/event`.

The Splunk system provides the URI and may contain a port. If applicable, ensure you share the port to prevent issues receiving the events.

**IMPORTANT:** Use a Cerby secure secret instead of sending sensitive details directly. For more information, refer to the articles [Share items with external users via a link](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/share-items-with-external-users-via-a-link) and [[Video] How to share a secret with external users via a public link](https://help.cerby.com/en/articles/8384438-video-how-to-share-a-secret-with-external-users-via-a-public-link) to learn how to share the values securely.

The next step is [2. Search for Cerby events via the Splunk Search app](export-analytics-data-from-cerby-to-splunk.md#id-2.-search-for-cerby-analytic-events-via-the-splunk-search-app).

### 2\. Search for Cerby analytic events via the Splunk Search app

To search for Cerby analytic events using the Splunk Search app, follow the instructions in the [Search Tutorial](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2209/SearchTutorial/Aboutthesearchapp) official documentation.

Now you’re done with the setup.

* * *

## Appendix: Analytic events format

The following is an example of the JSON object with the analytic events that Cerby sends to Splunk. The object contains a description of each key-value pair.

    {
        "timestamp":<Unix timestamp of the event>,
        "date": <event data in ISO format>,
        "eventName": <name of the event>,
        "user_id": <user whose action triggered the event>
        "accountName": <name of the account related to the event, when applicable>,
        "accountProvider": <provider of the account related to the event, when applicable>,
        "city": <event source city>,
        "region": <event source state/region>,
        "country": <event source country>,
        "ip": <event source IP>,
        "deviceName": <device type, for example, Mac, PC, and smartphone>,
        "browserName": <name of the browser>,
        "browserVersionMajor": <browser version>,
        "userAgent": <browser user agent>,
        "workspace": <customer workspace name>
    }

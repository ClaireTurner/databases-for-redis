---
copyright:
  years: 2017,2018
lastupdated: "2018-09-27"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}

# Activity Tracker Integration

{{site.data.keyword.databases-for-redis_full}} is integrated with  [Activity Tracker](https://console.{DomainName}/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov), so you can view service-level events.

In order to see the events, you need to [provision the Activity Tracker service](https://console.{DomainName}/docs/services/cloud-activity-tracker/how-to/provision.html#provision) from the [{{site.data.keyword.cloud_notm}}  catalog](https://console.{DomainName}/catalog/services/activity-tracker). Activity Tracker has a _Lite_ plan available at no additional cost.

Once you have the Activity Tracker service, the {{site.data.keyword.databases-for-redis}} events appear under _Account Logs_ from the _View Logs_ dropdown menu. 

In addition to the Activity Tracker UI, the Kibana dashboard is also available at https://logging.ng.bluemix.net.
{: .tip}

## Event Fields
A description of the common fields for an Activity Tracker event is on the [Activity Tracker event fields](https://console.{DomainName}/docs/services/cloud-activity-tracker/at_event.html#at_event) page.

## List of Events

The table lists the events that get sent to Activity Tracker from {{site.data.keyword.databases-for-redis}}.

Action|Description
-------|-------
`databases-for-redis.backup.create`|A backup of your deployment was created. If the backup failed, a "-failure" flag is included in the message.
`databases-for-redis.user-password.update`|The admin password was updated. A "-failure" flag is included in the message if the attempt to update the password failed.
`databases-for-redis.backup.restore`|A restore from backup was created. If the attempted restore failed, a "-failure" flag is included in the message.
`databases-for-redis.resources.scale`|A scaling operation was performed. If the scaling operation failed, a "-failure" flag is included in the message.
`databases-for-redis.whitelisted-ips-list.update`|The whitelist was modified. A "-failure" flag is included in the message if the attempt to modify the whitelist failed.
{: caption="Table 1. List of Events and Event Descriptions" caption-side="top"}


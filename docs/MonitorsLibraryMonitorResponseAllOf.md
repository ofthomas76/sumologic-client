# MonitorsLibraryMonitorResponseAllOf


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monitor_type** | **str** | The type of monitor. Valid values:   1. &#x60;Logs&#x60;: A logs query monitor.   2. &#x60;Metrics&#x60;: A metrics query monitor. | 
**queries** | [**[MonitorQuery]**](MonitorQuery.md) | All queries from the monitor. | 
**triggers** | [**[TriggerCondition]**](TriggerCondition.md) | Defines the conditions of when to send notifications. | 
**evaluation_delay** | **str** | The delay duration for evaluating the monitor (relative to current time). The timerange of monitor will be shifted in the past by this delay time. | [optional]  if omitted the server will use the default value of "0m"
**notifications** | [**[MonitorNotification]**](MonitorNotification.md) | The notifications the monitor will send when the respective trigger condition is met. | [optional]  if omitted the server will use the default value of []
**is_disabled** | **bool** | Whether or not the monitor is disabled. Disabled monitors will not run, and will not generate or send notifications. | [optional]  if omitted the server will use the default value of False
**status** | **[str]** | The current status of the monitor. Each monitor can have one or more status values. Valid values:   1. &#x60;Normal&#x60;: The monitor is running normally and does not have any currently triggered conditions.   2. &#x60;Critical&#x60;: The Critical trigger condition has been met.   3. &#x60;Warning&#x60;: The Warning trigger condition has been met.   4. &#x60;MissingData&#x60;: The MissingData trigger condition has been met.   5. &#x60;Disabled&#x60;: The monitor has been disabled and is not currently running. | [optional] 
**group_notifications** | **bool** | Whether or not to group notifications for individual items that meet the trigger condition. | [optional]  if omitted the server will use the default value of True
**warnings** | **{str: (str,)}** | Monitor manager warnings | [optional] 
**playbook** | **str** | Notes such as links and instruction to help you resolve alerts triggered by this monitor. {{Markdown}} supported. It will be enabled only if available for your organization. Please contact your Sumo Logic account team to learn more. | [optional]  if omitted the server will use the default value of ""
**any string name** | **bool, date, datetime, dict, float, int, list, str, none_type** | any string name can be used but the value must be the correct type | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


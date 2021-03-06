# Zuora::NotificationHistoryApi

All URIs are relative to *https://rest.zuora.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_callout_history**](NotificationHistoryApi.md#get_callout_history) | **GET** /v1/notification-history/callout | Get callout notification histories
[**get_email_history**](NotificationHistoryApi.md#get_email_history) | **GET** /v1/notification-history/email | Get email notification histories


# **get_callout_history**
> GETCalloutHistoryVOsType get_callout_history(opts)

Get callout notification histories

This REST API reference describes how to get a notification history for callouts. 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::NotificationHistoryApi.new

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  page_size: 20 # Integer | Number of rows returned per page. 
  end_time: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | The final date and time of records to be returned. Defaults to now. Use format yyyy-MM-ddTHH:mm:ss.
  start_time: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | The initial date and time of records to be returned. Defaults to (end time - 1 day). Use format yyyy-MM-ddTHH:mm:ss.
  object_id: "object_id_example", # String | The ID of an object that triggered a callout notification.
  failed_only: true, # BOOLEAN | If `true`, only return failed records. If `false`, return all records in the given date range. The default value is `true`.
  event_category: "event_category_example", # String | Category of records to be returned by event category.
  include_response_content: true # BOOLEAN | 
}

begin
  #Get callout notification histories
  result = api_instance.get_callout_history(opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling NotificationHistoryApi->get_callout_history: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **page_size** | **Integer**| Number of rows returned per page.  | [optional] [default to 20]
 **end_time** | **DateTime**| The final date and time of records to be returned. Defaults to now. Use format yyyy-MM-ddTHH:mm:ss. | [optional] 
 **start_time** | **DateTime**| The initial date and time of records to be returned. Defaults to (end time - 1 day). Use format yyyy-MM-ddTHH:mm:ss. | [optional] 
 **object_id** | **String**| The ID of an object that triggered a callout notification. | [optional] 
 **failed_only** | **BOOLEAN**| If &#x60;true&#x60;, only return failed records. If &#x60;false&#x60;, return all records in the given date range. The default value is &#x60;true&#x60;. | [optional] 
 **event_category** | **String**| Category of records to be returned by event category. | [optional] 
 **include_response_content** | **BOOLEAN**|  | [optional] 

### Return type

[**GETCalloutHistoryVOsType**](GETCalloutHistoryVOsType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **get_email_history**
> GETEmailHistoryVOsType get_email_history(opts)

Get email notification histories

This REST API reference describes how to get a notification history for notification emails.   ## Notes Request parameters and their values may be appended with a \"?\" following the HTTPS GET request.  Additional request parameter are separated by \"&\".   For example:  `GET https://rest.zuora.com/v1/notification-history/email?startTime=2015-01-12T00:00:00&endTime=2015-01-15T00:00:00&failedOnly=false&eventCategory=1000&pageSize=1` 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::NotificationHistoryApi.new

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  page_size: 20 # Integer | Number of rows returned per page. 
  end_time: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | The end date and time of records to be returned. Defaults to now. Use format yyyy-MM-ddTHH:mm:ss. The maximum date range (endTime - startTime) is three days.
  start_time: DateTime.parse("2013-10-20T19:20:30+01:00"), # DateTime | The initial date and time of records to be returned. Defaults to (end time - 1 day). Use format yyyy-MM-ddTHH:mm:ss. The maximum date range (endTime - startTime) is three days.
  object_id: "object_id_example", # String | The Id of an object that triggered an email notification.
  failed_only: true, # BOOLEAN | If `true`, only returns failed records. When `false`, returns all records in the given date range. Defaults to `true` when not specified.
  event_category: "event_category_example" # String | Category of records to be returned by event category.
}

begin
  #Get email notification histories
  result = api_instance.get_email_history(opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling NotificationHistoryApi->get_email_history: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **page_size** | **Integer**| Number of rows returned per page.  | [optional] [default to 20]
 **end_time** | **DateTime**| The end date and time of records to be returned. Defaults to now. Use format yyyy-MM-ddTHH:mm:ss. The maximum date range (endTime - startTime) is three days. | [optional] 
 **start_time** | **DateTime**| The initial date and time of records to be returned. Defaults to (end time - 1 day). Use format yyyy-MM-ddTHH:mm:ss. The maximum date range (endTime - startTime) is three days. | [optional] 
 **object_id** | **String**| The Id of an object that triggered an email notification. | [optional] 
 **failed_only** | **BOOLEAN**| If &#x60;true&#x60;, only returns failed records. When &#x60;false&#x60;, returns all records in the given date range. Defaults to &#x60;true&#x60; when not specified. | [optional] 
 **event_category** | **String**| Category of records to be returned by event category. | [optional] 

### Return type

[**GETEmailHistoryVOsType**](GETEmailHistoryVOsType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8




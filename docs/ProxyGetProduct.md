# Zuora::ProxyGetProduct

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_feature_changes** | **BOOLEAN** |  Controls whether to allow your users to add or remove features while creating or amending a subscription. **Character** **limit**: n/a **Values**: true, false (default)  | [optional] 
**category** | **String** |  Category of the product. Used by Zuora Quotes Guided Product Selector. **Character** **limit**: 100 **Values**: One of the following:  - Base Products - Add On Services - Miscellaneous Products  | [optional] 
**created_by_id** | **String** | The ID of the Zuora user who created the &#x60;Product&#x60; object. **Character limit**: 32 **Values**: automatically generated  | [optional] 
**created_date** | **DateTime** |  The date when the &#x60;Product&#x60; object was created. **Character limit**: n/a **Values**: automatically generated  | [optional] 
**description** | **String** |  A descriptionof the product. **Character limit**: 500 **Values**: a string of 500 characters or fewer  | [optional] 
**effective_end_date** | **Date** | The date when the product expires and can&#39;t be subscribed to anymore, in &#x60;yyyy-mm-dd&#x60; format. **Character limit**: 29  | [optional] 
**effective_start_date** | **Date** | The date when the product becomes available and can be subscribed to, in &#x60;yyyy-mm-dd&#x60; format. **Character limit**: 29  | [optional] 
**id** | **String** | Object identifier. | [optional] 
**name** | **String** | The name of the product. This information is displayed in the product catalog pages in the web-based UI. **Character limit**: 100 **Values**: a string of 100 characters or fewer  | [optional] 
**sku** | **String** | The unique SKU for the product. **Character limit**: 50 **Values**: one of the following:  - leave null for automatic generated - an alphanumeric string of 50 characters or fewer  | [optional] 
**updated_by_id** | **String** | The ID of the last user to update the object. **Character limit**: 32 **Values**: automatically generated  | [optional] 
**updated_date** | **DateTime** | The date when the object was last updated. **Character limit**: 29 **Values**: automatically generated  | [optional] 



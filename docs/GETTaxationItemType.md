# Zuora::GETTaxationItemType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_by_id** | **String** | The ID of the Zuora user who created the taxation item.   | [optional] 
**created_date** | **DateTime** | The date and time when the taxation item was created in the Zuora system, in &#x60;yyyy-mm-dd hh:mm:ss&#x60; format.  | [optional] 
**exempt_amount** | **Float** | The amount of taxes or VAT for which the customer has an exemption.  | [optional] 
**finance_information** | [**GETTaxationItemTypeFinanceInformation**](GETTaxationItemTypeFinanceInformation.md) |  | [optional] 
**id** | **String** | The ID of the taxation item.  | [optional] 
**jurisdiction** | **String** | The jurisdiction that applies the tax or VAT. This value is typically a state, province, county, or city.  | [optional] 
**location_code** | **String** | The identifier for the location based on the value of the &#x60;taxCode&#x60; field.   | [optional] 
**memo_item_id** | **String** | The ID of the credit or debit memo associated with the taxation item.  | [optional] 
**name** | **String** | The name of the taxation item.  | [optional] 
**source_tax_item_id** | **String** | The ID of the taxation item of the invoice, which the credit or debit memo is created from.  | [optional] 
**success** | **BOOLEAN** | Returns &#x60;true&#x60; if the request was processed successfully. | [optional] 
**tax_amount** | **Float** | The amount of the tax applied to the credit or debit memo.  | [optional] 
**tax_code** | **String** | The tax code identifies which tax rules and tax rates to apply to a specific credit or debit memo.  | [optional] 
**tax_code_description** | **String** | The description of the tax code.  | [optional] 
**tax_date** | **Date** | The date when the tax is applied to the credit or debit memo.  | [optional] 
**tax_rate** | **Float** | The tax rate applied to the credit or debit memo.  | [optional] 
**tax_rate_description** | **String** | The description of the tax rate.  | [optional] 
**tax_rate_type** | **String** | The type of the tax rate applied to the credit or debit memo.  | [optional] 
**updated_by_id** | **String** | The ID of the Zuora user who last updated the taxation item.  | [optional] 
**updated_date** | **DateTime** | The date and time when the taxation item was last updated, in &#x60;yyyy-mm-dd hh:mm:ss&#x60; format.   | [optional] 



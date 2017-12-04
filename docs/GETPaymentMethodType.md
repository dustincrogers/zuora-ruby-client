# SwaggerClient::GETPaymentMethodType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**card_holder_info** | [**GETPaymentMethodTypeCardHolderInfo**](GETPaymentMethodTypeCardHolderInfo.md) |  | [optional] 
**card_number** | **String** | Credit or debit card number, 16 characters or less, masked for security purposes.  | [optional] 
**card_type** | **String** | The type of credit card or debit card being billed.  Possible values are: &#x60;Visa&#x60;, &#x60;MasterCard&#x60;, &#x60;AmericanExpress&#x60;, &#x60;Discover&#x60;.  | [optional] 
**default_payment_method** | **BOOLEAN** | Contains true if this is the default payment method for this customer, otherwise false.  | [optional] 
**expiration_month** | **String** | Two-digit expiration month (01 - 12).  | [optional] 
**expiration_year** | **String** | Four-digit expiration year.  | [optional] 
**id** | **String** | Unique ID generated by Zuora when this payment method was created.  | [optional] 


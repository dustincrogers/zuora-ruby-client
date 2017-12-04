# SwaggerClient::PUTSubscriptionResumeType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**apply_credit_balance** | **BOOLEAN** | Applies a credit balance to an invoice.  If the value is &#x60;true&#x60;, the credit balance is applied to the invoice. If the value is &#x60;false&#x60;, no action is taken.   To view the credit balance adjustment, retrieve the details of the invoice using the Get Invoices method.  Prerequisite: &#x60;invoice&#x60; must be &#x60;true&#x60;.   **Note:**    - If you are using the field &#x60;invoiceCollect&#x60; rather than the field &#x60;invoice&#x60;, the &#x60;invoiceCollect&#x60; value must be &#x60;true&#x60;.   - This field is deprecated if you have the Advanced AR Settlement feature enabled.  | [optional] 
**collect** | **BOOLEAN** | Collects an automatic payment for a subscription. The collection generated in this operation is only for this subscription, not for the entire customer account.  If the value is &#x60;true&#x60;, the automatic payment is collected. If the value is &#x60;false&#x60;, no action is taken.  The default value is false.  This field is in Zuora REST API version control. Supported minor versions are 196.0 or later. To use this field in the method, you must set the &#x60;zuora-version&#x60; parameter to the minor version number in the request header.  Prerequisite: &#x60;invoice&#x60; must be &#x60;true&#x60;.  | [optional] 
**contract_effective_date** | **Date** | The date when the customer notifies you that they want to resume their subscription.  | [optional] 
**extends_term** | **BOOLEAN** | Whether to extend the subscription term by the length of time the suspension is in effect.  Values: &#x60;true&#x60;, &#x60;false&#x60;.  | [optional] 
**invoice** | **BOOLEAN** | **Note:** This field has been replaced by the &#x60;runBilling&#x60; field. The &#x60;invoice&#x60; field is only available for backward compatibility.   Creates an invoice for a subscription. The invoice generated in this operation is only for this subscription, not for the entire customer account.   If the value is &#x60;true&#x60;, an invoice is created. If the value is &#x60;false&#x60;, no action is taken. The default value is &#x60;false&#x60;.   This field is in Zuora REST API version control. Supported minor versions are &#x60;196.0&#x60; and &#x60;207.0&#x60;. To use this field in the method, you must set the &#x60;zuora-version&#x60; parameter to the minor version number in the request header.   | [optional] 
**invoice_collect** | **BOOLEAN** | **Note:** This field has been replaced by the &#x60;invoice&#x60; field and the &#x60;collect&#x60; field. &#x60;invoiceCollect&#x60; is available only for backward compatibility.  If &#x60;true&#x60;, an invoice is generated and payment collected automatically during the subscription process. If &#x60;false&#x60; (default), no invoicing or payment takes place.  The invoice generated in this operation is only for this subscription, not for the entire customer account.  This field is in Zuora REST API version control. Supported minor versions are 186.0, 187.0, 188.0, 189.0, and 196.0.  | [optional] 
**invoice_target_date** | **Date** | **Note:** This field has been replaced by the &#x60;targetDate&#x60; field. The &#x60;invoiceTargetDate&#x60; field is only available for backward compatibility.   Date through which to calculate charges if an invoice is generated, as yyyy-mm-dd. Default is current date.   This field is in Zuora REST API version control. Supported minor versions are &#x60;207.0&#x60; and earlier.    | [optional] 
**resume_periods** | **String** | The length of the period used to specify when the subscription is resumed. The subscription resumption takes effect after a specified period based on the suspend date or today&#39;s date. You must use this field together with the &#x60;resumePeriodsType&#x60; field to specify the period.  **Note:** This field is only applicable when the &#x60;suspendPolicy&#x60; field is set to &#x60;FixedPeriodsFromToday&#x60; or &#x60;FixedPeriodsFromSuspendDate&#x60;.  | [optional] 
**resume_periods_type** | **String** | The period type used to define when the subscription resumption takes effect. The subscription resumption takes effect after a specified period based on the suspend date or today&#39;s date. You must use this field together with the &#x60;resumePeriods&#x60; field to specify the period.  Values: &#x60;Day&#x60;, &#x60;Week&#x60;, &#x60;Month&#x60;, &#x60;Year&#x60;  **Note:** This field is only applicable when the &#x60;suspendPolicy&#x60; field is set to &#x60;FixedPeriodsFromToday&#x60; or &#x60;FixedPeriodsFromSuspendDate&#x60;.  | [optional] 
**resume_policy** | **String** | Resume methods. Specify a way to resume a subscription.  Values:  * &#x60;Today&#x60;: The subscription resumption takes effect on today&#39;s date.  * &#x60;FixedPeriodsFromSuspendDate&#x60;: The subscription resumption takes effect after a specified period based on the suspend date. You must specify the &#x60;resumePeriods&#x60; and &#x60;resumePeriodsType&#x60; fields to define the period.  * &#x60;SpecificDate&#x60;: The subscription resumption takes effect on a specific date. You must define the specific date in the &#x60;resumeSpecificDate&#x60; field.  * &#x60;FixedPeriodsFromToday&#x60;: The subscription resumption takes effect after a specified period based on the today&#39;s date. You must specify the &#x60;resumePeriods&#x60; and &#x60;resumePeriodsType&#x60; fields to define the period.  | 
**resume_specific_date** | **Date** | A specific date when the subscription resumption takes effect, in the format yyyy-mm-dd.  **Note:** This field is only applicable only when the &#x60;resumePolicy&#x60; field is set to &#x60;SpecificDate&#x60;.  The value should not be earlier than the subscription suspension date.  | [optional] 
**run_billing** | **BOOLEAN** | Creates an invoice for a subscription. If you have the Advanced AR Settlement feature enabled, a credit memo might also be created based on the [invoice and credit memo generation rule](https://knowledgecenter.zuora.com/CB_Billing/Advanced_AR_Settlement/Credit_and_Debit_Memos/Rules_for_Generating_Invoices_and_Credit_Memos).     The billing documents generated in this operation is only for this subscription, not for the entire customer account.   Possible values:  - &#x60;true&#x60;: An invoice is created. If you have the Advanced AR Settlement feature enabled, a credit memo might also be created.   - &#x60;false&#x60;: No invoice is created.   **Note:** This field is in Zuora REST API version control. Supported minor versions are &#x60;211.0&#x60; or later. To use this field in the method, you must set the &#x60;zuora-version&#x60; parameter to the minor version number in the request header.  | [optional] [default to false]
**target_date** | **Date** | Date through which to calculate charges if an invoice or a credit memo is generated, as yyyy-mm-dd. Default is current date.   **Note:** The credit memo is only available if you have the Avdanced AR Settlement feature enabled.   This field is in Zuora REST API version control. Supported minor versions are &#x60;211.0&#x60; and later. To use this field in the method, you must set the  &#x60;zuora-version&#x60; parameter to the minor version number in the request header.  | [optional] 


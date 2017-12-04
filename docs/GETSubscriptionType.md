# SwaggerClient::GETSubscriptionType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cpq_bundle_json_id__qt** | **String** |  | [optional] 
**opportunity_close_date__qt** | **String** | The closing date of the Opportunity. This field is populated when the subscription originates from Zuora Quotes.  This field is used only for reporting subscription metrics.    | [optional] 
**opportunity_name__qt** | **String** | The unique identifier of the Opportunity. This field is populated when the subscription originates from Zuora Quotes.  This field is used only for reporting subscription metrics.    | [optional] 
**quote_business_type__qt** | **String** | The specific identifier for the type of business transaction the Quote represents such as New, Upsell, Downsell, Renewal, or Churn. This field is populated when the subscription originates from Zuora Quotes.  This field is used only for reporting subscription metrics.    | [optional] 
**quote_number__qt** | **String** | The unique identifier of the Quote. This field is populated when the subscription originates from Zuora Quotes.  This field is used only for reporting subscription metrics.    | [optional] 
**quote_type__qt** | **String** | The Quote type that represents the subscription lifecycle stage such as New, Amendment, Renew or Cancel. This field is populated when the subscription originates from Zuora Quotes.  This field is used only for reporting subscription metrics.    | [optional] 
**account_id** | **String** |  | [optional] 
**account_name** | **String** |  | [optional] 
**account_number** | **String** |  | [optional] 
**auto_renew** | **BOOLEAN** | If &#x60;true&#x60;, the subscription automatically renews at the end of the term. Default is &#x60;false&#x60;.  | [optional] 
**contract_effective_date** | **Date** | Effective contract date for this subscription, as yyyy-mm-dd.  | [optional] 
**contracted_mrr** | **String** | Monthly recurring revenue of the subscription.  | [optional] 
**current_term** | **Integer** | The length of the period for the current subscription term.  | [optional] 
**current_term_period_type** | **String** | The period type for the current subscription term.  Values are:  * &#x60;Month&#x60; (default) * &#x60;Year&#x60; * &#x60;Day&#x60; * &#x60;Week&#x60;  | [optional] 
**custom_field__c** | **String** | Any custom fields defined for this object. The custom field name is case-sensitive.  | [optional] 
**customer_acceptance_date** | **Date** | The date on which the services or products within a subscription have been accepted by the customer, as yyyy-mm-dd.  | [optional] 
**id** | **String** | Subscription ID.  | [optional] 
**initial_term** | **Integer** | The length of the period for the first subscription term.  | [optional] 
**initial_term_period_type** | **String** | The period type for the first subscription term.  Values are:  * &#x60;Month&#x60; (default) * &#x60;Year&#x60; * &#x60;Day&#x60; * &#x60;Week&#x60;  | [optional] 
**invoice_owner_account_id** | **String** |  | [optional] 
**invoice_owner_account_name** | **String** |  | [optional] 
**invoice_owner_account_number** | **String** |  | [optional] 
**invoice_separately** | **String** | Separates a single subscription from other subscriptions and creates an invoice for the subscription.   If the value is &#x60;true&#x60;, the subscription is billed separately from other subscriptions. If the value is &#x60;false&#x60;, the subscription is included with other subscriptions in the account invoice.  | [optional] 
**notes** | **String** | A string of up to 65,535 characters.  | [optional] 
**order_number** | **String** | The order number of the order in which the changes on the subscription are made.   **Note:** This field is only available if you have the [Order Metrics](https://knowledgecenter.zuora.com/BC_Subscription_Management/Orders/Orders_Generation_for_Subscriptions_and_Amendments) feature enabled. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com/). We will investigate your use cases and data before enabling this feature for you.  | [optional] 
**rate_plans** | [**Array&lt;GETSubscriptionRatePlanType&gt;**](GETSubscriptionRatePlanType.md) | Container for rate plans.  | [optional] 
**renewal_setting** | **String** | Specifies whether a termed subscription will remain &#x60;TERMED&#x60; or change to &#x60;EVERGREEN&#x60; when it is renewed.   Values are:  * &#x60;RENEW_WITH_SPECIFIC_TERM&#x60; (default) * &#x60;RENEW_TO_EVERGREEN&#x60;  | [optional] 
**renewal_term** | **Integer** | The length of the period for the subscription renewal term.  | [optional] 
**renewal_term_period_type** | **String** | The period type for the subscription renewal term.  Values are:  * &#x60;Month&#x60; (default) * &#x60;Year&#x60; * &#x60;Day&#x60; * &#x60;Week&#x60;  | [optional] 
**service_activation_date** | **Date** | The date on which the services or products within a subscription have been activated and access has been provided to the customer, as yyyy-mm-dd  | [optional] 
**status** | **String** | Subscription status; possible values are:  * &#x60;Draft&#x60; * &#x60;PendingActivation&#x60; * &#x60;PendingAcceptance&#x60; * &#x60;Active&#x60; * &#x60;Cancelled&#x60; * &#x60;Suspended&#x60; (This value is in Limited Availability.)  | [optional] 
**subscription_number** | **String** |  | [optional] 
**subscription_start_date** | **Date** | Date the subscription becomes effective.  | [optional] 
**term_end_date** | **Date** | Date the subscription term ends. If the subscription is evergreen, this is null or is the cancellation date (if one has been set).  | [optional] 
**term_start_date** | **Date** | Date the subscription term begins. If this is a renewal subscription, this date is different from the subscription start date.  | [optional] 
**term_type** | **String** | Possible values are: &#x60;TERMED&#x60;, &#x60;EVERGREEN&#x60;.  | [optional] 
**total_contracted_value** | **String** | Total contracted value of the subscription.  | [optional] 


# Zuora::BillRunApi

All URIs are relative to *https://rest.zuora.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**object_delete_bill_run**](BillRunApi.md#object_delete_bill_run) | **DELETE** /v1/object/bill-run/{id} | CRUD: Delete Bill Run
[**object_get_bill_run**](BillRunApi.md#object_get_bill_run) | **GET** /v1/object/bill-run/{id} | CRUD: Retrieve Bill Run
[**object_post_bill_run**](BillRunApi.md#object_post_bill_run) | **POST** /v1/object/bill-run | CRUD: Create Bill Run
[**object_put_bill_run**](BillRunApi.md#object_put_bill_run) | **PUT** /v1/object/bill-run/{id} | CRUD: Post or Cancel Bill Run
[**post_email_billing_documentsfrom_bill_run**](BillRunApi.md#post_email_billing_documentsfrom_bill_run) | **POST** /v1/bill-runs/{billRunId}/emails | Email billing documents generated from bill run


# **object_delete_bill_run**
> ProxyDeleteResponse object_delete_bill_run(id, opts)

CRUD: Delete Bill Run

**Note:** This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com).    When deleting a bill run, the logic is the same as when using the UI to delete a bill run. The only required parameter is `BillRunId`. The Status for the bill run must be `Canceled` in order to delete a bill run. 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::BillRunApi.new

id = "id_example" # String | Object id

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #CRUD: Delete Bill Run
  result = api_instance.object_delete_bill_run(id, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling BillRunApi->object_delete_bill_run: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Object id | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**ProxyDeleteResponse**](ProxyDeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **object_get_bill_run**
> ProxyGetBillRun object_get_bill_run(id, opts)

CRUD: Retrieve Bill Run

**Note:** This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com).    Business operations depending on the completion of the bill run will not be available while the bill run query returns `PostInProgress`. Upon completion of the bill run, a query will return `Posted`. 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::BillRunApi.new

id = "id_example" # String | Object id

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  fields: "fields_example" # String | Object fields to return
}

begin
  #CRUD: Retrieve Bill Run
  result = api_instance.object_get_bill_run(id, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling BillRunApi->object_get_bill_run: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Object id | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **fields** | **String**| Object fields to return | [optional] 

### Return type

[**ProxyGetBillRun**](ProxyGetBillRun.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **object_post_bill_run**
> ProxyCreateOrModifyResponse object_post_bill_run(create_request, opts)

CRUD: Create Bill Run

**Note:** This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com).    Creates an ad hoc bill run or a single account or multiple customer accounts.  When creating a single account ad hoc bill run, your request must include `AccountId` and must not include `Batch` or `BillCycleDay`.  

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::BillRunApi.new

create_request = Zuora::ProxyCreateBillRun.new # ProxyCreateBillRun | 

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #CRUD: Create Bill Run
  result = api_instance.object_post_bill_run(create_request, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling BillRunApi->object_post_bill_run: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_request** | [**ProxyCreateBillRun**](ProxyCreateBillRun.md)|  | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**ProxyCreateOrModifyResponse**](ProxyCreateOrModifyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **object_put_bill_run**
> ProxyCreateOrModifyResponse object_put_bill_run(id, modify_request, opts)

CRUD: Post or Cancel Bill Run

**Note:** This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com).    ## Post a Bill Run  Posting a bill run is an asynchronous operation. To post a bill run, the current bill run must have a status of `Completed`.  When a bill run is posted, its status is changed to `PostInProgress`. Once all invoices for this bill run are posted then its status is changed to `Posted`.     When you post a bill run and query the status of a bill run, you will get one of the following results `PostInProgress`, `Completed`, or `Posted`. If all invoices in the bill run are posted, then the status of the bill run is `Posted`. If one or more invoices fail to post, the status will change back to `Completed` and you will need to post the bill run again.  ## Cancel a Bill Run  Canceling a bill run is an asynchronous operation. When canceling a bill run, the logic is the same as when using the UI to cancel a bill run. You need to provide the `BillRunId`, and set the Status to `Canceled`.   When canceling a bill run, consider the following:  * Canceling a bill run with a `Completed` status.   * Only the current bill run will be canceled. * Canceling a bill run with a `Pending` status.   * When canceling an Ad-hoc bill run, only the current bill run will be canceled.   * When canceling a scheduled bill, all scheduled bill runs will be canceled.  The Cancel operation may not be successful. Its success depends on its current business validation. Only a bill run that has no posted invoices can be canceled. If any posted invoices belong to the bill run then an invalid value exception will be thrown with the message, \"The Bill Run cannot be Cancelled, There are Posted invoices.\" 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::BillRunApi.new

id = "id_example" # String | Object id

modify_request = Zuora::ProxyModifyBillRun.new # ProxyModifyBillRun | 

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #CRUD: Post or Cancel Bill Run
  result = api_instance.object_put_bill_run(id, modify_request, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling BillRunApi->object_put_bill_run: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Object id | 
 **modify_request** | [**ProxyModifyBillRun**](ProxyModifyBillRun.md)|  | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**ProxyCreateOrModifyResponse**](ProxyCreateOrModifyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **post_email_billing_documentsfrom_bill_run**
> CommonResponseType post_email_billing_documentsfrom_bill_run(bill_run_id, request, opts)

Email billing documents generated from bill run

Manually emails all the billing documents that are generated from a specified bill run to your customers.    Bill runs can generate invoices and credit memos based on your [invoice and credit memo generation rule](https://knowledgecenter.zuora.com/CB_Billing/Advanced_AR_Settlement/Credit_and_Debit_Memos/Rules_for_Generating_Invoices_and_Credit_Memos). Credit memos are only available if you have the Advanced AR Settlement feature enabled.   Using this API operation, the billing documents are sent to the email addresses specified in the **To Email** field of the email templates. The email template used for each billing document is set in the **Delivery Options** panel of the **Edit notification** dialog from the Zuora UI. See [Edit Email Templates](https://knowledgecenter.zuora.com/CF_Users_and_Administrators/Notifications/Create_Email_Templates) for more information about how to edit the **To Email** field in the email template.      ## Notes   - Even though no field is required in the Request body, you still need to specify `{}` in the request. Otherwise, an error will be returned.     - You can only email posted billing documents.         - You must activate the following notifications before emailing invoices and credit memos:     - **Manual Email For Invoice | Manual Email For Invoice**      - **Email Credit Memo | Manually email Credit Memo**        - To include the invoice PDF in the email, select the **Include Invoice PDF** check box in the **Edit notification** dialog from the Zuora UI. To include the credit memo PDF in the email, select the **Include Credit Memo PDF** check box in the **Edit notification** dialog from the Zuora UI. See [Create and Edit Notifications](https://knowledgecenter.zuora.com/CF_Users_and_Administrators/Notifications/C_Create_Notifications#section_2) for more information.      - Zuora sends the email messages based on the email template you set. You can set the email template to use in the **Delivery Options** panel of the **Edit notification** dialog from the Zuora UI. By default, the following templates are used for billing documents:     - Invoices: **Invoice Posted Default Email Template**     - Credit memos: **Manual Email for Credit Memo Default Template**        See [Create and Edit Email Templates](https://knowledgecenter.zuora.com/CF_Users_and_Administrators/Notifications/Create_Email_Templates) for more information.       

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::BillRunApi.new

bill_run_id = "bill_run_id_example" # String | The ID of the bill run. For example, 2c92c8f95d0c886e015d11287a8f0f8b. 

request = Zuora::POSTEmailBillingDocfromBillRunType.new # POSTEmailBillingDocfromBillRunType | 

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Email billing documents generated from bill run
  result = api_instance.post_email_billing_documentsfrom_bill_run(bill_run_id, request, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling BillRunApi->post_email_billing_documentsfrom_bill_run: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bill_run_id** | **String**| The ID of the bill run. For example, 2c92c8f95d0c886e015d11287a8f0f8b.  | 
 **request** | [**POSTEmailBillingDocfromBillRunType**](POSTEmailBillingDocfromBillRunType.md)|  | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**CommonResponseType**](CommonResponseType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8




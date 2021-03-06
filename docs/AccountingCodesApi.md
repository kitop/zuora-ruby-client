# Zuora::AccountingCodesApi

All URIs are relative to *https://rest.zuora.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_accounting_code**](AccountingCodesApi.md#delete_accounting_code) | **DELETE** /v1/accounting-codes/{ac-id} | Delete accounting code
[**get_accounting_code**](AccountingCodesApi.md#get_accounting_code) | **GET** /v1/accounting-codes/{ac-id} | Query an accounting code
[**get_all_accounting_codes**](AccountingCodesApi.md#get_all_accounting_codes) | **GET** /v1/accounting-codes | Get all accounting codes
[**post_accounting_code**](AccountingCodesApi.md#post_accounting_code) | **POST** /v1/accounting-codes | Create accounting code
[**put_accounting_code**](AccountingCodesApi.md#put_accounting_code) | **PUT** /v1/accounting-codes/{ac-id} | Update an accounting code
[**put_activate_accounting_code**](AccountingCodesApi.md#put_activate_accounting_code) | **PUT** /v1/accounting-codes/{ac-id}/activate | Activate accounting code
[**put_deactivate_accounting_code**](AccountingCodesApi.md#put_deactivate_accounting_code) | **PUT** /v1/accounting-codes/{ac-id}/deactivate | Deactivate accounting code


# **delete_accounting_code**
> CommonResponseType delete_accounting_code(ac_id, opts)

Delete accounting code

This reference describes how to delete an accounting code through the REST API. ## Prerequisites If you have Zuora Finance enabled on your tenant, then you must have the Delete Unused Accounting Code permission. ## Limitations You can only delete accounting codes that have never been associated with any transactions. An accounting code must be deactivated before you can delete it. 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

ac_id = "ac_id_example" # String | ID of the accounting code you want to delete.

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Delete accounting code
  result = api_instance.delete_accounting_code(ac_id, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->delete_accounting_code: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ac_id** | **String**| ID of the accounting code you want to delete. | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**CommonResponseType**](CommonResponseType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **get_accounting_code**
> GETAccountingCodeItemType get_accounting_code(ac_id, opts)

Query an accounting code

This reference describes how to query an accounting code through the REST API.

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

ac_id = "ac_id_example" # String | ID of the accounting code you want to query.

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Query an accounting code
  result = api_instance.get_accounting_code(ac_id, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->get_accounting_code: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ac_id** | **String**| ID of the accounting code you want to query. | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**GETAccountingCodeItemType**](GETAccountingCodeItemType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **get_all_accounting_codes**
> GETAccountingCodesType get_all_accounting_codes(opts)

Get all accounting codes

This reference describes how to query all accounting codes in your chart of accounts through the REST API.

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  page_size: 300 # Integer | Number of rows returned per page. 
}

begin
  #Get all accounting codes
  result = api_instance.get_all_accounting_codes(opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->get_all_accounting_codes: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **page_size** | **Integer**| Number of rows returned per page.  | [optional] [default to 300]

### Return type

[**GETAccountingCodesType**](GETAccountingCodesType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **post_accounting_code**
> POSTAccountingCodeResponseType post_accounting_code(request, opts)

Create accounting code

This reference describes how to create a new accounting code through the REST API.  The accounting code will be active as soon as it has been created.  ## Prerequisites   If you have Zuora Finance enabled on your tenant, you must have the  Configure Accounting Codes permission.  

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

request = Zuora::POSTAccountingCodeType.new # POSTAccountingCodeType | 

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Create accounting code
  result = api_instance.post_accounting_code(request, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->post_accounting_code: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**POSTAccountingCodeType**](POSTAccountingCodeType.md)|  | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**POSTAccountingCodeResponseType**](POSTAccountingCodeResponseType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **put_accounting_code**
> CommonResponseType put_accounting_code(ac_id, request, opts)

Update an accounting code

This reference describes how to update an existing accounting code through the REST API. ## Prerequisites   If you have Zuora Finance enabled on your tenant, you must have the  Manage Accounting Code permission.  ## Limitations You can only update accounting codes that are not already associated with any transactions. 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

ac_id = "ac_id_example" # String | ID of the accounting code you want to update.

request = Zuora::PUTAccountingCodeType.new # PUTAccountingCodeType | 

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Update an accounting code
  result = api_instance.put_accounting_code(ac_id, request, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->put_accounting_code: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ac_id** | **String**| ID of the accounting code you want to update. | 
 **request** | [**PUTAccountingCodeType**](PUTAccountingCodeType.md)|  | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**CommonResponseType**](CommonResponseType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **put_activate_accounting_code**
> CommonResponseType put_activate_accounting_code(ac_id, opts)

Activate accounting code

This reference describes how to activate an accounting code through the REST API.  Prerequisites ------------- If you have Zuora Finance enabled on your tenant, you must have the Manage Accounting Code permission.  

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

ac_id = "ac_id_example" # String | ID of the accounting code you want to activate.

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Activate accounting code
  result = api_instance.put_activate_accounting_code(ac_id, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->put_activate_accounting_code: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ac_id** | **String**| ID of the accounting code you want to activate. | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**CommonResponseType**](CommonResponseType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8



# **put_deactivate_accounting_code**
> CommonResponseType put_deactivate_accounting_code(ac_id, opts)

Deactivate accounting code

This reference describes how to deactivate an accounting code through the REST API.  ## Prerequisites If you have Zuora Finance enabled on your tenant, you must have the Manage Accounting Code permission. ## Limitations You can only deactivate accounting codes that are not associated with any transactions.  You cannot disable accounting codes of type AccountsReceivable. 

### Example
```ruby
# load the gem
require 'zuora'

api_instance = Zuora::AccountingCodesApi.new

ac_id = "ac_id_example" # String | ID of the accounting code you want to deactivate.

opts = { 
  entity_id: "entity_id_example", # String | The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
  entity_name: "entity_name_example" # String | The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name).
}

begin
  #Deactivate accounting code
  result = api_instance.put_deactivate_accounting_code(ac_id, opts)
  p result
rescue Zuora::ApiError => e
  puts "Exception when calling AccountingCodesApi->put_deactivate_accounting_code: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ac_id** | **String**| ID of the accounting code you want to deactivate. | 
 **entity_id** | **String**| The Id of the entity that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 
 **entity_name** | **String**| The [name of the entity](https://knowledgecenter.zuora.com/BB_Introducing_Z_Business/Multi-entity/B_Introduction_to_Entity_and_Entity_Hierarchy#Name_and_Display_Name) that you want to access. Note that you must have permission to access the entity. For more information, see [REST Authentication](https://www.zuora.com/developer/api-reference/#section/Authentication/Entity-Id-and-Entity-Name). | [optional] 

### Return type

[**CommonResponseType**](CommonResponseType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8




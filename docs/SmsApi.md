# Buzi::V1::SmsApi

All URIs are relative to *https://petstore3.swagger.io*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_message**](SmsApi.md#cancel_message) | **POST** /v1/sms/messages/{messageId}/cancel | Cancel a message |
| [**create_message**](SmsApi.md#create_message) | **POST** /v1/sms/messages | Create Message |
| [**create_pricing**](SmsApi.md#create_pricing) | **PUT** /v1/sms/networks/{networkId}/pricing | Create network price |
| [**delete_message**](SmsApi.md#delete_message) | **DELETE** /v1/sms/messages/{messageId} | Deletes a message |
| [**get_message**](SmsApi.md#get_message) | **GET** /v1/sms/messages/{messageId} | Get message |
| [**get_network**](SmsApi.md#get_network) | **GET** /v1/sms/networks/{networkId} | Get network |
| [**get_pricing**](SmsApi.md#get_pricing) | **GET** /v1/sms/networks/{networkId}/pricing | List network rates |
| [**list_messages**](SmsApi.md#list_messages) | **GET** /v1/sms/messages | List messages |
| [**list_networks**](SmsApi.md#list_networks) | **GET** /v1/sms/networks | List networks |
| [**send_message**](SmsApi.md#send_message) | **POST** /v1/sms/messages/{messageId}/send | Sends a message |


## cancel_message

> <Message> cancel_message(message_id)

Cancel a message

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
message_id = 789 # Integer | ID of pet to return

begin
  # Cancel a message
  result = api_instance.cancel_message(message_id)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->cancel_message: #{e}"
end
```

#### Using the cancel_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Message>, Integer, Hash)> cancel_message_with_http_info(message_id)

```ruby
begin
  # Cancel a message
  data, status_code, headers = api_instance.cancel_message_with_http_info(message_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Message>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->cancel_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message_id** | **Integer** | ID of pet to return |  |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_message

> <Message> create_message(create_message_input)

Create Message

Update an existing pet by Id

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
create_message_input = Buzi::V1::CreateMessageInput.new # CreateMessageInput | Update an existent pet in the store

begin
  # Create Message
  result = api_instance.create_message(create_message_input)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->create_message: #{e}"
end
```

#### Using the create_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Message>, Integer, Hash)> create_message_with_http_info(create_message_input)

```ruby
begin
  # Create Message
  data, status_code, headers = api_instance.create_message_with_http_info(create_message_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Message>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->create_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_message_input** | [**CreateMessageInput**](CreateMessageInput.md) | Update an existent pet in the store |  |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_pricing

> <Message> create_pricing(network_id)

Create network price

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
network_id = 56 # Integer | 

begin
  # Create network price
  result = api_instance.create_pricing(network_id)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->create_pricing: #{e}"
end
```

#### Using the create_pricing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Message>, Integer, Hash)> create_pricing_with_http_info(network_id)

```ruby
begin
  # Create network price
  data, status_code, headers = api_instance.create_pricing_with_http_info(network_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Message>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->create_pricing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network_id** | **Integer** |  |  |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_message

> <Error> delete_message(message_id, opts)

Deletes a message

delete a message

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
message_id = 789 # Integer | Pet id to delete
opts = {
  api_key: 'api_key_example' # String | 
}

begin
  # Deletes a message
  result = api_instance.delete_message(message_id, opts)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->delete_message: #{e}"
end
```

#### Using the delete_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Error>, Integer, Hash)> delete_message_with_http_info(message_id, opts)

```ruby
begin
  # Deletes a message
  data, status_code, headers = api_instance.delete_message_with_http_info(message_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Error>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->delete_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message_id** | **Integer** | Pet id to delete |  |
| **api_key** | **String** |  | [optional] |

### Return type

[**Error**](Error.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_message

> <Message> get_message(message_id)

Get message

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
message_id = 789 # Integer | ID of pet to return

begin
  # Get message
  result = api_instance.get_message(message_id)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->get_message: #{e}"
end
```

#### Using the get_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Message>, Integer, Hash)> get_message_with_http_info(message_id)

```ruby
begin
  # Get message
  data, status_code, headers = api_instance.get_message_with_http_info(message_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Message>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->get_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message_id** | **Integer** | ID of pet to return |  |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_network

> <Network> get_network(network_id, opts)

Get network

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
network_id = 56 # Integer | 
opts = {
  country_code: 789 # Integer | ID of pet to return
}

begin
  # Get network
  result = api_instance.get_network(network_id, opts)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->get_network: #{e}"
end
```

#### Using the get_network_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Network>, Integer, Hash)> get_network_with_http_info(network_id, opts)

```ruby
begin
  # Get network
  data, status_code, headers = api_instance.get_network_with_http_info(network_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Network>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->get_network_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network_id** | **Integer** |  |  |
| **country_code** | **Integer** | ID of pet to return | [optional] |

### Return type

[**Network**](Network.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_pricing

> <Array<Pricing>> get_pricing(network_id)

List network rates

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
network_id = 56 # Integer | 

begin
  # List network rates
  result = api_instance.get_pricing(network_id)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->get_pricing: #{e}"
end
```

#### Using the get_pricing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Pricing>>, Integer, Hash)> get_pricing_with_http_info(network_id)

```ruby
begin
  # List network rates
  data, status_code, headers = api_instance.get_pricing_with_http_info(network_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Pricing>>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->get_pricing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network_id** | **Integer** |  |  |

### Return type

[**Array&lt;Pricing&gt;**](Pricing.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_messages

> <Array<Message>> list_messages(opts)

List messages

Update an existing pet by Id

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
opts = {
  inbox: 'inbox_example', # String | 
  status: 'status_example' # String | 
}

begin
  # List messages
  result = api_instance.list_messages(opts)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->list_messages: #{e}"
end
```

#### Using the list_messages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Message>>, Integer, Hash)> list_messages_with_http_info(opts)

```ruby
begin
  # List messages
  data, status_code, headers = api_instance.list_messages_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Message>>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->list_messages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |

### Return type

[**Array&lt;Message&gt;**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_networks

> <Array<Network>> list_networks(opts)

List networks

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
opts = {
  country_code: 'country_code_example' # String | ID of pet to return
}

begin
  # List networks
  result = api_instance.list_networks(opts)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->list_networks: #{e}"
end
```

#### Using the list_networks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Network>>, Integer, Hash)> list_networks_with_http_info(opts)

```ruby
begin
  # List networks
  data, status_code, headers = api_instance.list_networks_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Network>>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->list_networks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **String** | ID of pet to return | [optional] |

### Return type

[**Array&lt;Network&gt;**](Network.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_message

> <Message> send_message(message_id)

Sends a message

Returns a single pet

### Examples

```ruby
require 'time'
require 'buzi-v1'
# setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
message_id = 789 # Integer | ID of pet to return

begin
  # Sends a message
  result = api_instance.send_message(message_id)
  p result
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->send_message: #{e}"
end
```

#### Using the send_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Message>, Integer, Hash)> send_message_with_http_info(message_id)

```ruby
begin
  # Sends a message
  data, status_code, headers = api_instance.send_message_with_http_info(message_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Message>
rescue Buzi::V1::ApiError => e
  puts "Error when calling SmsApi->send_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message_id** | **Integer** | ID of pet to return |  |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


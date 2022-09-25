# buzi-v1

Buzi::V1 - the Ruby gem for the Swagger Petstore - OpenAPI 3.0

This is a sample Pet Store Server based on the OpenAPI 3.0 specification.  You can find out more about
Swagger at [https://swagger.io](https://swagger.io). In the third iteration of the pet store, we've switched to the design first approach!
You can now help us improve the API whether it's by making changes to the definition itself or to the code.
That way, with time, we can improve the API in general, and expose some of the new features in OAS3.

_If you're looking for the Swagger 2.0/OAS 2.0 version of Petstore, then click [here](https://editor.swagger.io/?url=https://petstore.swagger.io/v2/swagger.yaml). Alternatively, you can load via the `Edit > Load Petstore OAS 2.0` menu option!_

Some useful links:
- [The Pet Store repository](https://github.com/swagger-api/swagger-petstore)
- [The source API definition for the Pet Store](https://github.com/swagger-api/swagger-petstore/blob/master/src/main/resources/openapi.yaml)

This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 0.202209251244.0
- Build package: org.openapitools.codegen.languages.RubyClientCodegen

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build buzi-v1.gemspec
```

Then either install the gem locally:

```shell
gem install ./buzi-v1-0.202209251244.0.gem
```

(for development, run `gem install --dev ./buzi-v1-0.202209251244.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'buzi-v1', '~> 0.202209251244.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/buzi-project/buzi-sdk-ruby, then add the following in the Gemfile:

    gem 'buzi-v1', :git => 'https://github.com/buzi-project/buzi-sdk-ruby.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:

```ruby
# Load the gem
require 'buzi-v1'

# Setup authorization
Buzi::V1.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'

  # Configure HTTP basic authorization: BasicAuth
  config.username = 'YOUR_USERNAME'
  config.password = 'YOUR_PASSWORD'

  # Configure Bearer authorization: BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Buzi::V1::SmsApi.new
message_id = 789 # Integer | ID of pet to return

begin
  #Cancel a message
  result = api_instance.cancel_message(message_id)
  p result
rescue Buzi::V1::ApiError => e
  puts "Exception when calling SmsApi->cancel_message: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *https://petstore3.swagger.io*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*Buzi::V1::SmsApi* | [**cancel_message**](docs/SmsApi.md#cancel_message) | **POST** /v1/sms/messages/{messageId}/cancel | Cancel a message
*Buzi::V1::SmsApi* | [**create_message**](docs/SmsApi.md#create_message) | **POST** /v1/sms/messages | Create Message
*Buzi::V1::SmsApi* | [**create_pricing**](docs/SmsApi.md#create_pricing) | **PUT** /v1/sms/networks/{networkId}/pricing | Create network price
*Buzi::V1::SmsApi* | [**delete_message**](docs/SmsApi.md#delete_message) | **DELETE** /v1/sms/messages/{messageId} | Deletes a message
*Buzi::V1::SmsApi* | [**get_message**](docs/SmsApi.md#get_message) | **GET** /v1/sms/messages/{messageId} | Get message
*Buzi::V1::SmsApi* | [**get_network**](docs/SmsApi.md#get_network) | **GET** /v1/sms/networks/{networkId} | Get network
*Buzi::V1::SmsApi* | [**get_pricing**](docs/SmsApi.md#get_pricing) | **GET** /v1/sms/networks/{networkId}/pricing | List network rates
*Buzi::V1::SmsApi* | [**list_messages**](docs/SmsApi.md#list_messages) | **GET** /v1/sms/messages | List messages
*Buzi::V1::SmsApi* | [**list_networks**](docs/SmsApi.md#list_networks) | **GET** /v1/sms/networks | List networks
*Buzi::V1::SmsApi* | [**send_message**](docs/SmsApi.md#send_message) | **POST** /v1/sms/messages/{messageId}/send | Sends a message


## Documentation for Models

 - [Buzi::V1::Cost](docs/Cost.md)
 - [Buzi::V1::CreateMessageInput](docs/CreateMessageInput.md)
 - [Buzi::V1::Error](docs/Error.md)
 - [Buzi::V1::Message](docs/Message.md)
 - [Buzi::V1::Network](docs/Network.md)
 - [Buzi::V1::Pricing](docs/Pricing.md)


## Documentation for Authorization


### ApiKeyAuth


- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header

### BasicAuth

- **Type**: HTTP basic authentication

### BearerAuth

- **Type**: Bearer authentication


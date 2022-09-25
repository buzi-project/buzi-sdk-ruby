# Buzi::V1::CreateMessageInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **to** | **Array&lt;String&gt;** |  | [optional] |
| **from** | **String** |  | [optional] |
| **network_id** | **Integer** |  | [optional] |
| **callback_url** | **String** |  | [optional] |

## Example

```ruby
require 'buzi-v1'

instance = Buzi::V1::CreateMessageInput.new(
  to: null,
  from: null,
  network_id: null,
  callback_url: null
)
```


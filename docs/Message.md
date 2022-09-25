# Buzi::V1::Message

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **status** | **String** |  | [optional] |
| **reason** | **String** |  | [optional] |
| **cost** | [**Cost**](Cost.md) |  | [optional] |
| **inbox** | **String** |  | [optional] |

## Example

```ruby
require 'buzi-v1'

instance = Buzi::V1::Message.new(
  id: null,
  created_at: null,
  status: REJECTED,
  reason: null,
  cost: null,
  inbox: null
)
```


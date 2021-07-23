MessageForUpdate
=======

>Describes a beckn message object for **Update** API call

### Schema Definition


|**Field**|**Type**|**Description**|
|---------|--------|---------------|
|update_target| string | Comma separated values of order objects being updated. For example: "update_target":"item,billing,fulfillment"
|order| [Order](/Core/Latest/02_Schemas/order)  | Describes the details of an order
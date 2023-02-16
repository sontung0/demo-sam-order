# Services

```
order_management
	tables
		orders
			id
			product
			quantity
			amount
			status: new, canceled, completed
			created_at
	events
		order_created
			order: {}
		order_completed
			order: {}
		order_canceled
			order: {}
	apis
		create order
		list orders
		order detail

order_fulfillment
	tables
		order_fulfillments
			id
			order_id
			product
			quantity
			status: pending, fulfilled, out_of_stock
			created_at
	events
		order_fulfillment_fulfilled
			order: {}
		order_fulfillment_out_of_stock
			order: {}
```

# Test payload

```
{
  "product": "iphone",
  "quantity": 3,
  "amount": 3000
}

{
  "order_fulfillment_id": "xxx",
  "status": "fulfilled"
}

{
  "order_fulfillment_id": "xxx",
  "status": "out_of_stock"
}
```
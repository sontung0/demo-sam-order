# Services

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
			product
			quantity
			status: pending, fulfilled, out_of_stock
			created_at
	events
		order_fulfilled
			order: {}
		order_out_of_stock
			order: {}

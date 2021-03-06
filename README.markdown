# mws-rb

This gem is a complete wrapper for Amazon.com's Marketplace Web Service (MWS) API extracted from http://veeqo.com

## Installation

Using with a Gemfile:

    gem 'mws-rb'
    bundle install

Using in a simple ruby file:

    gem install mws-rb
    require 'mws-rb'

## Initialization

```ruby
    mws_api = MWS.new(
      host: "mws-eu.amazonservices.com",
      aws_access_key_id: "Your access key id",
      aws_secret_access_key: "Your secret access key",
      seller_id: "Your seller/merchant id"
    )
```

## Using

To access the apis you can use:

```ruby
     mws_api._api_name_._action_to_calll(params={})
```

Let's say we want to retrieve a list of orders using MWS orders api:

```ruby
    mws_api.orders.list_orders(
      "MarketplaceId.Id.1" => "marketplace id",
      created_after: Time.new(2013, 1, 1)
    )
```

Here is a list of all available APIS:

- mws_api.feeds
- mws_api.orders
- mws_api.reports
- mws_api.products
- mws_api.sellers
- mws_api.recommendations
- mws_api.fulfillment_inventory
- mws_api.fulfillment_inbound_shipment
- mws_api.fulfillment_outbound_shipment

## API docs/actions/params

You can check on the MWS documentation section all actions and params needed:

- http://docs.developer.amazonservices.com/en_US/feeds/index.html
- http://docs.developer.amazonservices.com/en_US/reports/index.html
- http://docs.developer.amazonservices.com/en_US/fba_inbound/index.html
- http://docs.developer.amazonservices.com/en_US/fba_inventory/index.html
- http://docs.developer.amazonservices.com/en_US/fba_outbound/index.html
- http://docs.developer.amazonservices.com/en_US/orders/index.html
- http://docs.developer.amazonservices.com/en_US/products/index.html
- http://docs.developer.amazonservices.com/en_US/recommendations/index.html
- http://docs.developer.amazonservices.com/en_US/sellers/index.html

## TODO

- Complete documentation.

## LICENSE

Copyright (c) Jhimy Fernandes Villar

# Salesforce Commerce on Core Postman Collection

This repository contains a sample Postman collection that you can leverage to place orders using the [Salesforce Commerce on Core APIs](https://developer.salesforce.com/docs/atlas.en-us.chatterapi.meta/chatterapi/connect_resources_commerce.htm).

## :gear: Get started

In order to start with this collection, please follow these steps:

1. Download Postman from the [official website](https://www.postman.com/downloads/) and install it
2. Once installed, open Postman
3. Once opened, import the collection and the environment from this repository to your Postman workspace
4. Once imported, open the `Salesforce Commerce on Core` environment, and modify all the data which contain placeholders (like `<YOUR-CLIENT-ID>`) with your details. Please **don't modify the values with `{{` and `}}`, as these values are calculated values within your Postman environment.**. The environment also contains sample values that you can use, or modify, as per your needs.
5. Once the environment is setup, open the `Salesforce Commerce on Core` collection, and start using it.

## :gear: Where do I find these setup values?

This Postman collection authenticates with the Salesforce instance by using the [OAuth 2.0 Username-Password Flow for Special Scenarios](https://help.salesforce.com/s/articleView?id=sf.remoteaccess_oauth_username_password_flow.htm&type=5). Please refer to this documentation to understand how this works.
As per the documentation, you need to create a [Connected App](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_oauth_and_connected_apps.htm) to be able to use this way of authentication.

### authTokenUrl

If you are using this Postman collection against a sandbox, the `url` environment variable is `https://test.salesforce.com`, else it is `https://login.salesforce.com`. You can also use the url of your instance directly, like `https://[your-domain].my.salesforce.com` if you set up a domain in the org.

### clientId and clientSecret

The `clientId` and `clientSecret` environment variables are the `Consumer Key` and `Consumer Secret` values from the created connected app
In order to get them, please do the following steps:
1. Go to your instance
2. Go to the gear on the top right, and click on `Setup`
3. In the left sidebar, search for `App Manager`
4. Open the connected app you created in the beginning of this chapter
5. Click on the `copy` button to copy the `Consumer Key` and use it as the `clientId` environment variable
5. Click on the `Click to reveal` and `copy` button to copy the `Consumer Secret` and use it as the `clientSecret` environment variable

### username and password

As this Postman collection uses the `OAuth 2.0 Username-Password Flow for Special Scenarios`, it requires your username, password and security token.
Please use the username you use to authenticate against the org as the `username` environment variable, and your password as the `password` environment variable.

### secretToken

As said in the previous section, this collection uses the `OAuth 2.0 Username-Password Flow for Special Scenarios`. This requires you to generate a security token, and use it as the `secretToken` environment variable.
In order to generate it, please do the following steps:
1. Go to your instance
2. Click on your use avatar on the top right and click on `Settings`
3. In the left sidebar, click on `Reset My Security Token`
4. Click on the `Reset My Security Token` button. This will email you with the security token

## :asterisk: Endpoints Covered

#### :card_index_dividers: Clear Collection Variables
1. Clear Collection Variables

#### :key: Auth Salesforce API
1. Auth Salesforce API via Connected App
2. Login Admin
3. Login Buyer

#### :key: Set Webstore Id
1. Query Webstore Id

#### :card_index_dividers: Create Payment Gateway
1. Create Payment Gateway Provider
2. Create Payment Gateway
3. Query Payment Gateway

#### :card_index_dividers: WebStore External Services
##### :card_index_dividers: Inventory
1. Register Inventory External Service
2. Register Inventory Store Integrated Service
3. Get Inventory External Service

##### :card_index_dividers: Shipment
1. Register Shipment External Service
2. Register Shipment Store Integrated Service
3. Get Shipment External Service

##### :card_index_dividers: Tax
1. Register Tax External Service
2. Register Tax Store Integrated Service
3. Get Tax External Service

##### :card_index_dividers: Price
1. Register Price External Service
2. Register Price Store Integrated Service
3. Get Price External Service

##### :card_index_dividers: Payment
1. Register Payment External Service
2. Get Payment External Service

#### :new: :card_index_dividers: Webstore Context
1. Get App Context
2. Get Session Context

#### :card_index_dividers: Webstore Product Import

##### :key: Get Composite Values
1. Get Composite Values

##### :card_index_dividers: Upload CSV
1. base64 encode file
2. Upload Content
3. Retrieve Content Document by ID
4. Retrieve Content Document by Title

##### :card_index_dividers: Import Products
1. Import Product CSV
2. Import Sample Products

#### :card_index_dividers: Webstore Products
1. Get Products
2. Get Product Details

#### :new: :card_index_dividers: Webstore Product Prices
1. Get Product Pricing
2. Get Multiple Products Pricing

#### :card_index_dividers: OMS Products
1. Get Product Details

#### :card_index_dividers: Webstore Cart

##### :card_index_dividers: Query Carts
1. Query Carts by AccountId
2. Query Carts by WebStoreId

##### :card_index_dividers: Get Cart
1. Get Active Cart
2. Get Cart by ID
3. Query Carts

##### :card_index_dividers: Delete Cart
1. Delete Active Cart
2. Delete Cart by ID

##### :card_index_dividers: Create Cart
1. Create a Cart

##### :card_index_dividers: Cart Items
1. Add Item to Cart
2. Add Items to Cart (Batch)
3. Get Cart Items
4. Delete Cart Item
5. Patch Cart Item (**_not yet supported for B2CE_**)

#### :card_index_dividers: Webstore Checkout
##### :card_index_dividers: Checkout - Happy Path
1. Login Admin
2. Get Webstore Id
3. Login Buyer (optional, not needed for OOBO)
4. Delete Active Cart
5. Create a Cart
6. Add Items to Cart
7. Create Checkout
8. Patch Delivery Address
9. Create Payment Token
10. Authorize Payment
11. Cart to Order

##### :heavy_dollar_sign:
1. Create Checkout
2. Patch Delivery Address
3. Get Checkout Status
4. Cancel Checkout
5. Patch Delivery Method
6. Create Payment Token
7. Authorize Payment
8. Cart to Order

##### :card_index_dividers: :new: Guest Cart and Checkout (using cookies, DTC)
1. Login Admin
2. :key: Query Site Id, URL Prefix, Set Site URL
3. :key: Set Collection Variables
4. Get Session Context
5. Create a Guest Cart
6. Get Cart by ID
7. Add Item to Cart
8. Create Checkout
9. Patch Contact Info
10. Patch Delivery Address
11. Create Payment Token
12. Authorize Payment
13. Cart to Order

#### :new: :card_index_dividers: Search Settings

##### :card_index_dividers: Searchable Fields
1. Get Searchable Fields
2. Update Searchable Fields

##### :card_index_dividers: Search Filters
1. Get Search Filters
2. Update Search Filters

##### :card_index_dividers: Search Indexes
1. Get Search Indexes
2. Create Search Index
3. Get Search Index
4. Get Search Index Logs

##### :card_index_dividers: Product Search Settings
1. Get Product Search Settings
2. Update Product Search Settings

##### :card_index_dividers: Sorting Rules
1. Get Sorting Rules
2. :key: Get Custom Field Id
3. Update Sorting Rules

## :rocket: How to?

### How to use the collection?

You can leverage this collection in different ways:

:arrow_forward: By using any endpoint one-by-one. Please remember to always authenticate and fetch your webstore first.

![One Resource screenshot](docs/images/single-request-screenshot.png)

:next_track_button: By using the [Postman Runner](https://learning.postman.com/docs/running-collections/intro-to-collection-runs), which will run a full folder directly, by executing each endpoint one-by-one, sequentially, and report the unit tests results for each executed endpoint.

![Runner animation](docs/images/runner-animation.gif)

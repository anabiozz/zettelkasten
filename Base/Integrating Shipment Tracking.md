Links: [[Logistics]]

Source: https://www.altexsoft.com/blog/shipment-tracking-integration-apis-edis-carriers-aggregators/

What happens from the time an online order is made and then delivered to the customer? It’s shipment – something all parties involved want to track. They want to be well-informed about its movements, how soon it will reach its destination, and whether any delays are expected.

Whether you’re involved in regional, national, or international shipping, you have to learn the ropes of shipment tracking. And in this article, we’ll teach you how to untangle its mysteries.

We’ll describe the main ways to integrate shipment tracking into your system:

-   direct integration with each carrier
-   integration with shipment data aggregators and tech providers
-   integration with shipment providers that connect with multiple carriers

A provider in the last description can also be a freight forwarder that matches your shipment with the most efficient or cost effective carrier, or a [third party logistics provider](https://www.altexsoft.com/blog/business/logistics-management-systems-how-warehouse-transportation-and-distribution-software-work/) (3PL) if you need a full package of logistics services.

The main method to integrate shipment tracking functionality is via an API. Working in the background, a shipping API will pull in data from external servers and display shipping information to you or your customers.

## How shipment tracking works

Once a customer places an order, that’s when the shipment tracking process begins.

First, settle on a carrier. Applying such criteria as sender and addresses, parcel or cargo volume, and transit time should remove inapplicable variants leaving you with the right carriers to choose from. That’s, for example, how the Shippo API retrieves available shipping rates.

![Available rates retrieval via the Shippo API. You can specify a list of carriers to retrieve rates only from them](https://content.altexsoft.com/media/2019/09/word-image-43.png)

_Available rates retrieval via the Shippo API. You can specify a list of carriers to retrieve rates only from them_

After you’ve made the decision, you’ll be able to generate a shipping label from a chosen carrier. A shipping label is a unique ID with all the details related to the ordered item: pickup and destination, buyer and receiver contacts, etc.

At each stop en route, the label is scanned to determine the package’s whereabouts. Stored in the carrier’s tracking system, this data can be retrieved from there via API or another method for data exchange.

Summing up shipment tracking operations, we get the following step-by-step list:

1.  order placement
2.  available rates retrieval
3.  choice of carrier
4.  label generation
5.  locating the parcel by scanning the label
6.  storing data in the carrier’s tracking system
7.  retrieving data via API to enable shipment tracking from a third-party’s side.

Let’s have a look at the major sources of shipment tracking information.

[![Shipment tracking providers](https://content.altexsoft.com/media/2019/09/Shipment-tracking-providers.png)](https://www.altexsoft.com/media/2019/09/Shipment-tracking-providers.png)

_There’s a large variety of options to choose from_

## Shipment platforms and tech providers

There’s a variety of tech providers that connect with different carriers and tracking systems. They can serve as a single source of tracking information from multiple carriers. Connecting to them via API, you can monitor carrier delivery performance and display the corresponding tracking details on your side, whether it’s a tracking module in eCommerce or any other system.

As a rule, the solutions are multi-functional, but our focus is primarily on their tracking features.

### Shippo: ground shipping of containers and parcels

Shippo, a shipping software provider, has a number of out-of-the-box integrations with parcel carriers . It helps integrate shipping with multiple carriers through their [APIs](https://goshippo.com/docs/reference) and web application. Their solution compares carrier rates, generates labels, [validates address](https://goshippo.com/docs/address-validation/), provides [branded tracking pages](https://goshippo.com/docs/tracking/#tracking-pages), and notification emails for customers.

The Shippo [carrier network](https://goshippo.com/carriers/) includes carriers that provide regional, national, and international delivery. Among the carriers there are those who support overnight deliveries – DHL Express, FedEx, UPS, AxleHire, and CDL, to name a few.

[Shippo APIs](https://goshippo.com/docs/reference) perform the following operations:

-   validate address specifying the precision of the returned address
-   prepare international shipping documents
-   provide tracking status
-   refund unused labels
-   set up reverse-logistics and returns

**API connection.** [The Shippo Tracking REST API](https://goshippo.com/docs/tracking/) enables you to track shipments across all the available carriers. The API tracks from labels purchased on Shippo. It can also check the tracking status for shipments created outside of the platform, if provided with the carrier and a tracking number (given that [the carrier is supported](https://goshippo.com/docs/reference#carriers)). Shippo offers full tracking history and fetches live tracking data. You can also set up push notifications from the carrier.

**Conditions.** Shippo offers three [pricing plans](https://goshippo.com/pricing/) with an API accessible for each of them. _Pay As You Go_ plan starts at five cents per every order. _Professional_ plan starts at $10 per month and provides you with five user accounts. _Premier_ plan serves 15 accounts of yours and assists you in tech implementations. As of this writing, the first two were suggesting free trials.

### AfterShip: support of over half thousand carriers

[AfterShip](https://www.aftership.com/) is a Hong Kong startup that tracks shipments and handles returns. AfterShip can be integrated directly with your control panel. It pulls shipment deets into the system and alerts at every step of the transit journey ridding you of redundant customer service inquiries.

Integrating AfterShip RESTful API, you’ll get tracking updates from any [carrier supported by AfterShip](https://docs.aftership.com/api/4/supported-couriers) which now numbers 683 couriers.

**API connection.** Before you get going with the [AfterShip REST API](https://docs.aftership.com/api/4/overview), you have to [create an account](https://accounts.aftership.com/login?audience=analytics.aftershipapi.com&client_id=ebad4444-f01e-4f75-aa83-742553ba10a6&prompt=none&redirect_uri=https%3A%2F%2Fadmin.aftership.com%2Fsso%2Fcallback%2Findex.html&response_type=token&scope=aftership-user&state=8d8997dd-9b56-4259-91ad-4281c88be908) with AfterShip. Then, when you’re logged in, you’ll be able to generate your API key. Once it’s done, you’re all set to request data from AfterShip in JSON string. It’s worth mentioning that AfterShip users note poor documentation on integrating the tracking page and on the API in general.

Prior to tracking, the API matches you with a fitting carrier based on validation of tracking number format and selected couriers. API performs the following tracking manipulations requiring a tracking number to identify a shipment:

-   create/delete/update
-   get tracking results
-   return to the last checkpoint
-   retrack an expired tracking

The API functionality also updates customers on any changes in the tracking status. It can retrieve user contacts, and add or remove them from the tracking number.

![Unified delivery statuses in AfterShip across all the carriers they support](https://content.altexsoft.com/media/2019/09/word-image-45.png)

_Unified delivery statuses in AfterShip across all the carriers they support_

**Conditions.** But keep the limit in mind: _10 requests per second_ from one account. To be on the safe side, AfterShip advises authenticating users to keep limits outside the reach for each of them. Alternatively, you can choose the _Enterprise_ plan with custom API rate limits. As for the other [pricing plans](https://www.aftership.com/pricing), AfterShip has quite an assortment of them. Your choice will depend on the number of trackings you perform monthly. You get access to the API even with a _Forever Free_ plan that allows for 50 trackings.

AfterShip also has a tracking widget called [Track Button](https://www.aftership.com/features/track-button) that you can simply add to your site with a few lines of code. With Track Button on your website, your visitors just have to enter their tracking number to track their shipment.

### Easyship: free API to track shipment with 250+ couriers in five areas

Launched in Hong Kong and later expanded to Singapore, today Easyship is an eCommerce-focused shipping platform that also tracks [couriers](https://www.easyship.com/couriers/usa) in the US, Canada, and Australia. With their [APIs](https://developers.easyship.com/reference#introduction-1), you can integrate Easyship’s real-time shipping rates into your website for free. Easyship has [the Rates API](https://developers.easyship.com/v1.0/reference#request-rates-and-taxes), [the Shipment](https://developers.easyship.com/v1.0/reference#create-a-shipment) and [Label](https://developers.easyship.com/v1.0/reference#confirm-and-buy-labels) APIs, [the Pickup API](https://developers.easyship.com/v1.0/reference#retrieve-available-pick-up-slots), and the Track API which is our primary concern.

**API connection.** [The Track API](https://developers.easyship.com/v1.0/reference#tracking-endpoint) fetches tracking information based on your Platform Order Number or Easyship Shipment ID. The responses give the most recent status update for the shipment as well as a history of all checkpoints.

The list of possible status messages are:

-   Pending Tracking Event
-   Tracking Information Received
-   In Transit to Customer
-   Out For Delivery
-   Delivered
-   Exception
-   Cancelled
-   Pending Refund
-   Cancelled and Refunded.

**Conditions.**To avoid being blocked, stay within the endpoints limit which is 60 requests per minute and 10 requests per second. If you’d like to access Easyship APIs, [become their partner](https://neel56.typeform.com/to/Xodd0Z) first.

### EasyPost: SOAP XML tracking APIs for 100+ carriers

EasyPost is a dedicated supplier of shipping APIs that works with more than 100 carriers worldwide.

**API connection.** Take the first step by [registering an account](https://www.easypost.com/signup) with EasyPost. You can test the EasyPost tracking solution prior to making any decision. SOAP / XML [Carrier Tracking APIs](https://www.easypost.com/carrier-tracking-apis) with tracking, rating, address verification, and insurance features.

For tracking, EasyPost generates a [_Tracker_](https://www.easypost.com/docs/api#trackers) [object](https://www.easypost.com/docs/api#trackers) with all the tracking information related to a package. That’s the case if you purchase shipping labels through EasyPost. Otherwise, you’ll have to create _Tracker_ yourself to enable tracking through the EasyPost API. For that you’ll need to provide a tracking code and the carrier associated with it. The latter is optional and can be auto-detected.

As the package moves along, a _Tracker_ is updated on its whereabouts accordingly. So, the Tracker contains the following info:

-   city, state, country, and zip information about the location where the package was scanned
-   current status of the package (“unknown,” “pre transit,” “in transit,” “out for delivery,” “delivered,” “available for pickup,” “return to sender,” “failure,” “cancelled,” or “error”), as well as previous updates
-   additional deets (service, container type, local delivery day and time) provided by the carrier

**Conditions.** Tracking packages not shipped through EasyPost will cost you one penny per package. If you ship 10K packages a month, EasyPost has [special discounts](https://www.easypost.com/talk-to-easypost?source=Volume%20Discounts) for you.

### Searates: shipping rate search engine with API for container tracking

Searates is a global aggregator of container shipment services that provides container tracking, along with freight and load calculators. The search covers all types of container shipments: less than container load, full container load, and bulk load.

Besides tracking, Searates allows you to generate tracking codes, if you provide your customers with shipment tracking details, and it supports document exchange.

**API connection.** Searates uses [JSON-based API](https://www.searates.com/reference/tracking-api/) for container tracking. You can request your container by sealine ID and container number. In return, you get:

-   Container status
-   Type of transportation (rail, air, sea, truck)
-   Distance from the previous point to this one
-   Geographical location
-   Date
-   Vessel name
-   Tracking ID, etc.

**Conditions.** Contact Searates directly for API use and [payment terms](https://www.searates.com/services/plans/). You can also integrate the service via iFrame for $65 per month. The integration will include all information: from container tracking to reports and statistics.

## Shipment marketplaces and freight forwarders

There are also marketplaces and freight forwarders that specialize in shipment tracking. However, you should expect to use their core services to access tracking APIs. If this works for you, check these two options.

### uShip: shipment marketplace that covers a broad variety of shipments from vehicles to standard freight

uShip is a service provider that connects carriers of any size with shippers. Unlike the businesses we described above, consider uShip a one-stop solution since it only allows you to track shipments that happen over uShip’s portal. This means that your other shipment operations must happen over uShip.

**API connection.** uShip uses [RESTful API](https://developer.uship.com/docs/read/FAQs) for all its operations. In terms of shipment tracking uShip has three shipment statuses:

-   Dispatched
-   Picked up
-   Delivered

Additionally, you can retrieve data on punctuality (e.g. on time, delayed), time of tracking record, and geographical coordinates.

**Conditions.** The API is free to use, but first you must [register as a developer](https://developer.uship.com/docs/read/Home) and directly specify API use conditions with uShip.

### Flexport: interact with freight data using the Flexport APIs

Since 2013, [Flexport](https://www.flexport.com/) has been providing air, ocean, and ground freight forwarding services through their cloud-based platform. They deal with both full-container and less-than-container load shipments, have direct contracts across the major ocean alliances and carriers, provide Private Air Service, and ensure instant access to the information for the carriers to deliver the cargo.

**API connection.** Using [Flexport Shipment REST API](https://apibeta.flexport.com/reference/shipment), you can get the following data:

-   a list of shipments with filtering options (e.g. associated with the given purchase order number)
-   the details of a single shipment:transportation mode, container/freight type, weight and volume, pickup date, estimated/actual arrival date, shipment status, money spent on delivery including customs and duty, origin/destination address, etc.
-   a list of shipment route legs (transportation connection points)
-   a list of containers and their legs

**Conditions.** To access the API, you can generate a key in your [Flexport account](https://app.flexport.com/users/sign_in). Then, include it with every API request in a header. For security purposes, Flexport APIs accept calls only over HTTPS.

## LTL carriers and how to integrate them

If you transport relatively small loads freight, Less-Than-Truckload (LTL) shipping is a resource-effective alternative to both parcel carriers and full-truckload shipping services. Obvious benefits include paying only for the space in a trailer used and pallets-packaged shipments. LTL carriers allow for numerous tracking options, such as a [bill of lading](https://www.altexsoft.com/blog/electronic-bill-of-lading-software/#what-is-an-electronic-bill-of-lading) (BoL), Progressive Rotating Order (PRO), Purchase Order (PO for short), and shipment reference numbers, as well as many others. But unlike the platforms that we described before, these support tracking of their own shipments rather than aggregating multiple carriers.

### YRC Freight – a global player with broad North American coverage

[YRC Freight](https://yrc.com/) is a long-standing carrier of industrial, commercial, and retail goods that focuses on LTL shipping solutions for businesses and supply chain companies. It’s one of the largest YRC Worldwide subsidiaries. Having been a participant in the freight forwarding market since 1924, YRC has broad North American coverage and serves Canada, Mexico, and the United States, including Alaska, Hawaii, Guam, the US Virgin Islands, and Puerto Rico. The company’s portfolio also includes international shipping, logistics, and supply chain services for volume shipments, tradeshow exhibits, cold-sensitive products, and product returns.

**API connection.** YRC Freight’s e-business integration solutions provide [APIs and Web](https://yrc.com/api/) services.

[Tracking API](https://yrc.com/api/) provides shipment information by a reference number or freight bill. Responses are available in HTML or XML. You can request the necessary format when registering.

Tracking Web Service provides a historical list of shipment statuses and allows for identifying the shipments by a PRO or reference number.

**Conditions.** To access all critical LTL shipment tracking, you must [register](http://my.yrc.com/) first and then apply for an API/service.

### New Penn – North American freight carrier with broad functionality

Established in 1931, [New Penn](https://www.newpenn.com/) is now another subsidiary of YRC Worldwide. It focuses on next-day, day-definite, and time-definite LTL and FTL (full truckload) shipping. With over 700 tractors, more than 1500 employees, and in excess of 1500 trailers, New Penn provides services in the northeastern US, Puerto Rico, Ontario, Canada.

**API connection.** In the context of technology integration, New Penn offers web services, which pulls data from the New Penn database. To ensure the data exchange, you’ll have to use SOAP-format APIs. Note that shipment tracking web services allow for specifying only a single PRO number or pickup label number per web service call.

Currently, about 25 shipment statuses are available, including en route, pickup, delivered, scheduled, and many others.

The testing option for web services is also ready for implementation.

More detailed instructions are available in the [documentation](http://reports.newpenn.com/PDFS/NEW_PENN_SHIPMENT_TRACKING_WEB_SERVICE.pdf).

**Conditions.** To access New Penn Web services, you need to

-   register on [the home page](https://www.newpenn.com/);
-   send an email with your user credentials, customer number, and TMS name directly to the [web services team](mailto:WebServices@newpenn.com); and
-   undergo the company verification process.

More details on the registration process and information required can be found in [New Penn Web Services FAQs.](http://reports.newpenn.com/PDFS/webservicefaqs.pdf)

**Shipment tracking URL.** Web page tracking with the link is also available.  It can be used to connect directly to the New Penn relevant response page. For example, you can insert http://newpenn.com/npweb/tracking.txt/process?tracking\_no\_1=56347812, where 56347812 is a PRO or pickup label number. Your web page will replace the last 8 numbers with the tracking number and retrieve the tracking results from the New Penn website.

### XPO Logistics – global business with considerable inventory available

[XPO Logistics](https://www.xpo.com/)  founded in 1989 now serves 30 countries in Western Europe and North America including the continental US as well as Alaska and Hawaii, Puerto Rico, Mexico, and Canada. Focusing on LTL shipment, the company also provides other transportation and supply chain services with its 8,000 tractors, 25,000 trailers, and over 12,000 drivers on board.

**API connection.** [XPO API](https://ltl-solutions.xpo.com/help-center/api/) identifies the current status or shipment history for a particular LTL PRO number and enlists all of the reference numbers related to the PRO number. APIs are available in RESTful format. Testing mode is also accessible.

The API covers about 40 shipment statuses including delayed en route, late, arrived, delivered, picked up, transferred, etc.

The API implementation [guide](https://xpodotcom.azureedge.net/xpo/files/s8/Shipment_Tracking_API_Implementation_Guide.pdf) with detailed description is also available.

**Conditions.** To access to all available API tools, you have to [register](https://ltl.xpo.com/webapp/membership_app/membershipSignupCompanySearch.do) and send an [email](mailto:LTLWebAPISupport@xpo.com) with your web user ID, list of desired REST APIs, and the type of integration method you use. The team will contact you.

### Dayton Freight – a local Midwestern US carrier with extensive vehicle choice

Founded in 1981, Dayton Freight established itself as the US Midwest regional LTL freight carrier. With over 1,500 tractors, about 4,000 trailers, and 5,000 employees on board, Dayton Freight also provides truckload and expedition services.

**API connection.** [Dayton Freight IT Integration Page](https://www.daytonfreight.com/it-integration/) opens access to numerous connection options, including REST APIs\\Web services. All responses are sent in JSON and XML formats.

Within integration, the API tracks shipments:

-   by number (Progress, Purchase Order, Bill of Lading, shipper, and pickup). Rate is limited to 900 calls in 15 min;
-   by date (includes date range and pickup number). Date requests are limited to 31 days with rates limitation to 900 calls per 15 min; and
-   pending shipments (for shipments that haven’t been delivered within 30 days, tracked by account number). Rates are also limited to 900 requests per 15 min.

**Conditions.** To get access to web tools, first [create](http://www.daytonfreight.com/CreateAccount.aspx) a web account and complete the activation process as [described](https://api.daytonfreight.com/public/3/docs). Detailed information on the authentication process is available in the API [documentation](https://api.daytonfreight.com/public/3/docs).

### Roadrunner Freight – a boutique LTL carrier with only-metro destinations

Founded in 1985, [Roadrunner Freight](https://freight.rrts.com/Pages/Home.aspx) established itself as a long-haul LTL carrier in 19 metro-to-metro markets.

**API Connection.** The company provides technology integration options through its [System Integration page](https://freight.rrts.com/_layouts/15/fba/siteLogin.aspx). APIs have RESTful format and all responses are in JSON files. Currently, shipment tracking APIs provide information by PRO, PO, BoL, and pickup numbers. To conduct a search by PO and BoL, authentication is required. GPS tracking position information, if any, is also included in the response. Messages may also contain the activity codes indicating status and/or reason.

**Conditions.** To access web services, first [register](https://freight.rrts.com/_layouts/15/fba/siteLogin.aspx) on the website. Further interaction is thoroughly described in [Tracking Web API Developer’s Guide](https://freight.rrts.com/Help/Documents/RRTS_Tracking_WebService_Developer's_Guide.pdf).  You may also contact the team directly by [email](mailto:servicedesk@rrts.com).

### Central Freight Lines – a seasoned forwarder with the US South destinations

On the freight forwarding scene since 1925, Central Freight Lines is a mature LTL carrier. The company mostly operates for manufacturing, retail, and distribution businesses. Running over 5000 tractors, trailers, and delivery trucks, Central Freight Lines offers coast-to-coast delivery for the southern part of the USA.

**API Connection.** Central Freight provides tools integration via [XML Web Services](http://www.centralfreight.com/website/WebServices.aspx?token=authToken1). Currently, shipment tracking will trace shipment status by PRO, BoL, PO, and original carrier number.

A more detailed implementation process is available in the relevant [documentation](http://www.centralfreight.com/CFLServices/CentralFreightLinesXMLShipmentTrackingWebService.pdf). Requests are responded to with XML files only.

**Conditions.** To access the web services, first [register](http://www.centralfreight.com/website/eCentralSignup.aspx) on eCentral. Further steps of integration and data retrieval are thoroughly described in the documentation for each tool.

## Global cargo carriers and their shipment tracking solutions

You also have cargo carriers. Describing all of them is way beyond the scope of this article, but we’ll mention a few that have decent technology support for tracking your shipments. Keep in mind, that using these APIs and other connectivity solutions also entails that you get data only from these carriers and must source the rest from somewhere else.

### Maersk: shipping solutions from the largest container ship and supply vessel operator

Don’t think of Maersk as only an ocean freight carrier. Besides large vessels and barges, they also provide point-to-point deliveries by truck, and transport high-capacity cargo by rail. There are ocean [prices](https://www.maersk.com/find-a-price/) and rates for inland transportation. In case of oversized cargo, contact Maersk directly to discuss their terms.

[Maersk digital tracking-related solutions](https://www.maersk.com/solutions/digital-solutions) include:

**Web solution.** Once logged into the platform, you can manage your shipping online: find a price, book shipments, submit documents, and track cargo.

[**The Maersk Shipment app**](https://apps.apple.com/us/app/maersk-line/id1163233195?mt=8). This mobile solution has features like instant booking, shipment management, quote requests, scheduling, tracking and sharing transportation plans and container lists

[**Maersk’s Electronic Data Interchange (EDI) suite**](https://www.maersk.com/solutions/digital-solutions/edi-solutions)**.** EDI links Maersk systems to yours, enabling you to manage your shipments from your own system. It empowers faster and easier data exchange like transport and customs documents.

Not sure [what EDI is](https://www.altexsoft.com/blog/business/what-is-edi-understanding-the-main-document-exchange-technology/)? Check our article.

![End-to-end supply chain operations with integrated Maersk’s EDI](https://content.altexsoft.com/media/2019/09/word-image-46.png)

_End-to-end supply chain operations with integrated Maersk’s EDI_

To use any of the above solutions, you have to be [registered](https://www.maersk.com/onboarding) with a Maersk brand (Maersk Line, Safmarine, MCC, Seago Line, or Sealand).

### Bring: shipments to and from the Nordics

With Bring you can deliver parcels, mail, and cargo mainly by road and rail (sea and air transport is available on demand) within the following countries: Norway, Sweden, Denmark, Finland, Holland, Belgium, and the UK. Bring provides local courier services, express and next-day deliveries from the Nordic countries to the rest of the world, and vice versa. Shipping prices depend on many variables: destination and origin countries, urgency, shipment [weight](https://www.bring.no/english/sending), and transport type.

![Price list for mail deliveries from/within Norway](https://content.altexsoft.com/media/2019/09/word-image-47.png)

_Price list for mail deliveries from/within Norway_

[**The Tracking API**](https://developer.bring.com/api/tracking/) facilitates integration of shipment details from their [tracking site](http://tracking.bring.com/tracking/?_ga=2.251726281.1749185671.1569223764-1402466843.1568908361) into your system. Use it to enable tracking based on a tracking number, shipment number, or reference. Besides tracking, Bring APIs can [choose shipping methods](https://developer.bring.com/api/shipping-guide_2/) on checkout, [generate reports](https://developer.bring.com/api/reports/), and [book a shipment](https://developer.bring.com/api/booking/).

### CMA CGM: global carrier with EDI and API integrations

[CMA CGM](https://www.cma-cgm.com/) is a French container shipping company with over 500 vessels.

[**EDI connection**](https://www.cma-cgm.com/products-services/ecommerce/edi-channels). Similar to other large players in the market, the company provides EDI to track containers and get other shipping information, including scheduling, booking confirmation, bill of landing, etc.

**API connection.** Besides EDI, the company offers an API solution. Unfortunately, the documentation isn’t available online, so you must contact CMA CGM directly.

## Top four parcel couriers and their tracking APIs

And, finally, you have parcel carriers. We covered [integration with the most influential parcel carriers](https://www.altexsoft.com/blog/business/how-to-integrate-with-ecommerce-delivery-and-shipment-carriers-dhl-fedex-uk-royal-mail-ups-usps-canada-post-amazon/) in another article. So here we’ll give a brief overview of their shipment tracking solutions only.

### DHL Global Forwarding: access to tracking services via Shipment Tracking and Shipment Status APIs

This global carrier has established its presence in about 220 countries. However, DHL doesn’t handle domestic shipments within the US, since it’s no longer a US company. So they delegate these services to other providers.

[**Shipment tracking API**](https://developer.dhl/api-reference/dgf-shipment-tracking). Using this API, you can request the latest shipment details, as well as all travel history with timestamps. Queries can be made using DHL shipment number, customer’s reference, container number, or master bill number.

[**Shipment Status API.**](https://developer.dhl/api-reference/dgf-shipment-status) If you don’t need all the shipment’s events but only the latest status update – use the Shipment Status API. Besides the most recent whereabouts, its response will also include the package’s origin, destination, count, and weight.

To use DHL APIs, you must have an eligible tracking code for the shipment and an API subscription key.

### FedEx solutions to integrate shipment tracking

FedEx is one of the largest international courier services with operating units spanning air, sea, and road lines. FedEx offers two major solutions to integrate shipment tracking along with other capabilities:

[**FedEx Web Services**](https://www.fedex.com/en-ca/resources-tools/api.html)**.** It’s a white-label solution, so no hosting on your side. It offers FedEx shipping functionality including shipment status tracking that you can integrate directly into your business software system.

[**FedEx Compatible Tier Program**](http://www.fedex.com/ca_english/compatible/)**.** You can [pick a business software solution](https://www.fedex.com/en-ca/compatible/find-a-solution.html) you need – from point-of-sale systems to [warehouse management solutions](https://www.altexsoft.com/blog/warehouse-management-systems/) – with FedEx already integrated to enable shipping functionality.

### UPS Tracking Tools: empower your customers to track their shipments

[United Parcel Service](https://www.ups.com/us/en/Home.page) or UPS operates in 220 countries worldwide. Their primary business is the time-definite delivery of packages and documents. Their position is strong in the US and rates – negotiable. UPS divide their operations into US domestic and international package operations, along with supply chain and freight operations that they have recently included into the service portfolio.

[UPS Developer Kit](https://www.ups.com/upsdeveloperkit?loc=en_US) includes:

**The Tracking API** – provides accurate status on shipments to your customers.

**The Signature Tracking API** – obtains valuable Proof of Delivery information including a digital signature and delivery address.

After you [sign up](https://wwwapps.ups.com/doapp/SignUp?ClientId=GEC&loc=en_US&returnto=https%3A%2F%2Fwww.ups.com%2Fupsdeveloperkit%3Floc=en_US) with UPS and log into the system, you’ll be able to select an API and obtain its documentation. You’ll also need to request a key to access it.

### USPS Web Tools: Tracking/Delivery Confirmation Label APIs

The United States Postal Service has one of the largest civilian fleets and serves as the postal service for the United States. It delivers mail and smaller packages both domestically and internationally. When it comes to packages of less than 13 lbs. (5.8 kg), USPS offers [better rates](https://pe.usps.com/text/imm/immpg.htm) than the other major carriers. At the same time, it lacks the same variety of short-term expedited options.

[**Package Tracking APIs**](https://www.usps.com/business/web-tools-apis/track-and-confirm-api.pdf)**.** They provide delivery status and tracking data. On top of that, you can connect your customers (if you use the data in B2C scenarios) to aUSPS rep to answer questions about their shipment status. The exchange limits is 35 packages per transaction.

You can use USPS APIs for free after [registering for a Web Tools user account](https://www.usps.com/business/web-tools-apis/web-tools-registration.htm). Once you’ve done so, you’ll receive a Web Tools User ID to enable API access.

## Which shipment tracking provider to choose

Before you move on to check a provider’s documentation and contact their agents, we suggest a couple of key takeaways.

**Choose a shipment management solution that supports tracking out of the box.** If you choose off-the-shelf software to manage your shipments, it’s worth checking their tracking options as this service usually comes with other features. And providers like Shippo support API integration if you need to connect tracking info with some other system that you use (e.g. customer portal on the eCommerce platform).

**Start with aggregators and dedicated solutions.** If you need shipment tracking across the widest variety of providers, the best option is to check the key shipment aggregators like AfterShip, Searates, and others. While they work mostly with parcel services, there is also container (freight) shipment tracking.

**Connect to FTL or LTL carriers if you work with a handful of them.** If you’re a small business that cooperates with one or two parcel carriers, you don’t need to integrate third parties for tracking data. Most likely, your carrier already supports tracking. This may be slightly trickier with freight shipments. Many carriers still use EDI exchange and paper-based documentation. It’s always worth contacting a carrier directly to know all the options available.
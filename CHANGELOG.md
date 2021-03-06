# Release 1.1.0 (unreleased)

* Fare_MasterPricerTravelBoardSearch: added new request options (https://github.com/amabnl/amadeus-ws-client/issues/20):
    - Preferred/excluded/... airlines option 'airlineOptions'.
    - Itinerary date: support for Date range +/- 1 day.
    - Itinerary date: Specify date & time of segment as departure or arrival date & time.
    - Itinerary date: deprecated 'date' and 'time' properties, replaced by unified 'dateTime' property.
    - Support for flight options such as direct flight, non-stop flight, etc.
    - Support for Cabin Mode (Mandatory, Major, Recommended) when specifying a cabin code.
    - Support for Fare Options such as Published Fares, Unifares, Electronic/Paper ticketing, ...
    - Support for "Price to beat" feature.
* Implemented Ticket_DisplayTST

# Release 1.0.0 (18 September 2016)

* PNR_AddMultiElements: support for adding OSI elements to a PNR.
* Implemented Ticket_DeleteTST
* Updated docs for 1.0.0 release.
* Released version 1: now following [semantic versioning](http://semver.org/).

# 2016-09

* Implemented SalesReports_DisplayQueryReport
* Implemented Air_MultiAvailability
* Added support for multiple WSDL's (interfaces) in a WSAP (https://github.com/amabnl/amadeus-ws-client/issues/5)
* Fixed a bug while authenticating with SoapHeader 2 (https://github.com/amabnl/amadeus-ws-client/pull/15) - Sergey Gladkovskiy
* PSR-2 code style enforced via StyleCI

# 2016-08

* Implemented PNR_DisplayHistory
* Implemented Fare_InformativePricingWithoutPNR (https://github.com/amabnl/amadeus-ws-client/issues/13)

# 2016-07

* Implemented Air_RetrieveSeatMap

# 2016-06

* Implemented Fare_PricePNRWithBookingClass version 13 and up (https://github.com/amabnl/amadeus-ws-client/issues/6)
* Implemented DocIssuance_IssueTicket (https://github.com/amabnl/amadeus-ws-client/issues/7)
* Implemented Info_EncodeDecodeCity
* Implemented Offer_ConfirmCarOffer
* Implemented checking for response errors for all supported messages _except Command_Cryptic_. For Command_Cryptic, you need to parse the response yourself to check for errors.
* Removed the 'asString' request option - the `Amadeus\Client\Result` object now always contains the result XML in the `responseXml` property.

# 2016-05

Completely re-worked the Result being returned by Web Service calls: the XML or PHP object is now encapsulated in an `Amadeus\Client\Result` object which makes checking for errors or warnings much easier. 

The library now always returns both the PHP object generated by `\SoapClient` as well as the result string. 

The Result object also has a `status` property which contains the status of the message performed: FATAL, OK, WARN or INFO. 

The library will now also convert `\SoapFault` exceptions to a FATAL result status. 

(https://github.com/amabnl/amadeus-ws-client/issues/2)

# 2016-04

* Added support for providing custom `\SoapClient` options (https://github.com/amabnl/amadeus-ws-client/issues/4)
* Implemented Amadeus SoapHeader 2 support (https://github.com/amabnl/amadeus-ws-client/issues/3)
* Changed all references 'tatoo' to 'tattoo' for consistency (https://github.com/amabnl/amadeus-ws-client/issues/1)

# UNSTABLE

The library's API will be unstable until we release the first version.

---
slug: downloading-orders-from-ebay
redirect_from: "/article/214-downloading-orders-from-ebay"
title: Export Orders from eBay
---
This task will export order information from eBay in XML format. The results can be filtered by Order ID if required. See the Examples section for a for sample output file.

## Settings
### Connection
_Required_  
The eBay connection to use. See the [Connecting to eBay](connecting-to-ebay) article if you require more information on how to create/manage connections.

### Export Date
_Required_  
The initial date to export orders from. Any orders placed before this date will not be exported, even if they have been modified.

### Export From
_Required_  
The date to export new/modified orders from. This will update automatically each time the task runs. Note that the task will export a maximum of 30 days worth of orders at a time.

### Include Item Specifics
_Required_  
Allows you to export extended information about the items sold on the order, e.g. MPN Identifier. Defaults to False.

### Order ID
_Optional_  
Allows you to specify a specific order to export. If an Order ID is provided, it will override the Export Date and Export From settings.

### Output File
_Required_  
The file to export orders to.

### Zynk Settings
See [Common Task Settings](common-task-settings).

## Examples
You can find an example of how to use this task in the [eBay to Sage 50 Integration](ebay-to-sage-to-uk-integration) article.

Sample output file:
```xml
<?xml version="1.0" encoding="utf-8"?>
<GetOrdersResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <Timestamp xmlns="urn:ebay:apis:eBLBaseComponents">2011-04-19T15:10:04.869Z</Timestamp>
    <Ack xmlns="urn:ebay:apis:eBLBaseComponents">Success</Ack>
    <Version xmlns="urn:ebay:apis:eBLBaseComponents">715</Version>
    <Build xmlns="urn:ebay:apis:eBLBaseComponents">E715_INTL_BUNDLED_13003939_R1</Build>
    <OrderArray xmlns="urn:ebay:apis:eBLBaseComponents">
        <Order>
            <OrderID>83658149016</OrderID>
            <OrderStatus>Completed</OrderStatus>
            <AdjustmentAmount currencyID="GBP">0</AdjustmentAmount>
            <AmountPaid currencyID="GBP">7.53</AmountPaid>
            <AmountSaved currencyID="GBP">0</AmountSaved>
            <CheckoutStatus>
                <eBayPaymentStatus>NoPaymentFailure</eBayPaymentStatus>
                <LastModifiedTime>2011-04-08T16:17:14Z</LastModifiedTime>
                <PaymentMethod>PayPal</PaymentMethod>
                <Status>Complete</Status>
                <IntegratedMerchantCreditCardEnabled>false</IntegratedMerchantCreditCardEnabled>
            </CheckoutStatus>
            <ShippingDetails>
                <SalesTax>
                    <SalesTaxPercent>0</SalesTaxPercent>
                    <SalesTaxState />
                    <ShippingIncludedInTax>false</ShippingIncludedInTax>
                    <SalesTaxAmount currencyID="GBP">0</SalesTaxAmount>
                </SalesTax>
                <ShippingServiceOptions>
                    <ShippingService>UK_RoyalMailFirstClassStandard</ShippingService>
                    <ShippingServiceCost currencyID="GBP">2.28</ShippingServiceCost>
                    <ShippingServicePriority>1</ShippingServicePriority>
                    <ExpeditedService>false</ExpeditedService>
                    <ShippingTimeMin>1</ShippingTimeMin>
                    <ShippingTimeMax>2</ShippingTimeMax>
                </ShippingServiceOptions>
                <SellingManagerSalesRecordNumber>143122</SellingManagerSalesRecordNumber>
                <GetItFast>false</GetItFast>
            </ShippingDetails>
            <CreatingUserRole>Seller</CreatingUserRole>
            <CreatedTime>2011-04-08T13:14:10Z</CreatedTime>
            <PaymentMethods>CCAccepted</PaymentMethods>
            <PaymentMethods>MOCC</PaymentMethods>
            <PaymentMethods>PayPal</PaymentMethods>
            <ShippingAddress>
                <Name>Billy Piper</Name>
                <Street1>29 Barnes Road</Street1>
                <Street2 />
                <CityName>Bishops Stortford</CityName>
                <StateOrProvince>Hertfordshire</StateOrProvince>
                <Country>GB</Country>
                <CountryName>United Kingdom</CountryName>
                <Phone />
                <PostalCode>CM32 2RR</PostalCode>
                <AddressID>12349283</AddressID>
                <AddressOwner>eBay</AddressOwner>
                <ExternalAddressID />
            </ShippingAddress>
            <ShippingServiceSelected>
                <ShippingService>UK_RoyalMailFirstClassStandard</ShippingService>
                <ShippingServiceCost currencyID="GBP">2.28</ShippingServiceCost>
            </ShippingServiceSelected>
            <Subtotal currencyID="GBP">5.25</Subtotal>
            <Total currencyID="GBP">7.53</Total>
            <TransactionArray>
                <Transaction>
                    <Buyer>
                        <Email>buyer@example.com</Email>
                    </Buyer>
                    <ShippingDetails>
                        <SellingManagerSalesRecordNumber>545078</SellingManagerSalesRecordNumber>
                    </ShippingDetails>
                    <Item>
                        <AutoPay>false</AutoPay>
                        <BuyerProtection>ItemEligible</BuyerProtection>
                        <BuyItNowPrice currencyID="GBP">0</BuyItNowPrice>
                        <Country>GB</Country>
                        <Currency>GBP</Currency>
                        <GiftIcon>0</GiftIcon>
                        <HitCounter>RetroStyle</HitCounter>
                        <ItemID>390234234873</ItemID>
                        <ListingDetails>
                            <Adult>false</Adult>
                            <BindingAuction>false</BindingAuction>
                            <CheckoutEnabled>true</CheckoutEnabled>
                            <ConvertedBuyItNowPrice currencyID="GBP">0</ConvertedBuyItNowPrice>
                            <ConvertedStartPrice currencyID="GBP">1.75</ConvertedStartPrice>
                            <ConvertedReservePrice currencyID="GBP">0</ConvertedReservePrice>
                            <HasReservePrice>false</HasReservePrice>
                            <StartTime>2011-03-12T19:55:05Z</StartTime>
                            <EndTime>2011-04-11T19:55:05Z</EndTime>
                            <ViewItemURL>http://cgi.ebay.co.uk/ws/eBayISAPI.dll?ViewItem&item=390234234873&category=82248</ViewItemURL>
                            <HasUnansweredQuestions>false</HasUnansweredQuestions>
                            <HasPublicMessages>false</HasPublicMessages>
                            <ViewItemURLForNaturalSearch>http://cgi.ebay.co.uk/IPHONE-4G-16GB-WITH-BOX_W0QQitemZ3902994873QQcategoryZ82248QQcmdZViewItem</ViewItemURLForNaturalSearch>
                        </ListingDetails>
                        <ListingDuration>Days_30</ListingDuration>
                        <ListingType>StoresFixedPrice</ListingType>
                        <Location>Newcastle</Location>
                        <PaymentMethods>MOCC</PaymentMethods>
                        <PaymentMethods>PayPal</PaymentMethods>
                        <PaymentMethods>CCAccepted</PaymentMethods>
                        <PayPalEmailAddress>seller@example.com</PayPalEmailAddress>
                        <PrimaryCategory>
                            <CategoryID>82248</CategoryID>
                            <CategoryName>Home & Garden:Garden &</CategoryName>
                        </PrimaryCategory>
                        <PrivateListing>false</PrivateListing>
                        <Quantity>337</Quantity>
                        <ReservePrice currencyID="GBP">0</ReservePrice>
                        <ReviseStatus>
                            <ItemRevised>true</ItemRevised>
                        </ReviseStatus>
                        <Seller>
                            <AboutMePage>false</AboutMePage>
                            <Email>seller@example.com</Email>
                            <FeedbackScore>87634</FeedbackScore>
                            <PositiveFeedbackPercent>99.9</PositiveFeedbackPercent>
                            <FeedbackPrivate>false</FeedbackPrivate>
                            <FeedbackRatingStar>PurpleShooting</FeedbackRatingStar>
                            <IDVerified>false</IDVerified>
                            <eBayGoodStanding>true</eBayGoodStanding>
                            <NewUser>false</NewUser>
                            <RegistrationDate>2002-12-14T16:35:06Z</RegistrationDate>
                            <Site>UK</Site>
                            <Status>Confirmed</Status>
                            <UserID>example-ebay-user</UserID>
                            <UserIDChanged>false</UserIDChanged>
                            <UserIDLastChanged>2006-08-31T14:33:47Z</UserIDLastChanged>
                            <VATStatus>VATExempt</VATStatus>
                            <SellerInfo>
                                <AllowPaymentEdit>false</AllowPaymentEdit>
                                <CheckoutEnabled>true</CheckoutEnabled>
                                <CIPBankAccountStored>false</CIPBankAccountStored>
                                <GoodStanding>true</GoodStanding>
                                <MerchandizingPref>OptIn</MerchandizingPref>
                                <QualifiesForB2BVAT>false</QualifiesForB2BVAT>
                                <StoreOwner>true</StoreOwner>
                                <StoreURL>http://www.stores.ebay.co.uk/id=12348789</StoreURL>
                                <SellerBusinessType>Commercial</SellerBusinessType>
                                <SafePaymentExempt>true</SafePaymentExempt>
                                <TopRatedSeller>true</TopRatedSeller>
                                <LiveAuctionAuthorized>false</LiveAuctionAuthorized>
                            </SellerInfo>
                            <MotorsDealer>false</MotorsDealer>
                        </Seller>
                        <SellingStatus>
                            <BidCount>0</BidCount>
                            <BidIncrement currencyID="GBP">0</BidIncrement>
                            <ConvertedCurrentPrice currencyID="GBP">1.75</ConvertedCurrentPrice>
                            <CurrentPrice currencyID="GBP">1.75</CurrentPrice>
                            <LeadCount>0</LeadCount>
                            <MinimumToBid currencyID="GBP">1.75</MinimumToBid>
                            <QuantitySold>36</QuantitySold>
                            <ReserveMet>true</ReserveMet>
                            <SecondChanceEligible>false</SecondChanceEligible>
                            <ListingStatus>Completed</ListingStatus>
                        </SellingStatus>
                        <ShippingDetails>
                            <ApplyShippingDiscount>false</ApplyShippingDiscount>
                            <SalesTax>
                                <SalesTaxPercent>0</SalesTaxPercent>
                                <ShippingIncludedInTax>false</ShippingIncludedInTax>
                            </SalesTax>
                            <ShippingServiceOptions>
                                <ShippingService>UK_RoyalMailFirstClassStandard</ShippingService>
                                <ShippingServiceCost currencyID="GBP">1.12</ShippingServiceCost>
                                <ShippingServiceAdditionalCost currencyID="GBP">0.58</ShippingServiceAdditionalCost>
                                <ShippingServicePriority>1</ShippingServicePriority>
                                <ExpeditedService>false</ExpeditedService>
                                <ShippingTimeMin>1</ShippingTimeMin>
                                <ShippingTimeMax>2</ShippingTimeMax>
                            </ShippingServiceOptions>
                            <InternationalShippingServiceOption>
                                <ShippingService>UK_RoyalMailInternationalSignedFor</ShippingService>
                                <ShippingServiceCost currencyID="GBP">5.5</ShippingServiceCost>
                                <ShippingServiceAdditionalCost currencyID="GBP">1</ShippingServiceAdditionalCost>
                                <ShippingServicePriority>1</ShippingServicePriority>
                                <ShipToLocation>Worldwide</ShipToLocation>
                            </InternationalShippingServiceOption>
                            <ShippingType>Flat</ShippingType>
                            <ThirdPartyCheckout>false</ThirdPartyCheckout>
                            <SellerExcludeShipToLocationsPreference>false</SellerExcludeShipToLocationsPreference>
                        </ShippingDetails>
                        <ShipToLocations>Worldwide</ShipToLocations>
                        <Site>UK</Site>
                        <StartPrice currencyID="GBP">1.75</StartPrice>
                        <Storefront>
                            <StoreCategoryID>4</StoreCategoryID>
                            <StoreCategory2ID>18</StoreCategory2ID>
                            <StoreURL>http://www.stores.ebay.co.uk/id=987654321</StoreURL>
                        </Storefront>
                        <TimeLeft>PT0S</TimeLeft>
                        <Title>APPLE IPHONE 4G 16GB WITH BOX</Title>
                        <HitCount>146</HitCount>
                        <GetItFast>false</GetItFast>
                        <SKU>3011</SKU>
                        <PostalCode>WR6 5LT</PostalCode>
                        <PictureDetails>
                            <GalleryType>Plus</GalleryType>
                            <GalleryURL>http://i.ebayimg.com/10/!C!Vcd9QBWk~$(KGrHqV,!hMEzsdfdfedEpD6ffdfPBNCjQDUrM!~~_1.JPG?set_id=88021000500F</GalleryURL>
                            <PhotoDisplay>PicturePack</PhotoDisplay>
                            <PictureURL>http://i.ebayimg.com/10/!C!Vcd9QBWk~$(KGrHqV,!hMEzedEpD62312asdPBNCjQDUrM!~~_1.JPG?set_id=88002300500F</PictureURL>
                        </PictureDetails>
                        <DispatchTimeMax>1</DispatchTimeMax>
                        <ProxyItem>false</ProxyItem>
                        <BusinessSellerDetails>
                            <Address>
                                <Street1>Example Sellter,</Street1>
                                <Street2>Rosewood Lane,</Street2>
                                <CityName>Corbridge</CityName>
                                <StateOrProvince>Tyne and Wear</StateOrProvince>
                                <CountryName>United Kingdom</CountryName>
                                <Phone>0191 123 6547</Phone>
                                <PostalCode>NE38 3DL</PostalCode>
                                <CompanyName>Example Seller Ltd</CompanyName>
                                <FirstName>Sales</FirstName>
                                <LastName>Dept</LastName>
                            </Address>
                            <Fax>0191 456 7878</Fax>
                            <Email>sales@example.com</Email>
                            <LegalInvoice>true</LegalInvoice>
                            <TermsAndConditions>Cheque payments; Please allow 10 working days for cheque clearance.</TermsAndConditions>
                            <VATDetails>
                                <VATSite>GB</VATSite>
                                <VATID>229222229</VATID>
                            </VATDetails>
                        </BusinessSellerDetails>
                        <BuyerGuaranteePrice currencyID="GBP">10000</BuyerGuaranteePrice>
                        <BuyerRequirementDetails>
                            <MinimumFeedbackScore>-1</MinimumFeedbackScore>
                            <MaximumUnpaidItemStrikesInfo>
                                <Count>2</Count>
                                <Period>Days_30</Period>
                            </MaximumUnpaidItemStrikesInfo>
                        </BuyerRequirementDetails>
                        <ReturnPolicy>
                            <ReturnsAcceptedOption>ReturnsAccepted</ReturnsAcceptedOption>
                            <ReturnsAccepted>Returns Accepted</ReturnsAccepted>
                            <Description>Faulty/Damaged items must be reported to us within 7 days of receipt..</Description>
                        </ReturnPolicy>
                        <ConditionID>1000</ConditionID>
                        <ConditionDisplayName>New</ConditionDisplayName>
                    </Item>
                    <QuantityPurchased>1</QuantityPurchased>
                    <Status>
                        <PaymentHoldStatus>None</PaymentHoldStatus>
                    </Status>
                    <TransactionID>1521921232150026</TransactionID>
                    <TransactionPrice currencyID="GBP">1.75</TransactionPrice>
                    <SellingManagerProductDetails>
                        <ProductName>APPLE IPHONE 4G 16GB WITH BOX</ProductName>
                        <CustomLabel>3011</CustomLabel>
                    </SellingManagerProductDetails>
                    <Platform>eBay</Platform>
                    <Variation />
                    <OrderLineItemID>3902873-1521950026</OrderLineItemID>
                </Transaction>
                <Transaction>
                    <Buyer>
                        <Email>buyer@example.com</Email>
                    </Buyer>
                    <ShippingDetails>
                        <SellingManagerSalesRecordNumber>198780</SellingManagerSalesRecordNumber>
                    </ShippingDetails>
                    <Item>
                        <AutoPay>false</AutoPay>
                        <BuyerProtection>ItemEligible</BuyerProtection>
                        <BuyItNowPrice currencyID="GBP">0</BuyItNowPrice>
                        <Country>GB</Country>
                        <Currency>GBP</Currency>
                        <GiftIcon>0</GiftIcon>
                        <HitCounter>RetroStyle</HitCounter>
                        <ItemID>39026578873</ItemID>
                        <ListingDetails>
                            <Adult>false</Adult>
                            <BindingAuction>false</BindingAuction>
                            <CheckoutEnabled>true</CheckoutEnabled>
                            <ConvertedBuyItNowPrice currencyID="GBP">0</ConvertedBuyItNowPrice>
                            <ConvertedStartPrice currencyID="GBP">1.75</ConvertedStartPrice>
                            <ConvertedReservePrice currencyID="GBP">0</ConvertedReservePrice>
                            <HasReservePrice>false</HasReservePrice>
                            <StartTime>2011-03-12T19:55:05Z</StartTime>
                            <EndTime>2011-04-11T19:55:05Z</EndTime>
                            <ViewItemURL>http://cgi.ebay.co.uk/ws/eBayISAPI.dll?ViewItem&item=390265474873&category=82248</ViewItemURL>
                            <HasUnansweredQuestions>false</HasUnansweredQuestions>
                            <HasPublicMessages>false</HasPublicMessages>
                            <ViewItemURLForNaturalSearch>http://cgi.ebay.co.uk/IPHONE-4G-16GB-WITH-BOX_itemZ390296894873QQcategoryZ82248QQcmdZViewItem</ViewItemURLForNaturalSearch>
                        </ListingDetails>
                        <ListingDuration>Days_30</ListingDuration>
                        <ListingType>StoresFixedPrice</ListingType>
                        <Location>Newcastle</Location>
                        <PaymentMethods>MOCC</PaymentMethods>
                        <PaymentMethods>PayPal</PaymentMethods>
                        <PaymentMethods>CCAccepted</PaymentMethods>
                        <PayPalEmailAddress>seller@example.com</PayPalEmailAddress>
                        <PrimaryCategory>
                            <CategoryID>82248</CategoryID>
                            <CategoryName>Home & Garden</CategoryName>
                        </PrimaryCategory>
                        <PrivateListing>false</PrivateListing>
                        <Quantity>127</Quantity>
                        <ReservePrice currencyID="GBP">0</ReservePrice>
                        <ReviseStatus>
                            <ItemRevised>true</ItemRevised>
                        </ReviseStatus>
                        <Seller>
                            <AboutMePage>false</AboutMePage>
                            <Email>sales@example.com</Email>
                            <FeedbackScore>87634</FeedbackScore>
                            <PositiveFeedbackPercent>99.9</PositiveFeedbackPercent>
                            <FeedbackPrivate>false</FeedbackPrivate>
                            <FeedbackRatingStar>PurpleShooting</FeedbackRatingStar>
                            <IDVerified>false</IDVerified>
                            <eBayGoodStanding>true</eBayGoodStanding>
                            <NewUser>false</NewUser>
                            <RegistrationDate>2002-12-14T16:35:06Z</RegistrationDate>
                            <Site>UK</Site>
                            <Status>Confirmed</Status>
                            <UserID>example-seller</UserID>
                            <UserIDChanged>false</UserIDChanged>
                            <UserIDLastChanged>2006-08-31T14:33:47Z</UserIDLastChanged>
                            <VATStatus>VATExempt</VATStatus>
                            <SellerInfo>
                                <AllowPaymentEdit>false</AllowPaymentEdit>
                                <CheckoutEnabled>true</CheckoutEnabled>
                                <CIPBankAccountStored>false</CIPBankAccountStored>
                                <GoodStanding>true</GoodStanding>
                                <MerchandizingPref>OptIn</MerchandizingPref>
                                <QualifiesForB2BVAT>false</QualifiesForB2BVAT>
                                <StoreOwner>true</StoreOwner>
                                <StoreURL>http://www.stores.ebay.co.uk/id=6543412</StoreURL>
                                <SellerBusinessType>Commercial</SellerBusinessType>
                                <SafePaymentExempt>true</SafePaymentExempt>
                                <TopRatedSeller>true</TopRatedSeller>
                                <LiveAuctionAuthorized>false</LiveAuctionAuthorized>
                            </SellerInfo>
                            <MotorsDealer>false</MotorsDealer>
                        </Seller>
                        <SellingStatus>
                            <BidCount>0</BidCount>
                            <BidIncrement currencyID="GBP">0</BidIncrement>
                            <ConvertedCurrentPrice currencyID="GBP">1.75</ConvertedCurrentPrice>
                            <CurrentPrice currencyID="GBP">1.75</CurrentPrice>
                            <LeadCount>0</LeadCount>
                            <MinimumToBid currencyID="GBP">1.75</MinimumToBid>
                            <QuantitySold>12</QuantitySold>
                            <ReserveMet>true</ReserveMet>
                            <SecondChanceEligible>false</SecondChanceEligible>
                            <ListingStatus>Completed</ListingStatus>
                        </SellingStatus>
                        <ShippingDetails>
                            <ApplyShippingDiscount>false</ApplyShippingDiscount>
                            <SalesTax>
                                <SalesTaxPercent>0</SalesTaxPercent>
                                <ShippingIncludedInTax>false</ShippingIncludedInTax>
                            </SalesTax>
                            <ShippingServiceOptions>
                                <ShippingService>UK_RoyalMailFirstClassStandard</ShippingService>
                                <ShippingServiceCost currencyID="GBP">1.12</ShippingServiceCost>
                                <ShippingServiceAdditionalCost currencyID="GBP">0.58</ShippingServiceAdditionalCost>
                                <ShippingServicePriority>1</ShippingServicePriority>
                                <ExpeditedService>false</ExpeditedService>
                                <ShippingTimeMin>1</ShippingTimeMin>
                                <ShippingTimeMax>2</ShippingTimeMax>
                            </ShippingServiceOptions>
                            <InternationalShippingServiceOption>
                                <ShippingService>UK_RoyalMailInternationalSignedFor</ShippingService>
                                <ShippingServiceCost currencyID="GBP">5.5</ShippingServiceCost>
                                <ShippingServiceAdditionalCost currencyID="GBP">1</ShippingServiceAdditionalCost>
                                <ShippingServicePriority>1</ShippingServicePriority>
                                <ShipToLocation>Worldwide</ShipToLocation>
                            </InternationalShippingServiceOption>
                            <ShippingType>Flat</ShippingType>
                            <ThirdPartyCheckout>false</ThirdPartyCheckout>
                            <SellerExcludeShipToLocationsPreference>false</SellerExcludeShipToLocationsPreference>
                        </ShippingDetails>
                        <ShipToLocations>Worldwide</ShipToLocations>
                        <Site>UK</Site>
                        <StartPrice currencyID="GBP">1.75</StartPrice>
                        <Storefront>
                            <StoreCategoryID>4</StoreCategoryID>
                            <StoreCategory2ID>18</StoreCategory2ID>
                            <StoreURL>http://www.stores.ebay.co.uk/id=65487123</StoreURL>
                        </Storefront>
                        <TimeLeft>PT0S</TimeLeft>
                        <Title>APPLE IPHONE 4G 16GB WITH BOX</Title>
                        <HitCount>146</HitCount>
                        <GetItFast>false</GetItFast>
                        <SKU>3011</SKU>
                        <PostalCode>NE38 2RR</PostalCode>
                        <PictureDetails>
                            <GalleryType>Plus</GalleryType>
                            <GalleryURL>http://i.ebayimg.com/10/!C!Vcd9QBWk~$(KGrHqV,EpD6PBNCjQDUrM!~~_1.JPG?set_id=880000500F</GalleryURL>
                            <PhotoDisplay>PicturePack</PhotoDisplay>
                            <PictureURL>http://i.ebayimg.com/10/!C!Vcd9QBWk~$(KGrHqV,!hD6PBNCjQDUrM!~~_1.JPG?set_id=880000500F</PictureURL>
                        </PictureDetails>
                        <DispatchTimeMax>1</DispatchTimeMax>
                        <ProxyItem>false</ProxyItem>
                        <BusinessSellerDetails>
                            <Address>
                                <Street1>Example Store,</Street1>
                                <Street2>Rosewood Lane,</Street2>
                                <CityName>Corbridge</CityName>
                                <StateOrProvince>Tyne and Wear</StateOrProvince>
                                <CountryName>United Kingdom</CountryName>
                                <Phone>0191 123 6547</Phone>
                                <PostalCode>NE38 3DL</PostalCode>
                                <CompanyName>Example Seller Ltd</CompanyName>
                                <FirstName>Sales</FirstName>
                                <LastName>Dept</LastName>
                            </Address>
                            <Fax>0191 123 4568</Fax>
                            <Email>Seller@example/com</Email>
                            <LegalInvoice>true</LegalInvoice>
                            <TermsAndConditions>Cheque payments.</TermsAndConditions>
                            <VATDetails>
                                <VATSite>GB</VATSite>
                                <VATID>88934349</VATID>
                            </VATDetails>
                        </BusinessSellerDetails>
                        <BuyerGuaranteePrice currencyID="GBP">10000</BuyerGuaranteePrice>
                        <BuyerRequirementDetails>
                            <MinimumFeedbackScore>-1</MinimumFeedbackScore>
                            <MaximumUnpaidItemStrikesInfo>
                                <Count>2</Count>
                                <Period>Days_30</Period>
                            </MaximumUnpaidItemStrikesInfo>
                        </BuyerRequirementDetails>
                        <ReturnPolicy>
                            <ReturnsAcceptedOption>ReturnsAccepted</ReturnsAcceptedOption>
                            <ReturnsAccepted>Returns Accepted</ReturnsAccepted>
                            <Description>Faulty/Damaged items must be reported to us within 7 days of receipt. </Description>
                        </ReturnPolicy>
                        <ConditionID>1000</ConditionID>
                        <ConditionDisplayName>New</ConditionDisplayName>
                    </Item>
                    <QuantityPurchased>2</QuantityPurchased>
                    <Status>
                        <PaymentHoldStatus>None</PaymentHoldStatus>
                    </Status>
                    <TransactionID>1521204026</TransactionID>
                    <TransactionPrice currencyID="GBP">1.75</TransactionPrice>
                    <SellingManagerProductDetails>
                        <ProductName>APPLE IPHONE 4G 16GB WITH BOX</ProductName>
                        <CustomLabel>3011</CustomLabel>
                    </SellingManagerProductDetails>
                    <Platform>eBay</Platform>
                    <Variation />
                    <OrderLineItemID>390234894873-152134214026</OrderLineItemID>
                </Transaction>
            </TransactionArray>
            <BuyerUserID>buyer-id</BuyerUserID>
            <PaidTime>2011-04-08T13:59:01Z</PaidTime>
            <ShippedTime>2011-04-08T16:16:54Z</ShippedTime>
            <IntegratedMerchantCreditCardEnabled>false</IntegratedMerchantCreditCardEnabled>
            <EIASToken>nY+sHZ2PrBmdj6wVnY+sEZ2PrA2dj6wJmYqmCJeFpQ+dj6x9nY+seQ==</EIASToken>
        </Order>
    </OrderArray>
</GetOrdersResponseType>
```

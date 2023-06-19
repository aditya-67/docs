What is a Bill Object?
Bill Object is Setu’s standard way of getting the details from a biller’s system. This contains info about the user, about the bill value, and different line items and breakups (such as taxes, fee, etc) within a bill. For more details, refer to documentation on creating bill objects.

What is a Settlement Object?
Settlement Object within a bill defines the money routing rules for settlement after the transaction is complete. It could be used to define which account to settle the money into as well as how much should which account get.
If you have more than one bank account registered with Setu, it is mandatory to use the Settlement Object. Refer to detailed documentation on the Settlement object

What is the time format to be used in APIs?
All timestamp related JSON parameters in Setu APIs use UTC time in ISO-8601 format with milliseconds precision. In general, this can be defined by the following datetime format - YYYY-MM-DDTHH:mm:ss.mmmZ - where ‘T’ and ‘Z’ are constants and other symbols have their usual meanings.
All JWT tokens to be used with Setu APIs also contain a timestamp field called ‘iat’. This is an Epoch timestamp with seconds precision.

I have an existing API with similar functionality, can it be used?
Please reach out to us at dev.support@setu.co and we will see what is the best we can do for you

Is there any other way to upload bills other than using the APIs for BBPS?
Setu has a paid CSV upload plugin for bills that allows any biller to upload a simple CSV file to generate as many bills as required. This simplifies the initial integration process for billers and allows them to go-live faster.

What happens once I go-live on BBPS?

Once we have integrated with your APIs and take you live let's say today. By tomorrow you will be able to see your business listed in the Bhim app where you can test the integration and may be even make a payment with real money.

The categories usually remains the same for all apps, so to find you business, select the app -> select the category -> search for your business.

If you see issues like business name being incorrect or amount exactness to be incorrect or any other issue, then this is the time to raise such issues with us because it's faster and easier to change now than later. After 2 weeks from today, you will gradually start seeing apps like PayTm, Mobikwik, PhonePe, GooglePay etc,. to start listing your business. It is completely dependent on the app to decide when to list you, but NPCI has mandated that all the BBPS integrated apps should list a business within two weeks of activation.

Although there's no live tracker to track when these apps will be onboarding you, we are actively working on getting this information to you.

Explain the different status of the bill in the Collect BBPS API.

Status Meaning
BILL_CREATED The bill is created in Setu system.
PAYMENT_SUCCESSFUL User has made a successful payment.
PAYMENT_FAILED User has made a payment but it failed due to some validation reasons or bank side issue.
CREDIT_RECEIVED The money is received by Setu from the payer app / BBPS network.
SETTLEMENT_SUCCESSFUL The money is settled to biller account.
SETTLEMENT_FAILE The attempt to settle money to biller account has failed - generally we would either resolve this internally with next batch of settlement or reach out to you in case there is some additional info required.
BILL_EXPIRED The bill is stale and has been expired.

Explain the different amount exactness scenarios in the Collect BBPS API.

Exactness Value Meaning
EXACT User can pay only the exact amount as mentioned in the bill.
EXACT_DOWN User can pay the exact amount as mentioned in the bill or any amount lower than that upto a certain minimum limit.
EXACT_UP User can pay the exact amount as mentioned in the bill or any amount higher than that upto a certain maximum limit.
RANGE User can pay any amount between the mentioned minimum limit and maximum limit.
ANY User can pay any amount between an optionally preset minimum limit and maximum limit.

What is T+2 Settlement?
Whenever a customer makes a bill payment, the amount is first deposited into the payment processor’s account. Next, Setu handles the settlement process when funds are released into Setu’s accounts and then Setu does a batch settlement against all transactions to respective biller accounts. This process takes 2 days after the customer transaction has been completed, and so the settlement timeframe is T+2.

When are settlements delayed?
In certain cases, when banks have settlement holidays, we receive funds into Setu’s account later than expected. This is the only time there may be unexpected settlement delays from our end. Refer to the list of settlement holidays here.

Can settlements be reversed? Why?
Settlements cannot be reversed once we have settled money to a biller’s account, as Setu has no control over the money that’s already gone out from its bank. However, if you have multiple settlement accounts for which settlement rules have to be updated OR if you want to update settlement account details, please contact us at support@setu.co.Settlements cannot be reversed once we have settled money to a biller’s account, as Setu has no control over the money that’s already gone out from its bank. However, if you have multiple settlement accounts for which settlement rules have to be updated OR if you want to update settlement account details, please contact us at support@setu.co.

Where can I view settlements?

Consume our Reports APIs to access settlement reports. Read more here.
Use our Console to view and download reports in a CSV format.

Can you support split settlements?

Setu bill objects can optionallycontain instructions to inform Setu about how to settle a collected bill amount. These details include—
Which bank accounts the settlement should be done to.
What is the split to be applied when doing the settlement.

Note that this is mandatory when you have multiple settlement account details provided to Setu. Refer to our detailed docs on how split settlement works.

What are the different types of Bill Status?

Payment Successful- Transaction is successful from the end customer to the payment partner.
Credit Received- Setu has received the funds and MIS from the payment partner.
Settlement Successful- Setu has settled the transaction to the biller
Settlement Failed- Transaction has failed from Setu to the billers.
Payment Failed- Transaction is failed from Payment partner to Setu

What is CSV upload system?
This is a system that can be used to quickly go live on BBPS. You can upload your customers' bill data as CSV files and Setu will interface with the BBPS systems to allow you to do bill collections.

Which biller categories are supported?
Currently Loan repayments and Education Fee collection are supported.

What are the steps I need to perform to go live?

Sign up
Download the template for data
Upload some test data into the system
URL with Setu Team
Setu team will configure you on BBPS and perform testing with the Bank and NPCI
Once you are ready to go live, you will be informed.
Upload real customer data.

What happens when the customer pays the bill?
When the customer pays the bill, the amount paid will be subtracted from the bill amount. When there is no more amount to be paid, customer will see no outstanding amount message on Payer Apps.

What happens when I upload new data?
The older data for that customer is overwritten.

Can I upload excel files?
No, we only accept CSV files.

My customer has paid through another channel, how do I update?
You can update a customer's record in our system by uploading new batch of data with outstanding amount as 0. You can upload fresh data as many times as you want and keep our system refreshed.

How long is the csv files stored for?
Your CSV files are stored for 1 month and are deleted from our system

How can I delete all my data in your system?
Contact our support and we will delete all your data in our system.

What happens if I exclude a customer line item in the last upload? Will the system keeps fetching as per old records?
Yes. The only way to mark a customer as no outstanding balance is to make sure you upload a new record with that customer's outstanding amount as 0.

How much time does it take to reflect your system whenever there is a fresh upload?
The data is refreshed in our systems in under 10 minutes. However on BBPS payer apps do cache the bills and it might take a while before the data is updated for them. Please make sure you update the right data always to make sure your customer does not face any issues.

Is there any validation check done on data uploaded ?
No, the system does not validate any details about the data.

If there are errors in some of the rows, is there a way to know this?
No, the CSV system does not give visibility into this. It expects data uploaded to be in the exact format and the file to be valid.

What is Bharat BillPay System?

BBPS (Bharat BillPay System) is an interoperable network of billers and payer apps. National Payments Council of India operates this scheme with the approval from RBI.

Merchants can connect to an omni-channel network of UPI Apps (PhonePe, GooglePay), net banking portals, mobile banking, ATM/ Kiosks and physical locations like bank branches, business correspondents, agent kiosks, all with a single integration. There are 400+ digital apps and 3.5 million offline locations across India where customers can pay bills.

Think about how you pay utility bills - electricity, water, gas, DTH recharge? You open any mobile app of choice, find the 'biller', input the customerID, and complete the payment within minutes. This is now expanded to non-utility categories, such as:

Loan Repayments
Credit Card
Mutual Fund
Insurance
Cable
Housing Society
Subscription Fees (eg OTT)
Educational Fees (School/College/Pvt. Institutions)
Municipal Taxes

Setu enables you to enlist one such 'biller' under the given categories. Collecting through this channel can improve efficiency and drastically reduce the cost of collections.

Pricing and operating guidelines have been provided by NPCI for each category.

Who is eligible for BBPS?

According to RBI, any merchant with a recurring payment relationship with a customer can qualify as a biller.

NPCI is responsible for creating guidelines and pricing for each category. As of August 2020, here is the exhaustive list of categories enabled by NPCI:

There are 17 categories live on BBPS currently.:

Utilities
Electricity
Gas - Piped Line
Water
Telecommunications
Mobile Postpaid
Landline Postpaid
Broadband Postpaid
DTH
Gas- Cylinder
Fastag Recharge
Loan Repayments
Credit Card
Mutual Fund
Insurance
Cable
Housing Society
Educational fees (School/ College/ Pvt. Institutions, etc.)
Subscription fees - digital, offline, OTT
Hospital Collection
Clubs and Associations
Recurring deposits/ EMI deposits/ Installment deposits
Municipal Taxes and Services
Note \*Mobile Prepaid recharge not covered in BBPS

Don't see a category here that you want to participate in? Write to us at sales@setu.co

What is the customer flow in BBPS?

Think of how you make an electricity bill payment. You login to the preferred app (e.g. PhonePe), find the electricity provider (e.g. BESCOM), and “fetch” and outstanding bill.

Like BESCOM, your business may want to enable retail customers to pay using such an experience. Setu will enable you to onboard as a ‘biller’ with our APIs.

The flow as will be similar for other categories. Each category unique ID differs based on the choice of the biller. For example, the loans category enables “loan account number” or a combination of “mobile number” and “date of birth”.

Who is a biller in BBPS?

A biller is a business that can generate bills against provided goods / services and wants to transact with our Collect BBPS or PhonePe product

What is the difference between Payment gateway and Bill collection?

The basic difference between a payment gateway and bill collection is the mechanic of “push” vs “pull”.

When a payment gateway is used for collecting the money from users, you need to “pull” them to an app or webpage that can support the transaction - this could be your website, your app, the payment gateway’s webpage, etc. Sometimes, these also require the user to create an additional account to complete the transaction or even do this behind the scenes without user consent.

When you use Collect BBPS, you are enabling users to search for outstanding bills and pay from within the comfort of payment apps that they already use. Users use their preferred apps, and can also avail popular cashbacks and discounts. Additionally, the payer apps also provide helpful nudges like reminders and push notifications to help you with your bill collections in a timely manner. In a way, you are “push”-ing the user to complete the transaction using their favorite channels / apps.

Finally, you don't incur the cost of maintaining your own payment gateway and customers can pay you 24x7 from any one of 400+ apps or 3.5 million agent locations across India.

What is Setu’s role in BBPS? Are you an operating unit?

Setu Collect is a technology platform that enables businesses to onboard BBPS as a ‘biller’.

Our goal with Setu Collect is to provide you with a comprehensive, easy to consume API set for bill payments and a world-class developer experience that is unmatched. We’ve partnered with multiple BBPOUs (RBI licensed entities who can offer BBPS services to businesses) so that you don’t have to go through the hassle! Some of these partners include top banks in the country.

Contact us at sales@setu.co for a complete list of all our BOU partners.

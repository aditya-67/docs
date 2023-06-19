What is UPI?

UPI is a real-time, instant payment system developed by NPCI, with which funds can be transferred instantly to any bank account. UPI Deeplinks is a medium through which transaction details can be shared across all UPI / banking apps in line with NPCI specs.

Steps Taken for PA Non-Compliance

This is to apprise you that your UPI DeepLinks account with Setu is disabled as of 24-Mar-2023 due to non-compliance with PA migration formalities in spite of multiple reminders.

As we have previously communicated to you, Setu has been acquired by Pine Labs, and further to this acquisition, we have decided to withdraw our Payment Aggregator (PA) license application, and move our PA services under Pine Labs’ PA License. To ensure a smooth transition for all our valued merchants, certain services would have to be migrated under Pine Labs' PA license. As a merchant onboarded and transacting via Setu, this means that you were required to re-upload your KYC documents and sign the Amendment to the Setu MSA and the PA agreement of Pine Labs - which were not completed per the set deadline of 15-Mar-2023.

What does this mean?

From 24-Mar-2023, you will no longer be able to generate payment links nor will your customers be able to make payments against previously created links.

You will no longer be able to initiate refunds via the API or via the Bridge.

You will continue to have access to the Bridge to view any previous transactions and settlement reports.

Refunds: With the window for initiating refunds being 180 days and since you will no longer be able to initiate refunds via the Bridge/APIs, the refund process will have to be handled manually. This means you must transfer funds [to an account communicated by Setu] with the amount equivalent to the transaction amount for which the refund must be initiated along with the transaction details.

Chargebacks and Disputes: For chargebacks and disputes raised for previous transactions, Setu will reach out to the designated POCs to submit/share the proof of deliveries, invoices, and any other authorized proof of product/service delivery. If you fail to provide the necessary proof within the due date, Setu will send a debit note followed by a legal notice

Current Onboarding Requirement for UPI Deeplinks

We would like to inform you of an update to our UPI DeepLinks service agreement. As you may know, Setu has been acquired by Pine Labs. As part of this acquisition, we have decided to withdraw our Payment Aggregator (PA) license application.

To ensure a smooth transition for all our valued merchants, certain services will be migrated under Pine Labs' PA license. This means that all merchants who are onboarded and transacting via Setu will be required to re-upload their KYC documents and sign the PA agreement of Pine Labs.

To simplify this process for you, we have updated the KYC & Agreement sections on the Bridge to collect the necessary KYC documents for your type of business. We have prepared a step-by-step guide on how to re-upload your KYC documents and sign the PA agreement of Pine Labs to ensure a seamless transition.

We kindly remind you that the deadline for completing the activity is 15th March, 2023. To ensure uninterrupted service, we request you complete this activity before the deadline. Failure to complete this activity before the deadline will result in the deactivation of your account and transactions. We appreciate your continued support during this transition and thank you for your understanding. If you have any questions or concerns, please do not hesitate to reach out to us.

How to re-upload your KYC documents?

https://www.loom.com/share/fc6c39f5d0c1454bae97b5e23898fa6b

Overview/Flow of how UPI Deeplinks works?

A Merchant sends payment details to Setu and receives a unique payment link to send to their Customer.

A Customer clicks the payment link, chooses the preferred UPI app, and enters mPIN to make a successful payment.

Once the payment is successful, Setu triggers a webhook notification for the completed payment, which the Merchant can use to update the transaction status at their end.

Once payment is received, Setu settles the amount to the Merchant per the configured settlement timeline.

What can I do with UPI deeplinks?

Provide payment details and generate deeplinks that work across supported UPI apps. Your customers can make payments using any UPI app available on their phone, like PhonePe or GPay.

Share the payment link anywhere—WhatsApp, SMS, as QR codes, or as part of reminders and push notifications.

Who is a Merchant?

Any business that wants to collect payments for goods or services provided to customers to use UPI DeepLinks.

What is Collect UPI DeepLinks?

UPI is a real-time payment system developed by NPCI, with which funds can be transferred instantly to any bank account. Through Collect DeepLinks, which conforms to NPCI specs, a merchant can enable their customers to go to a UPI app with pre-filled payment information directly.

How do refunds for UPI work?

Setu provides access to refund functionality for UPI payments. Refunds can either be auto-initiated by Setu for pre-defined scenarios or voluntarily initiated by the merchant using APIs and through The Bridge.

Types of Refunds:

Merchant-initiated refunds: The merchant can request a refund for one or more transactions. Reasons could include the return of goods and services and more.

Third-party verification (TPV) refunds: If the account used by the customer for making payment does not match what the merchant is expecting (for example, a KYC-specific source account in the case of financial services merchants), a refund can be initiated. TPV is enabled by Setu only upon request from the merchant.

Setu-initiated refunds: Setu automatically refunds a transaction in cases where the transaction is not properly routed through the UPI eco-system and cannot be reconciled. Setu also initiates refunds automatically when the amount exactness validation rules set for the payment link fail.

Various scenarios for Setu-initiated refunds.

Missed notification from the bank: Occasionally, our partner bank does not send us the platform bill ID correctly in their notification to Setu, resulting in us being unable to reconcile the transaction even though the payment was successfully made by the customer. In such cases, we refund the transaction.
Missing/Incorrect OrderID: There are scenarios when the partner bank does not send us a payment notification in real-time. We end up reconciling such transactions the following day when we get an MIS file from the bank and refund them. But if the merchant wishes, we allow a configuration to process these transactions & settle instead as well.
Amount exactness validation failure: An amount exactness validation is when a given payment has a validation error - for example, payment has an exactness condition of ≥Rs 500, but the payment is for Rs. 400. In such cases, it doesn’t meet the amount exactness validation and is refunded to the source account.
Duplicate payment for the same bill: Setu’s UPI DeepLinks supports only one payment per generated DeepLink. But if more than one payment is detected for a given link, all subsequent payments (except the first) are refunded to the source account. Whether the first payment was a failure or a success doesn't matter.
Expired bill: Whenever a link is created with an expiry date and payment is made after that time, the transaction will automatically be refunded.

How many times can a user pay on a link?

All UPI links are for single use, irrespective of the expiry date. Even if the customer is able to make double payments (due to the UPI app caching policy or other such issues), Setu will settle the first payment to the merchant and automatically refund all subsequent ones to the user. The refund TATs depend on the user's bank.

Why is the intent flow different on an iOS device?

UPI intent is very popular with Android users because it enables them to make payments from any UPI PSP app installed on their mobile phone. The customer selects the desired app on the merchant checkout, an intent flow is triggered, and the payment is completed by entering the mPIN on the UPI app. The customer gets redirected back to the merchant’s app upon successful completion.

Whereas an iOS user moves around to the selected UPI app manually and completes the payment by entering the mPIN on the desired UPI app.

What is an intent flow, and how is it different from a collect flow?

1. Collect Flow

This traditional UPI collection flow allows bank account holders to transact using VPAs without entering additional bank information. The standard steps followed include:

Select UPI as the payment option in the merchant app/website and enter a valid VPA.

Push notification/SMS on collect request is sent to the customer to verify with UPI PIN/MPIN.

When done, a notification is sent to the app/website.

2. Intent Flow

In intent flow, as soon as the customer selects the UPI payment app on the checkout of the website/app, the app is launched automatically on the mobile device. Your customers are also benefitted in the following ways:

No need to handle push or SMS notifications

No need to switch between applications to complete a payment (merchant, SMS, and app)

No need to remember their VPAs

How much time does it take for me to go live?

It takes 3-4 working days to go live post-submission of KYC in case there are no clarifications.

What is the KYC required for me to go live?

Below is the list of KYC required to go live on UPI

Proof of Identity

Business Legality Proof

Proof of Business Address

Merchant UPI VPA

Settlement account details

Can a customer pay on the same link once a bill has been paid?

The user cannot pay on the same link once a bill has been paid.

How long are the links available/What is the validity of the links?

The validity of payment links is 40 days.

Is Sandbox testing possible for UPI Deeplinks?

The sandbox environment does not connect to live bank systems or NPCI systems. Hence, we have developed an API addCredit where you can pass certain parameters to simulate a successful transaction.
Steps:

Generate a UPI deep link using the create payment link API.

Note the parameter name upiID in the response.

Use this UPI ID in the accountID under destinationAccount.

Use any UPI ID in the accountID under sourceAccount, any amount as float value in rupees (caution: this is different from other Setu APIs where the amount is an integer value in paise), and type as "UPI".

Send the add credit request, and you should receive a 200 OK response.

If you have followed the above steps correctly, the payment status should change to CREDIT_RECEIVED, and you should receive a hit on the callback URL.

Can I get onboarded to use UPI Deeplinks if I am an Individual?

Yes, you will have to submit certain KYC details, and post verification, you can get yourself onboarded.

How do Merchant-Initiated refunds work?

Refunds can be initiated from the merchant side either on The Bridge or by integrating directly with the API. Refunds for UPI payments will always be adjusted against the total settlement amount to merchants’ settlement accounts on a given day.
Settlements from Setu are always done in batches on T+1 day for UPI, with the batches essentially being a combination of Merchant ID + Settlement Account.
So, as an example, if 100 transactions of 10 rupees were made for Merchant A with settlement account S, a single settlement of 1000 rupees (minus Setu’s charges) would be made to account S.

When the merchant initiates refunds, the refund amount will be adjusted against this batch amount. As an example, if the merchant wishes to refund 2 transactions (from the current day or from the past) worth 200 rupees each, then 400 rupees will be deducted from the 1000 rupee payout batch, and only 600 rupees will be settled to the merchant’s settlement account and the refunds worth 400 rupees will be initiated via our partner bank.

Which roles have access to initiate refunds on the Bridge Dashboard?

A Maintainer, Developer and Admin can access can initiate refunds on the Bridge Dashboard.

What is the Chargeback and Dispute period for UPI Transactions?

The duration applicable to dispute or raise a chargeback is 170 days.

How to use OAuth 2.0 encryption?

To use OAuth 2.0 authentication merchant has first to generate OAuth 2.0 keys. Then the merchant admin can use the keys to generate tokens via our OAuth 2.0 token generation API. The token can be passed as a Bearer token Authentication header to call other APIs.

How to test callback notifications?

Callback notification can be triggered by using the mock payment API on the sandbox. Before the development of the callback API, merchants can use Beeceptor (https://beeceptor.com/) to create endpoints and see what kind of requests are sent to this URL.

Which authentication mechanism is better? JWT or OAuth 2.0 ? and why?

OAuth 2.0 is an open standard for authorization and works over HTTPS. In Setu's context, it is used to authorize API requests with access tokens. Read more about OAuth 2.0 here ↗.
For Setu products, OAuth keys provide a lot of flexibility—you can set up a single set of keys to authorize requests for multiple product configurations or authorize requests for a single configuration using multiple sets of keys. One can delete/regenerate OAuth 2.0 keys. These features are not available for JWT.

How to download Reports on Bridge?

Please follow the below steps:

Steps to download a report:

Click on the Reports Tab on the explore bar on the left.

You could choose to Download or Email the report.

If you want reports to be scheduled for you or your team can also be done.

Where can I view Refund and its status?

When you click on Reports Tab on the dashboard, click on the Refunds tab, and you can view all the refund details for the transactions.

What are the different types of refund statuses?

Created: This is when the merchant initiates a refund request via APIs or through the Bridge (Setu dashboard). The refund or its processing has not taken place at this point.

Initiated: This is when the refund request has been intimated to the banking partner and begins processing the refund. This is a refund's final or terminal status, as NPCI does not share information about when a refund hits the customer’s bank account.

Pending: This status is implied in case the refunds have not been processed due to a low settlement balance/funds, or the merchant is not transacting for a while. There are two primary reasons for this status:

Insufficient funds: This status would appear if a merchant creates refunds and there is a low balance to refund all or any of the requests made. The merchant should have sufficient or more balance to avoid refunds getting delayed due to insufficient funds.

Example: Merchant X created 10 refunds for Rs.1000, and only 8 got refunded since the clearing balance was insufficient for the refunds to get processed, consisting of 10, 100 rupee refund requests each, and the total settlement amount for the day is 850 rupees. These would be refunded once the merchant has sufficient balance. The first 8 refunds that were registered will be processed in the current settlement cycle. A callback notification will be sent to the merchant with the payload containing the first 8 refunds in the `initiated` block and the remaining in the `pending` block.

No Active Transactions: This status implies that when a merchant has not had transactions for a while and raises a refund, active transactions are required for this to move to initiated status.

Example: Merchant Y has not transacted for 1 or more days and has created Refund requests. Since there are no active transactions, the refunds would remain in Pending status with the reason No Active Transactions.

Are partial refunds possible?

Yes, partial refunds are possible.

How to set up refunds on our accounts?

Refunds will be available for all merchants by default. You can integrate with the Refund API mentioned here or log in to the Bridge and navigate to the report section.

What is the timeline for a refund to be credited to the customer's accounts?

The timeline for a refund to be credited to a customer's bank account is 1-7 working days.

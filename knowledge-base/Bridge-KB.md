What is the Bridge?

The Bridge, a completely revamped Setu Console, lets you integrate with Setu’s financial products, manage live integrations, and view transaction & settlement reports.

Some important changes from the old Setu Console—

Products → Instead of a single Biller ID for all payment channels, you will now see a unique Biller ID for each payment channel you have integrated with. Each biller ID corresponds to a unique product configuration. You can click on Configured products to see all configurations you have created. Please note that the product configurations you are live with, will only show on the Production environment on the Bridge. Switch to Production environment by clicking the top border, to view transactions for live product configurations. Here’s how.

Reports → We have upgraded Reports to display both transactions & settlements data with new, advanced filters and search. View up to 25,000 records and instantly download CSV for any search result. Reports can be viewed both for Sandbox / Production product configurations.

User Management → Add users with different permissions to your account—Admin, Developer, Maintainer & Reporter and give access to some or all Sandbox / Production product configurations.

What are the common Setu Bridge terms?

Partner ID → A partner ID is a unique identifier for your account, created during sign-up. You can find this partner ID by going to Org settings from the left panel. This would be useful while reporting any issues with your account.

Products / Product Configurations → Products are API integrations offered by Setu and a partnering payment channel like PhonePe, Kotak, or ICICI. Your account can have multiple configurations of products, which are listed inside Product Configurations in the left panel.

Biller ID / Merchant ID → A unique identifier for a specific product configuration. This can be used to report and resolve issues. When a product configuration is opened, this ID is shown below the Biller / Merchant name.

Sandbox Environment → The Sandbox environment lets you create test configurations, to do mock transactions from a customer’s point of view and test settlements, without any KYC / business details.

Production Environment → Product configurations can be taken live on the Production environment by providing additional KYC details to be reviewed by Setu. Reports for live product configurations can be viewed on Production.

How do I sign in to Bridge account?

Kindly access bridge.setu.co and log in with your existing Setu Console credentials.
Change the password by clicking on Forgot Password.
Use the reset password link sent to the specified e-mail ID and do the necessary changes accordingly.

How do I reach Setu’s support team for any issues with Bridge?

Create a new ticket on this link in case you face any issue. If applicable, add screenshots or screen recordings to help us resolve your query faster.

If possible, do include additional details against your complaint, either the

Partner ID → A partner ID is a unique identifier for your account, created during sign up. You can find this partner ID by going to Org settings from the left panel. This would be useful while reporting any issues with your account.

Biller ID / Merchant ID → This is unique identifier for a configured product (same as the integration done for a payment channel). Navigate to Configured Products from the left panel, click a configuration and look for the ID below the Biller / Merchant name.

How do I view and use Settlement and Transaction reports on The Bridge?

Access Reports from the left panel. View data for one or multiple product configurations (payment channels). Filter data for successful payments, settled bills, or for different types of payment instruments.

\*You can additionally access Reports from inside a product configuration, on the Transactions tab.

Here's a video (https://www.loom.com/share/581b0fceb3b94703b82565d398082e9a) on how to search for, view, and download settlement information.

You can access reports for configured products on both Sandbox and Production. Switch to the Production environment by clicking the top border, to view transactions for live product configurations. Here’s how (https://www.loom.com/share/79b5d2bb5c514a7f8884327ba1d78675).

How do I use search and filters?

Search across one or multiple product configurations done on different payment channels and combine with a search for Platform Bill ID or Transaction Reference ID to view a particular bill. A quick video on this.

Also, filter by transaction or settlement dates, payment instrument, and bill status. Update & re-apply filters too. Here’s another video for reference. To understand what different bill statuses mean, refer to this.

Bridge Report Parameter definition

S: NO Report Parameters Meaning
1 Platform Bill ID A unique Bill ID generated for every transaction by Setu
2 Biller Bill ID Identifier created by the biller for every bill
3 Biller MCC Merchant Category Code of the biller. Applicable for UPI Deeplink Products Only
4 Platform Bill Status Status of the bill in Setu System
4.1 SETTLEMENT_SUCCESSFUL The money is settled in the merchant/Biller account.
4.2 SETTLEMENT_FAILED The attempt to settle money to merchant/Biller account has failed - generally, we would either resolve this internally with the next batch of settlement or reach out to you in case there is some additional info required.
4.3 BILL_EXPIRED The UPI link has expired either by the default timeline or the timeline set by the customer.
4.4 BILL_CREATED The UPI link or BBPS Transaction link is created.
4.5 PAYMENT_SUCCESSFUL The user had made a successful payment for a transaction
4.6 PAYMENT_FAILED The user has made a payment but it failed due to some validation reasons or bankside issue (rare scenario).
4.7 CREDIT_RECEIVED The money is received by Bank Partners to Setu's Bank account.
5 Amount Total Exact amount billed for the end customer
6 Amount Paid Amount paid by the end customer
7 Payment Instrument Various modes of payment available by the end customer to make the payment
8 Payment Date Payment date and time details
9 Payment Reference ID Unique payment ID as shared by UPI/BBPS network
10 Payment Receipt The receipt generated against the payment by Biller/Merchant/Setu
11 Settlement Date Date of Settlement to the Biller/Merchant
12 Settlement UTR Settlement UTR details for the biller/merchant
13 Primary Account Number Primary bank account associated with the biller/merchant
14 Primary Account IFSC Primary bank IFSC associated with the biller/merchant
15 Primary Account Name Primary bank account name associated with the biller/merchant
16 Primary Account Settlement Amount Settlement amount sent to the primary bank account
17 Total Settlement Amount Total amount settled for a transaction to biller/merchant
18 Split Settlements Description of each part of the split in settlement
19 BPC Total Total bill payment charges deducted by Setu
20 BPC (%) Percentage on the basis of which the bill payment charge is calculated
21 BPC FLAT Flat fee calculation of bill payment charge
22 GST Total Total GST charged on bill payment
23 GST(%) Percentage fee on the basis of which the GST is calculated
24 GST FLAT Flat fee calculation of GST

Refunds 101

Setu provides access to refund functionality for UPI payments. Refunds can either be auto-initiated by Setu for pre-defined scenarios or can be voluntarily initiated by the merchant using APIs and through The Bridge.

Types of Refunds:
Merchant-initiated refunds: The merchant can request a refund for one or more transactions. Reasons could include the return of goods and services and more.

Third-party verification (TPV) refunds: If the account used by the customer for making payment does not match what the merchant is expecting (for example, a KYC-specific source account in the case of financial services merchants), a refund can be initiated. TPV is enabled by Setu only upon request from the merchant.

Setu-initiated refunds: Setu automatically refunds a transaction in cases where the transaction is not properly routed through the UPI eco-system and cannot be reconciled. Setu also initiates refunds automatically when the amount exactness validation rules set for the payment link fail.

Various scenarios for Setu-initiated refunds.
Missed notification from the bank: Occasionally, our partner bank does not send us the platform bill ID correctly in their notification to Setu, resulting in us not being able to reconcile the transaction even though the payment is successfully made by the customer. In such cases, we refund the transaction.

Missing/Incorrect OrderID: There are scenarios when the partner bank does not send us a payment notification in real time. We end up reconciling such transactions the following day when we get an MIS file from the bank and refund them. But if the merchant wishes, we allow a configuration to process these transactions & settle instead as well.
Amount exactness validation failure: An amount exactness validation is when a given payment has a validation error - for example, payment has an exactness condition of ≥Rs 500, but the payment is for Rs. 400. In such cases, it doesn’t meet the amount exactness validation and is refunded to the source account.

Duplicate payment for the same bill: Setu’s UPI DeepLinks supports only one payment per generated DeepLink. But if more than one payment is detected for a given link, then all subsequent payments (except the first) are refunded to the source account. It doesn’t matter whether the first payment was a failure or a success.

Expired bill: Whenever a link is created with an expiry date and payment is made after that time, the transaction will automatically be refunded.

What are the different types of refund statuses?

Created: This is when the merchant initiates a refund request via APIs or through The Bridge (Setu dashboard). The refund or its processing has not taken place at this point.

Initiated: This is when the refund request has been intimated to the banking partner and begins processing the refund. This is the terminal status of a refund, as NPCI does not share information about when a refund hits the customer’s bank account.

Pending: This status is implied in case the refunds have not been processed due to a low balance or the merchant not transacting for a while. There are 2 reasons to elaborate on this status:

Insufficient funds: This status reason would appear if a merchant creates refunds and there is a low balance to refund all or any of the requests made. The merchant should have sufficient or more balance to avoid refunds getting delayed due to insufficient funds.
Example: Merchant X created 10 refunds for Rs.1000, and only 8 got refunded since the clearing balance was insufficient for the refunds to get processed, consisting of 10, 100 rupee refund requests each, and the total settlement amount for the day is 850 rupees. These would be refunded once the merchant has sufficient balance. The first 8 refunds that were registered will be processed in the current settlement cycle. A callback notification will be sent to the merchant with the payload containing the first 8 refunds in the `initiated` block and the remaining in the `pending` block.

No Active Transactions: This status implies that when a merchant has not had transactions for a while and raises a refund, active transactions are required for this to move to initiated status.
Example: Merchant Y has not transacted for 1 or more days and has created Refund requests. Since there are no active transactions, the refunds would remain in Pending status with the reason No Active Transactions

Are partial refunds possible?

Yes, partial refunds are possible.

How to set up refunds on our accounts?
Refunds will be available for all merchants by default. You can integrate with the Refund API mentioned here.

What is the timeline for a refund to be credited to the customers' accounts?
The timeline for a refund to be credited to a customer's bank account is 1-7 working days.

How do Merchant-Initiated refunds work?
Refunds can be initiated from the merchant side either via The Bridge or by integrating directly with the API. Refunds for UPI payments will always be adjusted against the total settlement amount to merchants’ settlement accounts on a given day.

Settlements from Setu are always done in batches on T+1 day for UPI, with the batches essentially being a combination of Merchant ID + Settlement Account.

So, as an example, if 100 transactions of 10 rupees were made for Merchant A with settlement account S, a single settlement of 1000 rupees (minus Setu’s charges) would be made to account S.

Now, when the merchant initiates refunds, the refund amount will be adjusted against this batch amount. As an example, if the merchant wishes to refund 2 transactions (from the current day or from the past) worth 200 rupees each, then 400 rupees will be deducted from the 1000 rupee payout batch, and only 600 rupees will be settled to the merchant’s settlement account and the refunds worth 400 rupees will be initiated via our partner bank.

Which roles have access to initiate refunds on the Bridge Dashboard?
Maintainer, developer & admin level access holders can initiate refunds on the Bridge Dashboard.

How do you add settlement accounts on Bridge?

For adding Settlement accounts in Bridge navigate to the “Configured products” section from the left navigation. Choose the product configuration for which settlement information needs to be added—you will be able to see and select the “Configuration” tab. Scroll down on this page to add settlement account details.

How do I switch from one partner ID to another?

You may have more than one partner ID on Bridge. If so, you will see a list of available partner IDs during login and can select anyone to proceed. See a sample video.

You may also switch your partner after logging in by navigating to Organisation settings → Switch org

How do I disable or edit a role for a user?

Navigate to Organisation settings → People. Search for the user you want to disable or edit the role for, and click to Edit permissions for the user.

How do I add a role?

If you are an Admin for this partner ID, you can navigate to Org settings from the left panel. Click “People” to add a new user—

Click Invite new member.

Enter e-mail and role type. Select the product configurations to give access to on Sandbox and/or Production. To understand what a “role” is, read this.

Once done, hit Send Invite—this invites the user to log in to your partner ID with the above rules.

Here’s a video walkthrough to give a “Reporter“ access to a product config on Sandbox.

How do I use search and filters?

Search across one or multiple product configurations done on different payment channels and combine with a search for Platform Bill ID or Transaction Reference ID to view a particular bill. A quick video on this.

Also, filter by transaction or settlement dates, payment instrument, and bill status. Update & re-apply filters too. Here’s another video for reference. To understand what different bill statuses mean, refer to this.

How do I view settlement details & reports?

Search across one or more product configurations by specific settlement information like Settlement UTR or Settlement Account . You can also download settlement reports. Here’s a video on how to search for, view and download settlement information.

What is user role management on The Bridge?

User role management can be used to specify different types of permissions for a user when an Admin gives access to their partner ID (or account). You can also view more information on each role on this link. Below is a brief summary of role permissions—

Admin

Developer

Maintainer

Reporter

Add new users

✅

⛔

⛔

⛔

Add new product configurations

✅

✅

⛔

⛔

Edit existing configurations

✅

✅

✅

⛔

View reports

✅

✅

✅

✅

Manage API keys
✅

⛔

⛔

⛔

View API keys

✅

⛔

⛔

⛔

\*Aside from the Admins for a partner ID, all users will have access only to specified products on Sandbox or Production.

Switch to Production environment by clicking the top border, to view transactions for live product configurations

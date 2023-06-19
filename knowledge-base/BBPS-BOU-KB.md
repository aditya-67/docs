Who is an Agent?

An agent is a registered BBPS entity allowed to collect payments for BBPS billers across all categories.

You may register as an agent on BBPS to collect BBPS bill payments with Setu APIs on your supported collection channels (offline or online).

What can I do with this product?

With Setu BillPay, you can enable a complete BBPS bill payment experience for your customers—from choosing the business to pay to fetching and paying bills—on your app or website. If you are a BBPS biller, you can even collect payments to your business directly.

Setu BBPS BillPay connects with NPCI and provides simple RESTful APIs, some of which are asynchronous. This means you may consume only the APIs or optionally subscribe to the notifications Setu provides via webhooks.

You may integrate with Setu in any of the following ways—

API integration—Register as an agent institution and use Setu APIs. Build your own screens and use your own payment gateway.

Website integration—1-line integration with pre-built screens. They have an inbuilt UPI payment option.

App integration—Integrate with pre-built screens as web views in your app. Support for Android and iOS. It has an inbuilt UPI payment option.

Why should I use the APIs and not the pre-built screens?

If you want to customize the screens and use your own payment gateway to collect the payments, then you should integrate with the APIs. You will also need to register as an Agent/Institution (AI) with NPCI. Setu teams will help you with this process.

What is an Agent/Institution?

These entities offer bill payments as a feature to their customers on their channels. These channels can be physical (like business correspondents) or digital (apps or websites). For all our customers, Setu’s onboarding team takes care of the end-to-end process of AI registration with NPCI.

What is the process for onboarding the Billpay API product?

The process of onboarding the API product can be summarized as

Registering as an Agent/Institution
Designing the front-end screens
Submit the test results
Integrate with the APIs

Don’t worry; Setu teams will handhold you through all these activities.

Is a current account with a partner bank mandatory?

Yes, it is for Agents/Institutions using the API product or those using custom payment options on the pre-built screens. You will have to ensure the current account is pre-funded. If you don’t have an account, we will work with you and the Bank to ensure the account is opened without hassle.

What are the screens that will have to be submitted in BOU bill payments?

Category list screen, on which all BBPS categories are listed.

Biller list screen, on which all billers under a selected category are listed.

Customer input screen, where a customer enters identifiers specific to a selected biller before their bill can be fetched.

Payment confirmation screen, on which the customer confirms the bill amount and proceeds with the payment.

Payment status screen, when payment is being processed and is finally either successful or failed.

Confirmation SMS is the text sent after payment is successful or failed.

Bill receipt screen, through which a customer can view and download receipts for a successful transaction.

Raise a complaint screen where a customer can raise a complaint. Complaints are raised against specific transaction IDs.

Complaint status screen, where a customer can see the latest status associated with a registered complaint.

You may use the BBPS logo and branding guidelines provided here.

Here is a BBPS-compliant UX flow and a quick summary of BBPS guidelines to keep in mind—,

The app/website UI must contain a button for “Pay bills” with the BBPS logo shown.

BBPS logo must be on the top right corner of all screens used by customers during the search of biller or bill and also for screens relating to the payment of the bill.

BBPS assured logo must always be shown on the payment successful and receipt pages. The regular BBPS logo can be removed from these.

How much time does it take to go live on BillPay product?

It takes 3-4 weeks to be onboarded as an agent institution once the screen approvals are in place.

When can a customer raise a dispute on a transaction?

It is advised for a customer to raise a dispute after 24 hrs of making a transaction.

How do we know if a new biller is onboarded on BBPS?

We refresh the master file of the biller every week to ensure any new biller is reflected in the list.

What is the timeline for getting the final status of the transaction?

What is the timeline for getting the final status of the transaction?

What is the validity of the created pre-built screens link? Can this be extended?

The validity of the link expiry can be configured according to the agent’s use case. The default validity to accept payments once the link is opened is 3 days, and the validity of the link expiry is 7 days.

What are the pre-built screens?

The pre-built screens are those that Setu has developed that follow NPCI guidelines for BBPS BillPay.

We have worked with NPCI to build a white-labeled product for agents to help minimize the time taken to go live for our agents. To use the pre-built screens or the white-labeled product, you only need to onboard with Setu.

What is the process for onboarding the white-label product?

Complete the onboarding with Setu and go live with a one-line integration. Refer here for more details on the integration.

Setu’s pre-built screens—for the website, iOS, and Android—come with an in-built UPI payment option. However, if you’d like to integrate your own payment gateway, please refer to these guides too.

What are the customizations available in the pre-built screens?

The pre-built screens are those that Setu has developed to follow all the NPCI guidelines for BBPS BillPay. With the screens, we have also allowed customizations to help agents align the pre-built screens to their front-end look and feel. This allows agents to enable the bill payments to feature quickly and efficiently at their end. Agents can customize the following:

Agent logo

Favicon

Icons color

Background color

Display specific biller categories

User journey, subject to NPCI guidelines

Which payment modes are available with the integration of the white-label/pre-built screen?

Currently, we only support UPI as the only payment mode with white-label product integration. However, if agents wish to use the pre-built screens and collect payments through modes other than UPI, they can do so. You can refer to this guide. To offer custom payments, an agent must onboard as an Agent/Institution with NPCI.

What are the steps involved in Agent Institution onboarding?

Following are the steps involved in Agent Institution onboarding

Current Account Opening

Agent Onboarding

Screen Approval

Test Case Submission

What payment modes can we use in our custom payment methods?

Below is the list of all the allowed payment methods in custom payment methods:

IMPS

Debit Card

Prepaid Card

NEFT

Credit Card (not allowed for biller categories such as loan repayments and credit card repayments)

Internet Banking

Account Transfer

Wallet

Cash (only available for Agents enabling offline payment modes)

UPI

How can an agent receive more details of a transaction?

Agents can configure a webhook to receive notifications on user events. This is an opt-in feature. Here are the different user events available for agents -

Bill_fetch_success,

Bill_fetch_failure,

Bill_payment_success,

Bill_payment_failure,

Bill_payment_refunded,

Dispute_raised,

Dispute_status_change

More details on the user events can be found here.

What are one-time links?

One-time links are an add-on feature of the white-labeled product wherein an agent can generate links to capture payments configured using customer and bill details. This can skip the bill fetch step for the customer.

Which parameters are needed while creating the one-time link?

Mobile number is a mandatory parameter that will take the user to the home page.

If a category Code is passed, it will show the user the list of Billers.

If the category code and the biller ID are passed, it will show the bill fetch form.

If the category code, biller Id, and customer parameters are passed, it will show the bill directly. The session is valid only for some time and becomes invalid if the user is inactive. You would need to generate this link uniquely for each of your customers and make sure you get a new link each time your customer wants to get back to the bill payment journey.

What are the Pre-built screens?
The pre-built screens are those which Setu has developed to follow all the NPCI guidelines for BBPS BillPay. We have worked with NPCI to build a Whitelabled Product for agents to help minimize the time taken to go live for our agents. To use the Pre-built screens or the Whitelabeled Product, you only need to onboard with Setu.

What is the process for onboarding the Whitelabel product?
Complete the onboarding with Setu and go live with a one-line integration. Refer here for more details on the integration.

What are the customizations available in the Pre-built screens?
The pre-built screens are those which Setu has developed to follow all the NPCI guidelines for BBPS BillPay. With the screens, we have also allowed for customizations to help agents align the pre-built screens to their own front-end look and feel. This allows agents to enable the bill payments to feature quickly and efficiently at their end. Agents can customize the following
Agent logo

Favicon

Icons colour

Background colour

Display specific biller categories

User journey, subject to NPCI guidelines

Which are the payment modes available with the integration of the whitelabel/pre-built screen?
Currently, we only support UPI as the only payment mode with the whitelabel product integration. However, if agents wish to use the pre-built screens and collect payments through modes other than UPI, they can do so. You can refer to this guide. To offer custom payments, an agent has to onboard as an Agent/Institution with NPCI. More on this here (<insert link for the question on AI onboarding>).

What payment modes can we use in our custom payment methods?

Below is the list of all the allowed payment methods in Custom Payment Methods.
IMPS

Debit Card

Prepaid Card

NEFT

Credit Card (not allowed for biller categories such as loan repayments and credit card repayments)

Internet Banking

Account Transfer

Wallet

Cash (only available for Agents enabling offline payment modes)

UPI

How can an agent receive more details of a transaction?
Agents can configure a webhook to receive notifications on user events. This is an opt-in feature.
Here are the different user events available for agents -
Bill_fetch_success,

Bill_fetch_failure,

Bill_payment_success,

Bill_payment_failure,

Bill_payment_refunded,

Dispute_raised,

Dispute_status_change

More details on the User Events can be found here.

What are one-time links?
One-time links are an add-on feature of the Whitelabeled product wherein an agent can generate links to capture payments configured using customer and bill details. This can skip the bill fetch step for the customer.

Which parameters are needed while creating the one-time link?
Mobile Number is a mandatory Parameter and it will take the user to the home page.
If a category Code is passed, it will show the user the list of Billers.

If the category code and the biller ID are passed, it will show the bill fetch form.

If the category code, biller Id, and customer parameters are passed, it will show the bill directly. The session is valid only for some time and becomes invalid if the user is inactive. You would need to generate this link uniquely for each of your customers and make sure you get a new link each time your customer wants to get back to the bill payment journey.

What is the validity of the created link? Can this be extended?
The validity of the link expiry can be configured according to the agent’s use case. The default validity to accept payments once the link is opened is 3 days and the validity of the link expiry is 7 days.

API product FAQs
Onboarding Related
Why should I use the APIs and not the pre-built screens?
If you want to customize the screens and use your own payment gateway to collect the payments, then you should integrate with the APIs. You will also need to register as an Agent/Institution (AI) with NPCI. Setu teams will help you with this process.

What is an Agent/Institution?
These are entities that offer bill payments as a feature to their customers on their channels. These channels can be physical (like business correspondents) or digital (apps or websites). For all our customers, Setu’s onboarding team takes care of the end-to-end process of the AI registration with NPCI.

You can know more about the technical and compliance information on this here.

What is the process for onboarding the API product?  
The process of onboarding the API product can be summarized as
Registering as an Agent/Institution

Designing the front-end screens

Submit the test results

Integrate with the APIs

Don’t worry, Setu teams will handhold you through all these activities.

Is a current account with a partner bank mandatory?
Yes, it is for Agents/Institutions using the APIs or those using custom payment options on the pre-built screens. You will have to ensure the current account is pre-funded. If you don’t have an account, we will work with you and the Bank to ensure the account is opened without any hassle.

What are the screens that will have to be submitted?
Category list screen, on which all BBPS categories are listed.
Biller list screen, on which all billers under a selected category are listed.

Customer input screen, where a customer enters identifiers specific to a selected biller before their bill can be fetched.

Payment confirmation screen, on which the customer confirms the bill amount and proceeds with the payment.

Payment status screen, when payment is being processed and is finally either successful or failed.

Confirmation SMS is the text that is sent after payment is successful or failed.

Bill receipt screen, through which a customer can view and download receipts for a successful transaction.

Raise a complaint screen, where a customer can raise a complaint. Complaints are raised against specific transaction IDs.

Complaint status screen, where a customer can see the latest status associated with a registered complaint.

You may use the BBPS logo and branding guidelines provided here.

Here is a BBPS-compliant UX flow and a quick summary of BBPS guidelines to keep in mind—,

The app/website UI must contain a button for “Pay bills” with the BBPS logo shown.

BBPS logo must be present on the top right corner of all screens used by customers during the search of biller or bill and also for screens relating to the payment of the bill.

BBPS assured logo must always be shown on the payment successful and payment receipt pages. The regular BBPS logo can be removed from these.

How much time does it take to go live?
It takes a total of 3-4 weeks to be onboarded as an agent institution once the screen approvals are in place.

APIs related
When can a customer raise a dispute on a transaction?
It is advised for a customer to raise a dispute after 24 hrs of making a transaction.

How do we know if a new biller is Onboarded on BBPS?
We refresh the master file of the biller every week to ensure any new biller is reflected in the list.

What is the timeline to get the final status of the transaction?
The timeline is T+1. If you do not get a final status even after T+1, you can reach out to Setu Support by writing to support@setu.co.

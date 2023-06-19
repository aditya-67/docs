What is KYC?

What is Setu KYC?
Setu KYC is an umbrella of user verification data blocks to validate customers or businesses. Setu works with multiple government agencies and partners to help organizations validate identity.

Setu KYC offers PAN verification, Aadhar verification, Bank account verification, Digilocker Verification, and Aadhar-based E-Sign.

Pick one or more data blocks from our KYC verification bundle. Get details instantly over API with industry-best response times. Type of data blocks that we are solving for :

PAN
Adhaar KYC
Digilocker
Bank account verification

PAN: Setu PAN API allows you to use just one API to verify your customer’s PAN details. We directly connect with NSDL, to maintain the best uptimes. Link
Check the name, category, and validity instantly
Use one API for individuals/businesses
Verify straight from NSDL

Adhaar KYC: Offline Aadhaar KYC, or OKYC, is a legally compliant KYC method as per UIDAI guidelines. Your customers can provide their Aadhaar number and verify with an OTP sent to their Aadhaar-linked mobile number, to access a downloadable XML file with their Aadhaar detailsThis file has all details that can be derived from an Aadhaar card—like name, gender, DOB, and address—and is locked by default. Your customer sets up a 4-digit access code that can be used to unlock the contents of this file. Link
Get all details with Aadhaar input
Ensure privacy with base 64 encoded encryption
Integrate pre-built, theme-able UI

Digilocker: DigiLocker is a document wallet from the Government of India. Citizens can use it to store digital versions of various documents, including Aadhaar card, driving license, marks sheets, ration card, and much more. Documents are fetched into DigiLocker directly from the source of the issuer and are deemed to be at par with original physical documents as per Rule 9A of the Information Technology Rules, 2016. Documents can also be uploaded by citizens, for storage on DigiLocker. Link
Verify via authorized government sources
Reduce document file uploads
Validate users, even new to DigiLocker

Bank account verification: Setu Bank account verification API allows you to use just one API to verify your customer's Bank account details. We integrate with RBI-licensed banks to provide bank account verification services. ₹1 is credited to the bank account that has to be verified. Link
Verify private or public bank accounts
Use one API for current or savings accounts
Choose between async or sync modes

How can I sign up for Setu KYC?
Please reach out to us at this link

What is Setu PAN API?

Setu PAN API allows you to use just one API to verify your customer’s PAN details. We directly connect with NSDL, to maintain the best uptimes.

What can I do with Setu PAN API?

Use our lightweight PAN API to verify your customer, with their consent—to check identity during onboarding, enable other financial products or to enable income tax filing/verification.

Here’s a quick overview of the PAN API. Additionally, here are the URLs you would need for this API:

Sandbox—https://dg-sandbox.setu.co

Production—https://dg.setu.co

Headers—Contact Setu for providing the credentials required to successfully call Setu APIs. This contains:

x-client-id

x-client-secret

How do you verify PAN?

Call the API to verify a PAN provided by your customer. Here is a quick explanation of the request params—

pan is the PAN value. It may belong to categories like Person, Company, Trust, Government, Firm, etc.

consent indicates if you have collected consent from your customer. To get a successful verification, it must contain Y or y.

reason is the explanation of why you are requesting for PAN from your customer. It should be explained in 20 characters or more.

NOTE: While the implementation of consent and reason cannot be enforced by Setu, we recommend collecting explicit consent from your customers and also explaining to your customers the reason why you are verifying their PAN.

What are the test details one can use?

While testing on Sandbox, you may use the following sample values—

Use ABCDE1234A for a valid PAN

Use ABCDE1234B for an invalid PAN, i.e, a PAN number has been found but is invalid. A PAN is considered invalid by NSDL for different reasons. For e.g, if it is a blacklisted one, or maybe because it is not linked to an Aadhaar card.

If you use any other values for pan, you will get a 404 PAN not found error.

What is DigiLocker?

DigiLocker is a document wallet from the Government of India. Citizens can use it to store digital versions of various documents, which include an Aadhaar card, driving license, marks sheets, ration card, and a lot more.

Documents are fetched into DigiLocker directly from the source of the issuer and are deemed to be at par with original physical documents as per Rule 9A of the Information Technology Rules, 2016. Documents can also be uploaded by citizens for storage on DigiLocker.

What can I do with the Digilocker product?

Fetch documents of your users instantly and directly from the issuing authority, with user consent. Use the fetched documents to perform KYC without any delay.

DigiLocker has a wide variety of documents—covering a large number of government organizations, educational institutions, banks, etc. that can be leveraged to ease the onboarding and verification journeys for your customers.

What are the steps in Digilocker Integration?

Setu DigiLocker APIs can be used to fetch documents of your users instantly—with their consent.

Here’s a quick run-through of the APIs—

Create a DigiLocker request—Create a request to start the user journey, with which you can get user consent and then fetch the document from the user’s Digi locker. You get an id in response, which you can use to track this request throughout the journey.

Get DigiLocker request status—Check the status of a request created by passing the request id, at any point in the journey.

Get the list of all docs available—Get a global list of all documents that DigiLocker lets you fetch and the identifiers required to fetch a particular document.

Fetch a document—Get the document the user has consented to share with you, made available as a file URL to download. All docs, other than Aadhaar, can be fetched with this API.

Fetch Aadhaar data—Fetch Aadhaar document data in JSON format as well as an XML file. The API response is consistent with our OKYC APIs, which aids in replacing OKYC with DigiLocker, for carrying out Aadhaar KYC.

Revoke access token—Revoke the OAuth user token once necessary user documents are fetched.

Do you have any test data/identity for validating API in the sandbox?

PAN
Use ABCDE1234A for a valid PAN
Use ABCDE1234B for an invalid PAN, i.e, a PAN number has been found but is invalid
If you use any other values for PAN you will get a 404 PAN not found error.

Aadhar Verification
Use 999999990019 as the Aadhaar number for success
Use 773032249986 for an Aadhaar that does not have a linked mobile number
Use 2GAD0 for valid captcha and any other value for invalid.
Use 123456 for a valid OTP.
Use 123457 for OTP to mimic 1st failed attempt.
Use 123458 for OTP to mimic 2nd failed attempt.
Use 123459 for OTP to mimic failed attempts limit exceeded.

Bank Account Verification
Always set the account number value as 1234567890
ABCD0123456—successful verification response.
ABCD0123457—invalid transaction response. This may happen if the provided account does not support IMPS transactions.
ABCD0123458—transaction limit may have been reached. This may happen if, at the time of the penny drop, the transaction has exceeded the daily IMPS limit for the account. While this is rare, it is still a possibility.
ABCD0123459—downstream service error.
ABCD0123450—pending verification.
ABCD0123467—invalid account details.

What is masking?

Masking is a type of task to mask some sensitive data on a document image. We mask the first 8 digits of the aadhar number as part of the response.

Do you charge for all API requests?

We only charge for the tasks that are marked as “Completed/Successful” by our system.

Where are your servers located?

Our servers are located in India - Amazon web services platform (AWS), Mumbai region.

What is your purging policy?

Customer data is always purged after the completion of a task. We have two modes of purging the data - ‘Immediate’ or ‘After x minutes/hours. We purge the document images as well as the PII data from the API request & response. The mode is selected based on the product and use case

What are the certifications that you have?

We are ISO 27001:2013 certified.
We are also compliant with RBI SAR for data localization.
We have also implemented ISO 27017 and ISO 27018 codes of practice.

What is Setu Bank account verification API?

Setu Bank account verification API allows you to use just one API to verify your customer's Bank account details.

We integrate with RBI-licensed banks to provide bank account verification service. ₹1 is credited to the bank account that has to be verified.

What can I do with this product?

Use our lightweight verification APIs to verify the bank account information of your customer—to check identity during onboarding or to enable transfers to the account. You can choose one of the following modes to integrate with bank account verification APIs—

Sync API

Async API

What is the difference between Sync and Async APIs?

Sync API lets you initiate a verification request and expect an immediate response on the status of the verification. Essentially, you will need the following API—

Verify bank account—This lets you initiate a verification request, and get verification status in response.

Async lets you initiate a verification request and let it complete asynchronously—without having to wait for an immediate response. Essentially, you will need the following 2 APIs—

Verify bank account—This lets you initiate a verification request.

Get verification request details—This lets you check the status associated with the verification request.

What is offline Aadhaar KYC?

Offline Aadhaar KYC, or OKYC, is a process of verifying a customer's identity and other details through their Aadhaar card. It is a legally compliant KYC method per the guidelines of the Unique Identification Authority of India (UIDAI).

Under this process, the customer provides their Aadhaar card number and verifies it with an OTP sent to their Aadhaar-linked mobile number. Upon successful verification, the customer will get access to a downloadable XML file that contains all the details that can be derived from an Aadhaar card, such as name, gender, date of birth, and address. The file is locked by default, and the customer must set up a 4-digit access code to unlock it and view its contents.

What does Setu provide in the OKYC solution?

At OKYC, we understand the importance of providing customers with a secure and easy way to access their Aadhaar XML.

Our APIs provide a real-time solution to fetch Aadhaar XML for your users quickly and securely.

Our ready-to-use screens make it simple for customers to get their Aadhaar XML in a shareable format, as well as set up a share code for you to access the file’s contents.

We also give you the option to customize our screens to match your brand colors and logo, allowing you to embed them as a web view in your app or to redirect customers to the link via your website.

What can I do with OKYC?

Offer your customers a smooth experience for OKYC. Extract verified details of your customers with confidence.

Whichever industry you belong to—insurance, finance, gaming, or even transportation and logistics—you can ease the onboarding and verification processes for your customers.

What are the steps to integrate OKYC?

Below are the steps the client is required to follow:

Start KYC and business documentation

Get API credentials

Choose Integration Method

Different OKYC Modes of integration.

There are 2 ways to integrate on Setu:

Pre-built Screens

API Integration

Steps to perform in Pre-built Screens

Setu’s web-based solution can complete a customer’s KYC with offline Aadhaar—within your app or website, in real-time. Offline Aadhaar involves getting a downloadable, locked XML file with Aadhaar information from your customers.

Essentially, only 2 APIs are required to enable this flow—

Create an OKYC request—Create an OKYC request for your customer. You will get a unique id response, which can be used to track this particular request.

Post this, and the customer should be redirected to Setu’s UI for collecting details like the Aadhaar number and share code for the locked XML file.

Get OKYC request status—Get customer verification by providing the request id.

What are the steps in API Integration?

Setu’s API solution can complete a customer’s KYC with offline Aadhaar real-time—with your own screens on your app or website. With this, you will get a downloadable, locked XML file with Aadhaar information from your customers.

The following APIs are required to enable this flow—

Create an OKYC request—Create an OKYC request for your customer. You will get a unique id in response, which can be used to track this particular request.

Initiate OKYC Request—Initialise the OKYC request for your customer with the previously returned request id and receive an base64 encoded captchaImage from Setu. Once you have called this API, you can redirect your customer to your OKYC screens to collect the Aadhaar number and captcha from your customer.

Verify OKYC Request—Share the aadhaarNumber and captchaCode, collected from your customer, with Setu. Next, redirect your customer to a screen to collect OTP sent to your customer’s Aadhaar-linked mobile number. Also, request your customer to enter a 4-digit share code—this code will be used to unlock your customer’s fetch Aadhaar XML file.

Complete OKYC Request—Share the collected otp and shareCode to complete the verification process. Next, you can call the Get OKYC request status API. Once the OKYC request has been processed successfully, you will get customer details from the Aadhaar and the XML file link in the response

Get OKYC request status—Get customer verification status by providing the request id and, optionally, the shareCode.

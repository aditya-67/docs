What is Account Aggregators (AA)?

Account Aggregators have regulated entities that facilitate consented data between FIPs and FIUs. This data is facilitated based on the guidelines/framework set by Data Empowerment Protection Architecture (DEPA). They act as a bridge between information providers, i.e., banks, and users like lenders to enable data facilitation.

In simple words, an Account Aggregator is a consent manager for Financial Data: a new class of NBFC approved by RBI to manage consent for financial data sharing. It was created through an inter-regulatory decision by the Reserve Bank of India (RBI), Securities and Exchange Board of India (SEBI), Insurance Regulatory and Development Authority (IRDAI), Pension Fund Regulatory and Development Authority (PFRDA) through the Financial Stability and Development Council (FSDC). RBI licenses the AAs.

Who are the participants in the AA ecosystem?

FIUs: FIU stands for “Financial Information User’. An FIU consumes the data from a FIP to provide various services to the end consumer. E.g., a lending Bank wants access to the borrower’s data to determine if a borrower qualifies for a loan. The lending Bank is the FIU. Banks play a dual role – both as a FIP and an FIU.

FIPs: FIP stands for ‘Financial Information Provider’ – the data fiduciary. FIPs are the institutions that hold your data for E.g., For example, your Bank, NBFC, Mutual Fund Depository, Insurance Repository, Pension Fund Repository, etc.

Who do Setu cater to, and what is Setu offering?

The two products target different customers, and this is an indicative list of potential customers.

Product Name

Type of Customers

Setu FIU

Direct Customers

Digital Lenders (LendingKart, Recur Club, etc)

Banks & NBFCs ( Kotak Mahindra, Muthoot, etc.)

Personal Finance Management Apps (Jar, Smallcase, Spenny)

Neobanks (Jupiter, Open, etc.)

Many others with more data types are coming on board the framework

Agya Account Aggregator

TSPs: Technical Service Providers who handle parts of the value chain that an AA cannot or chooses not to participate in:

FIU TSPs - Anyone who wants to build flows for consumer data consent and sharing data with FIUs ( Setu, FinBox, etc.)

Data processors: Perfios, FinBit, Karza

Resellers - Any organization that wishes to sell Agya’s AA services

FIP TSPs - Organizations that specialize in onboarding and management of financial institutions that want to provide data via the AA framework.

Consumers - Citizens who utilize AAs consent and data fetch services to share their financial data securely.

What is the flow followed in AA?

The lender makes a data consent request, which is routed to the AA.

The user receives a notification through the AA that the lender wants to access 3 months' bank statements.

The user can decide to approve or reject the consent request.

If they approve the request, the data is fetched from the FIP—in this case, the bank—and shared with the lender.

The consent request carries details about the type of data, how long the FIU needs it for, and how they plan to use it. The user can take into consideration all of these factors before deciding to approve or reject the request. The user can also decide to withdraw consent for a previously-approved request. This way, the user remains the custodian of their own data

How does one integrate the product?

Setu’s AA APIs can be broken down into 3 broad flows—

Consent flow—To create and share data consent requests with your customers, along with the handling of approvals/rejections.

Data fetch flow—To request for and fetch the data, once your customer has approved the consent request.

Notifications flow—To receive notifications from Setu for key events like approval/rejection of consent or be notified when FI data is ready to be fetched.

What are the KYC requirements to get onboarded on the AA system?

FIU onboarding checklist

Here’s a checklist for a regulated and licensed entity to become an FIU in the AA ecosystem. Setu helps you get onboarded on the Central Registry, taking away compliance and certification complexity.

Step

Purpose

Process owner

Remarks

Submission of FIU's license

To be shared with Sahamati to establish eligibility to become an FIU

SETU

FIU to share this with Setu. Setu then shares this with Sahamati as part of our certification process.

Customer experience guidelines checklist

To serve as a common reference for all AA ecosystem participants with respect to the dos and don'ts of Customer experience design

SETU

Setu shares this with Sahamati on the FIU’s behalf

Legal adherence guidelines checklist

To examine and verify the legal boundaries around the roles of each party, particularly with respect to data privacy protection principles, against a set of principles that the AA committee has decided

SETU

Setu shares this with Sahamati on the FIU’s behalf

FIU certification

To ensure interoperability and adherence to technical standards specified by ReBIT. Read more here.

SETU

Setu completes the certification process on FIU’s behalf in partnership with Aujas

Central registry onboarding

To be discoverable by other entities in the ecosystem such as AAs and FIPs

SETU

Setu shares the necessary payload to get the FIU onboarded on the Central Registry

Customer journey demo

To demonstrate the customer journey of approving a consent

SETU

FIU's consent flow gets reviewed

Which banks/insurers/securities institutions are on the AA framework or FIPs?

You can view their status here: https://sahamati.org.in/fip-fiu-in-account-aggregators-ecosystem/

What are the data parameters that I can get on the consent of the user?

PAN of the user. It is part of the response in bank deposit data.

3 digits of the Bank account number

Bank account details of only chosen bank accounts will be shared with the FIU post the consent is signed.

CKYC status will be available during this consent as well

What are the UI guidelines as part of the FIU activity?

All relevant parts of the consent object need to be shown in some manner on the UI. This CAN be under expandable or secondary layers/sections.

The AA logo and text are mandatory with Financial Institutions' (FI) data life, Data types & Purpose on the UI.

Can I be the end recipient of user data on behalf of my FIU? (Eg: process a statement or do underwriting)

No, the end-user and accountable party will always be the regulated entity.

How does pricing work in this ecosystem?

FIPs charge for the data fetch is not yet determined by Sahamati. You get charged per statement pulled from a FIP.

Do I get immediately notified if a customer withdraws consent for data sharing? How?

Yes, via the consent notification APIs. Both FIUs & FIPs are intimated.

Does the data get fetched the moment the customer gives consent?

No, there is a separate API call related to data fetches that must be made to fetch data.

The time to fetch data is a few seconds and can be done within the data consent start and end date range

What are the various response types on data fetch request post consent?

inancial data from Setu FIP is available in XML and JSON formats.

Specify the required format as part of the Get Data Session API.

This page will help you understand the structure of each FI type and what data will be available for you to build on top of. These FI types contain one account per FI type with 15 to 30 transactions spread across 6 months (Jan 1, 2021, to June 30, 2021). We're adding dynamic mock data for more realistic and exhaustive integration testing.

Refer here : https://docs.setu.co/data/account-aggregator/fi-data-types

Can the customer change the consent parameters and then accept the request?

No, all consent parameters must be set and passed on via the Create Consent API BEFORE the approval flow for users

Here is the list of parameters to set in the consent https://docs.setu.co/data/account-aggregator/consent-object-The customer can only consent to or reject the request

How do the consent parameters or conditions get set? Does one need separate consent for each account from which I want data?

Here is the list of parameters to set in the consent Account Aggregator Consent object — Setu Docs. The FIU sets these parameters.

https://docs.setu.co/data/account-aggregator/consent-object

Can you generate a bank statement via AA?

No, it will not be an actual "bank statement" with a bank logo, but all statement data will be available and shared in JSON or XML format.

Do you have a bank statement analyzer and income verification function?

Yes, we do. https://docs.google.com/spreadsheets/d/1nfredSjAECqPgLWftb3lq-KiqKiKhJUk_e_pYDkku4Q/edit#gid=595183067

What's the maximum duration I can fetch a customer's data for in the past and future?

It is based on the use case and has guardrails set by Sahamati.

Does the FIP generate a session ID in a data fetch, or does the AA generate it? If FIPs, is there a unique session ID per FIP?

One Session ID per FIP is generated.

How does a user deny a consent request?

By abandoning the flow and not consenting until the consent request timeout

By clicking on reject consent during the flow

Do citizens/end-users have to download the AA app and have to sign up with ALL AAs? Or do they only sign up once?

They have the option to download the same at their convenience. They only need to sign up with AAs as and when they need to approve consents that involve the AA in question, OR they download the AAs' consent manager app.

When, how, and can an end user withdraw consent from my app as an FIU?

A user cannot withdraw from the FIU app currently. Customers must visit an AA consent manager app to withdraw consent. Customers must visit an AA consent manager app to withdraw consent.

Can AAs view the data in a fetch/consent flow?

No. AAs are data-blind and only transport encrypted data from FIP to FIU. Unencrypted data is never seen by the AA.

How do I test out the flow?

Visit Bridge

Ensure you are in "Sandbox" mode (Top & middle of the screen)

Setup a "financial information user" product under the data tab

Add your theming, and callback URL for notifications, and set up the product

Test it using our Postman collection (https://documenter.getpostman.com/view/15462260/UVCBBQLW#intro)

Why should I go via a TSP vs Directly going to an AA?

All AAs also have their own TSP

Going direct to AA is a tedious and time-consuming process. Things you have to handle yourself include:

Certification

Web-redirection guidelines of AAs (Frontend)

Request signing and decryption

Adhering to changes in AA standards

Maintaining your frontend consent flows on the AA partner infra and creating a deployment strategy.

Relations and commercial agreements as a single entity with each AA that you plan to integrate with

Why should I connect to more than 1 AA?

Multiple sign-ups: If the user has signed up on one AA and you are partnered with another AA, they will have to start their approvals with an added step of signing up

Coverage: There may be cases where some FIPs take a short while to get live on all AAs (only a 1-2month window)FIP-AA Mapping | FIP - Account Aggregator mapping - Sahamati

Regulatory mandate: It may be mandated by Sahamati and ReBIT to be completely interoperable and connected to every AA

Are all FIPs on all AAs?

Yes, they will be on all AAs. They do have the option to do limited rollouts with an AA partner, to begin with. FIP-AA Mapping (https://sahamati.org.in/fip-aa-mapping/) has details of the mapping of FIPs to AAs. Post the stability of the FIPs fetch services. It will roll out to multiple AAs (usually in 1-3 months)

Does one need separate consent for each account from which I want data?

No, a single consent can be used to fetch data from multiple FIUs (banks, insurers, etc)

For separate purposes, beyond the consent expiry date or a specified FIdatarange (from the consent object), the FIU may need another consent.

Does one need separate consent for each use case?

For separate purposes, the FIU will need to take another consent

Eg: One for underwriting and one to monitor loans

We allow for multiple consents to be taken in a single flow through our embedded UI

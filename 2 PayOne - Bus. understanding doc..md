**PROJECT: PAYONE DATABASE DESIGN**



**STAGE 1: DATABASE PLANNING AND REQUIREMENTS ANALYSIS**



**COMPONENT TWO: BUSINESS UNDERSTANDING DOCUMENT**



Document Category: Database Planning and Requirements Analysis
(Business Understanding Document)
Organisation: PayOne (Proposed Business Case)
Document Status: Draft – Version 1.0
Date: November 2026



**## 1. INTRODUCTION**



\# 1.1 Purpose of the Document



This Business Understanding Document (BUD) provides key details and information
to enhance appreciation and understanding of PayOne's business activities, processes,
operations, segments, services and stakeholders. In doing so, it outlines the business
context critical to analysing, documenting and  identifying the organisation's
database requirements.



The document is a critical base reference for subsequent stages

of the database planning and requirements analysis, particularly:

* Business process identification and documentation.
* Identification and categorisation of business entities and stakeholders.
* Identification of operational data requirements.
* Identification of information flows and business transactions.
* Determination of the organisation's database scope and boundaries.
* Identification of functional and non-functional database requirements.
* Development of the conceptual, logical and physical database designs.



This BUD primarily helps stakeholders better appreciate and understanding the business of PayOne,

how its business activities are organised, who participates in those activities. This is necessary to identify

the form and nature  information is generated, exchanged, processed and maintained. Note, therefore,

that it does not prescribe the final database architecture or implementation technology.



\# 1.2 Background and context of the business of PayOne



PayOne is a Ghanaian digital payments and financial technology enterprise, organized as an integrated

digital payments and business services provider.



The business commenced operations in 2020, initially serving fewer than 100 business and individual clients.

Its customer base has subsequently expanded to more than 500,000 business and individual clients/customers,

where more than a million business related transactions are conducted daily.

&#x20;

The organisation operates across multiple interconnected digital business segments, including commerce,

customer communication, digital service distribution, identity verification, merchant management

and payment facilitation.



Despite its significant expansion, PayOne currently maintains a fragmented information-management system, including:

* Enterprise Resource Planning (ERP) system
* Microsoft Excel spreadsheets.
* Manual operational records.
* WhatsApp-based business communications and records.
* Other operational and externally managed digital systems.



These impair data consistency and integration, reporting, record retrieval and coordination of business activities.

The company, therefore, intends to establish an integrated data system underpinned by a centralized database management system

essential for automated, efficient, scalable, reliable and timely business operations. This is necessary for real time transactions.



\# 1.3 Business Understanding Approach



The business may be broken down into the following hierarchical framework:



Business → | Business Function| → | Service/Process | → | Delivery Channel | →  | Technology/Infrastructure |



These are distinct levels and not interchangeable. For example, payment facilitation is a business function;

merchant collections are a service; a mobile application or USSD interface is a delivery channel;

and an API or database server is part of the supporting technology infrastructure.

Such distinction is important in determining appropriate database entities, relationships and operational boundaries.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



**## 2. BUSINESS PROFILE AND OPERATING ENVIRONMENT**



\# 2.1 Business Characteristics



PayOne is an integrated digital business services provider serving intermediary, transactional,

distribution, management and communication functions.



The principal characteristics of the business include:

* Multi-sided business model: PayOne serves different parties to each transaction including buyers, merchants,

&#x09;businesses, service providers and institutional clients.

* Multiple business functions: It is a financial and payment transaction facilitator. it further offers the following services:

&#x09;commerce,  merchant management, communications and identity verification.

* Transaction-oriented operations: The company initiates, processes, confirms, settles and / or records transactions.
* Digital service delivery: Services are accessible through multiple digital delivery channels, including mobile

&#x09;applications, web platforms, USSD, SMS, APIs and point-of-sale interfaces.

* Interconnected and  integrated operations: It offers an integrated digital business architecture used

&#x09;by firms and individuals. This system interacts seamlessly with external financial institutions, payment networks,

&#x09;service providers, billers, merchants and technology platforms.

* Business management services The company provides financial and related business management services

&#x09;to corporate clients requiring reliable customer records, transaction histories, operational reporting, reconciliation and audit trails.



\# 2.2 Business objectives



The principal business objectives relevant to the eventual design, implementation and management of the database are:

* Improve the efficiency and reliability of business operations.
* Integrate fragmented business information.
* Support automated and timely transaction processing.
* Improve customer and merchant management.
* Strengthen operational monitoring and reporting.
* Improve transaction traceability and accountability.
* Facilitate coordination across business functions.
* Support business expansion and increasing transaction volumes.
* Improve the security, availability and consistency of business information.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



**## 3. BUSINESS SEGMENTATION AND FUNCTIONAL CLASSIFICATION**



\# 3.1 Overview



PayOne's operations are organised into six principal business segments.

A key principle in the following categorization is "function over form".

Therefore, classification is based on nature of the business activity, rather than the technology or communication

channel through which the activity is delivered.

They may not particularly correspond to separate legal entities, departments or independent database systems,

although the company attempts as much as possible to streamline its organizational structure, processes and workflow accordingly.



The six business segments are:

* Payment and Settlement Facilitation.
* Marketplace and Commerce Facilitation.
* Digital Services Distribution.
* Merchant and Business Management Services.
* Customer Communication and Engagement Services.
* Identity Verification and Authentication Services.



\# 3.1.1 BUSINESS SEGMENT ONE: Payment and Settlement Facilitation



DESCRIPTION: This segment encompasses all PayOne's activities to facilitate collection, disbursement,

processing and settlement of funds between transacting individuals, businesses, merchants and institutions.

Herein, PayOne acts as a transactional intermediary, coordinating payment instructions and associated financial

information between transacting parties as well as relevant external financial service providers.



The principal business activities in this segment include but are not limited to:

* Customer-initiated payments.
* Merchant payment collections.
* Business-to-business payments.
* Business disbursements and payouts.
* Bill and invoice payments.
* Payment processing and transaction confirmation.
* Payment reversals and refunds.
* Settlement processing.
* Transaction reconciliation.
* Payment-related fee assessment and recording.



The main transacting parties include:

* Payment initiators.
* Individual customers.
* Merchants.
* Corporate and institutional clients.
* Payment recipients and beneficiaries.
* Banks and financial institutions.
* Mobile money operators.
* Payment networks and external payment processors.
* Billers and utilities.
* Important operational distinction
* Payment collection, disbursement and settlement are related but distinct processes.



Note that a collection records receipt or processing of payments, while disbursements are transfers of funds to a recipient.

Overall, settlements encompass financial completion of obligations between transacting parties.

Note that fees may be borne by the merchant, customer or another agreed participant,

depending on the applicable commercial arrangement.



The key database implications are:

* Database must efficiently and reliably enable or support identification of transaction participants, payment instructions,

&#x09;payment methods, transaction statuses, amounts, fees, reversals, refunds, settlements and reconciliation records.



\# 3.1.2 BUSINESS SEGMENT TWO: Marketplace and Commerce Facilitation



DESCRIPTION: The marketplace and commerce facilitation function covers activities to facilitate commercial interactions

between buyers and sellers on provided digital marketplace and commerce platforms.

PayOne provides the digital environment and platform where businesses and merchants can present their

products or services and interact with prospective customers.



As a marketplace and commerce facilitator, the principal business activities of PayOne are:

* Merchant and seller registration.
* Product and service listing.
* Product categorisation.
* Product and service discovery.
* Customer enquiries and orders.
* Order management.
* Purchase confirmation.
* Order fulfilment coordination.
* Delivery coordination.
* Order cancellation and returns, where applicable.
* Commerce-related payment coordination.



The principal participants in this regard are:

* Buyers and customers.
* Merchants and sellers.
* Product and service providers.
* Delivery and fulfilment providers.
* Payment service participants.
* Marketplace administrators.



Database implications include:

* Database should accommodate key internal and external stakeholders including:  clients, customers and merchants
* Database should enable efficient management of critical transactional information including: product and

&#x09;service catalogues, categories, listings, orders, order items, fulfilment arrangements and related payment references.

* The distinction between a marketplace order and its associated payment transaction must be maintained.

&#x09;An order represents a commercial commitment, whereas a payment represents a

&#x09;financial transaction associated with that commitment.



\# 3.1.3 BUSINESS SEGMENT THREE: Third-party Digital Business Services



DESCRIPTION: PayOne facilitates client access to third-party digital payments and related services.

Unlike the marketplace platform provided, in this case PayOne enables clients to digitally access required services,

not physical commodities and goods.



The major business activities include but are not limited to:
Digital service catalogue management.

* Service provider registration and management.
* Distribution of digital products.
* Airtime and data-related transactions.
* Utility and bill payment services.
* Subscription and other digital service transactions.
* Service activation and fulfilment coordination.
* Transaction confirmation.
* Provider-related transaction monitoring.



In this regard, the main participants are:

* Individual customers.
* Corporate customers.
* Digital service providers.
* Telecommunications operators.
* Utility companies.
* Billers.
* External service aggregators.



The core database implications are:

* Database must accommodate service providers, digital service categories, service offerings, customer requests,

&#x09;service transactions, provider references, activation statuses and transaction outcomes.

* The original service provider must be distinguishable from PayOne, which facilitates access to the service.



\# 3.1.4 BUSINESS SEGMENT FOUR: Merchant and Business Management Services



DESCRIPTION: This business segment of PayOne encompasses business-facing services provided by the company to

merchants, enterprises and institutional clients. Unlike the payment segment, which focuses on processing financial transactions,

this business function helps clients to automate and digitally manage their  business relationships, financial transactions and

operational services provided to their customers.



The major business management and merchant services activities are:

* Business registration and onboarding.
* Merchant registration and onboarding.
* Business profile management.
* Merchant outlet and branch management.
* Business account administration.
* Business user and employee management.
* Merchant service configuration.
* Transaction monitoring and business reporting
* Business account support.
* Commercial agreement and service arrangement management.



Its principal participants are:

* Business owner
* Corporate clients.
* Merchants.
* Business administrators.
* Merchant employees and authorised representatives.
* PayOne relationship managers.
* PayOne operations personnel.



Database implications

* Database should support organisational profiles, business registration details, merchant accounts, branches, outlets,

&#x09;authorised representatives, business users, service agreements and also report account status

* It implies that a business may operate multiple outlets, and an individual may be associated with several businesses in different capacities.



\# 3.1.5 BUSINESS SEGMENT FIVE: Customer Communication and Engagement Services



DESCRIPTION: PayOne facilitates information exchange between itself and its key stakeholders, namely:  customers,

merchants, businesses and other participants. Due to its critical importance, this is treated as a standalone

business function instead of as a support activity.



The core activities forming part of customer communication and engagement services are:

* SMS notifications.
* Transaction alerts.
* Customer notifications.
* Business and merchant communications.
* Promotional messaging.
* Bulk messaging.
* Customer engagement campaigns.
* Service announcements.
* Communication delivery monitoring.
* Message status and delivery reporting.



Principal participants within this segment are:

* Individual customers
* Merchants.
* Corporate and institutional clients.
* Communication service users.
* Message recipients.
* Telecommunications and messaging providers.
* PayOne communication administrators.



Database implications

* The database should facilitate administration and management of communication accounts and key details of such communications.

&#x09;These include: identities of message senders as well as recipients, message content or references, communication campaigns,

&#x09;delivery requests, timestamps, delivery statuses and associated service charges.

* In the database, communication records should be linked to relevant customers, businesses or transactions where appropriate.



\# 3..1.6 BUSINESS SEGMENT SIX: Identity Verification and Authentication Services



DESCRIPTION: As a vital core function, PayOne establishes, verifies and authenticates

identities of its internal and external stakeholders.

These use PayOne's business ecosystem and infrastructure. This function facilitates customer onboarding, account security,

regulatory compliance and prevention of unauthorised access or fraudulent transactions.



Principal business activities include but re mot limited to:

* Individual identity verification.
* Business identity verification.
* Customer onboarding verification.
* Merchant verification.
* Verification of authorised representatives.
* User authentication.
* Account access verification.
* Verification status management.
* Identity-related compliance monitoring.



Principal stakeholders

* Individual customers.
* Business entities.
* Merchants.
* Business representatives.
* Authorised users.
* Identity verification providers.
* Regulatory and compliance personnel.



Database implications

* Database should support identity records, verification requests, verification providers, verification results, verification

&#x09;statuses and relevant timestamps.

* Personal and sensitive identity information must be protected by appropriate access controls, security measures and retention policies.


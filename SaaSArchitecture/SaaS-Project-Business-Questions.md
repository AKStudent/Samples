---
title: Business Questions for SaaS Projects
abstract: This document contains business-related questions used to prepare software architecture workshops for SaaS projects. Discussing these topics is crucial for the success of SaaS projects as the technical implementation has to reflect the business goals. Starting a project with a too technical focus raises the danger of a project failure because of over-engineering or over-simplification.
author: 
- Rainer Stropek (software architects gmbh)
margin-left: 3cm
margin-top: 3cm
margin-bottom: 3cm
margin-right: 3cm
links-as-notes: true
toc: true
toc-depth: 2
numbersections: true
papersize: A4
lang: en
---

# Introduction


This document contains business-related questions used to prepare software architecture workshops for SaaS projects. Discussing these topics is crucial for the success of SaaS projects as the technical implementation has to reflect the business goals. Starting a project with a too technical focus raises the danger of a project failure because of over-engineering or over-simplification.


# Vision and Scope

## Vision

> Add a **summary of the vision** for the new SaaS solution (i.e. what is the solution all about and what could it become).

**Don't** go in too much detail. If available, add a reference to a more detailed [vision and scope document](https://en.wikipedia.org/wiki/Vision_document).

## Project Scope

> Describe the project scope in relation to the vision (i.e. what portion of the long-term vision should be addressed in the current project).

**Consider** describing the scope of the current project as well as a rough sketch of the scopes of downstream projects.

**Consider** explicitly mentioning topics that are **out of scope** of the current project. This can reduce the risk of [scope creep](https://en.wikipedia.org/wiki/Scope_creep)


# Innovation

## External Perspective

> Describe the **key points of innovation** of the new SaaS solution **from a customer's perspective**.

**Don't** include a description of all functional and non-functional requirements.

**Do** focus on those points that differentiate the new SaaS solution from existing internal or external products.

**Consider** limiting yourself to the five most important innovations.

**Consider** using the [Blue Ocean Strategy](https://en.wikipedia.org/wiki/Blue_Ocean_Strategy#Concept) while working on these question.

## Internal Perspective

> Describe how the new SaaS solution will **fundamentally change internal aspects** of your company.

**Don't** include existing processes and structures that remain more-or-less unchanged.

**Do** describe fundamental changes to 

* business processes,
* organizational structures and
* financing.

**Consider** describing fundamental changes to your company's [value chain](https://en.wikipedia.org/wiki/Value_chain).

**Consider** limiting yourself to the five most important changes.

**Consider** using the [Business Model Canvas](https://en.wikipedia.org/wiki/Business_Model_Canvas) while working on these question.


# Target Environment

## Public Cloud vs. Private Cloud

> Specify the extent to which the new SaaS solution focuses on **Cloud Computing**.

**Do** mention a potential focus on a specific public cloud platform (e.g. *Microsoft Azure*, *Amazon AWS*, *Google Cloud Platform*). If there is a specific focus, **consider** describing the reasoning behind it.

**Do** explicitly state whether the entire software solution must be installable on-premise in customers' or partners' data centers. If this is necessary, **consider** describing the maturity of customers' private clouds that can be assumed.

**Do** mention potential bring-your-own-subscription scenarios (e.g. install SaaS solution in a public cloud environment owned and controlled by a partner).

**Don't** go into technical details regarding used cloud services, cloud architecture patterns, etc. This will be part of downstream architecture workshops.

## Limitations

> Mention **limitations regarding public cloud services** used in the new SaaS solution. **Consider** describing the reasoning behind it (e.g. specific legal requirements, avoid lock-in effects, etc.).

**Consider** potential regional limits (e.g. data centers must be inside the EU).

**Consider** certification requirements (e.g. ISO 27018; see e.g. [compliance offerings in Azure Trust Center](https://www.microsoft.com/en-us/trustcenter/compliance/complianceofferings) for examples).

**Consider** specific requirements for used cloud services considering availability and performance SLAs (*Service Level Agreements*; see e.g. [Azure SLAs](https://azure.microsoft.com/en-us/support/legal/sla/) for examples).

**Consider** required support for specific standards (e.g. communication standards like *AMQP*, authentication standards like *OpenID Connect*, etc.).

**Consider** adding a statement in which cases lock-in effects to vendor-specific cloud services are acceptable (e.g. value short time-to-market higher than risks because of lock-in effects, avoid lock-in effects by using open standards and platforms, etc.).


# Customers

## Customer Characteristics

> Describe the **characteristics of typical customers** who are ideal, potential users for the new SaaS solution.

**Do** describe whether it will be a B2B or B2C solution.

**Do** include quantitative data (e.g. typical size of a customer in number of users, number of transactions, duration of use of the solution in hours/month, etc.).

**Do** include information about customers' locations (e.g. countries, languages, etc.).

**Consider** specific technical limitations of you customers concerning internet access (e.g. particularly slow or unstable internet access).

**Consider** mentioning expected changes in customer characteristics of the SaaS solution's target group (e.g. first we focus on..., later we extend our target group to...).

**Consider** mentioning real-world examples of customers (e.g. existing customers, well-known companies, examples from focus groups, etc.).

## Number of Customers

> Describe the anticipated **number of customers** short-term, mid-term, and long-term.

**Do** specify the planned number of customers and the planned number of users.

**Consider** describing multiple scenarios (e.g. optimistic, pessimistic).

**Do** estimate the numbers per pricing model (see also separate question below), if you plan to offer different pricing models. This is especially important if there will be a high-volume free or [freemium](https://en.wikipedia.org/wiki/Freemium) plan.

**Consider** adding expected churn and conversion rates.

## Usage Characteristics

> Describe the anticipated **usage scenarios and patterns** for typical customers.

**Do** mention predictable usage spikes (e.g. end of month, certain events, etc.).

**Do** mention time ranges with predictable below-average usage (e.g. night, weekend, etc.).

**Do** describe the most important business transaction types and their expected volume per timeframe. **Consider** limiting yourself to the five most important ones.

**Consider** mentioning at least boundaries if exact numbers have not been worked out yet (e.g. at least x transactions per month per user..., not more than y transactions per second..., etc.).

**Consider** describing usage scenarios from a customer's perspective (e.g. uses smartphone for certain scenarios while traveling). **Consider** limiting yourself to the five most important ones.

**Don't** go into too much details. Rough estimations that demonstrate the fundamental concepts are enough.

## Data Characteristics

> Describe the anticipated **data volume and structure** of a typical customer.

**Do** focus on the outstanding aspects (e.g. entities with the by far largest number of instances).

**Don't** include detailed technical data models. They will be worked out during the implementation project. Focus on the business view instead.

**Consider** describing especially complex data structures from a business point of view (e.g. graph data structures, data structures with complex time reference, etc.).

**Don't** go into too much details. Rough estimations that demonstrate the fundamental concepts are enough.


# Product

## Client Technology

> Describe **specific requirements** of customers regarding **client technology** (e.g. important client devices, browser support, etc.).

**Don't** include detailed UI specification here.

**Don't** go into too much technical detail. Focus on the user's perspective instead.

**Do** focus on differentiators (e.g. best user experience on iPhone, available on any device, etc.) instead of describing usually assumed client and UI features.

**Do** mention specific business requirements for certain client technologies (e.g. must support a specific browser version, must run on a specific Android version, must support certain screen sizes, etc.). **Consider** describing the reasoning behind it.

**Avoid** being vague and subjective (e.g. easy to use, self-describing).

**Consider** describing the need for supporting temporary offline work. Describe the business scenarios from a customer's point of view that should be enabled by offline capabilities.

## API

> Describe the **role of APIs** for the new SaaS solution.

**Don't** go into technical details. Focus on the business scenarios and the reasoning behind the APIs instead.

**Do** describe the target group for APIs (e.g. partners building plugins, integration scenarios built by power users). **Consider** describing their typical background (business and technology).

**Do** describe the most important business scenarios enabled by adding a public API to the SaaS solution. **Consider** limiting yourself to the five most important ones.

## Extensibility

> Describe necessary feature for **customer-specific extensions and customizations**.

**Don't** go into technical detail.

**Do** describe the most important business scenarios enabled by the required extensibility mechanisms. **Consider** limiting yourself to the five most important ones.


# Business Model

## Calculation

> Describe the **revenue and cost calculation** for the new SaaS solution.

**Do** describe the planned pricing model (e.g. price plans, volume scaling, freemium offerings, free pricing tier, etc.).

**Do** describe the budget and its structure for building and running the SaaS solution ([TCO](https://en.wikipedia.org/wiki/Total_cost_of_ownership), not just server costs).

**Consider** mentioning at least boundaries if exact numbers have not been worked out yet (e.g. must not be more expensive than..., we will charge at least..., etc.).

**Don't** go into too much details. Rough estimations that demonstrate the fundamental concepts are enough.

**Consider** adding a rough [customer lifetime value](https://en.wikipedia.org/wiki/Customer_lifetime_value) calculation for a typical target customer.

## Supporting Service

> Describe the planned **supporting services** for the new SaaS solution (e.g. self-service administration portal, web-based support portal, automated rating and billing, etc.).

**Do** add quantitative data if available (e.g. number of anticipated support requests per user per year).

**Do** add any specific requirements regarding standards or certifications (e.g. documentation for ISO certification, applicable legal requirements for invoices, etc.).


# Time Frame

> Describe important **dates for milestones** relevant for the SaaS project (e.g. important trade shows, presentation for venture capitalists, etc.).

**Do** describe the features that are absolutely necessary for each milestone.

**Consider** the concept of the [Minimum Viable Product](https://en.wikipedia.org/wiki/Minimum_viable_product).


# Technology

## Technological Restrictions

> Describe technological restrictions that the current project has to comply with (e.g. use of certain programming languages or frameworks).

**Don't** go in too much detail. If available, add references to existing documents and guidelines (e.g. [software design](https://en.wikipedia.org/wiki/Software_design) guidelines, description of methodologies like [*12factor*](https://12factor.net/)).

**Consider** describing the reasoning behind the restriction.

**Do** reference standards (e.g. standardized communication protocols, standard regarding data security, industry standards) that the project has to implement. **Consider** describing the reasoning why the standards are relevant.

**Avoid** subjective opinions (e.g. "we don't believe that x has a future"), **prefer** references to objective facts (e.g. decreasing adoption rate according to GitHub statistics or large-scale polls).

## Known Technical Risks

> Describe known technical risks and unsolved challenges (e.g. from previous projects, from research projects) that can already be anticipated.

**Don't** go in too much detail. If available, add a reference to more detailed documents (e.g. research project results).

**Consider** limiting yourself to the five most important risks and challenges that could lead to a failed project as a whole.

## Existing Artifacts

> Describe **existing components that have to be used** in the SaaS development process (e.g. existing code base, third-party components that must be used, interfaces to existing systems, etc.).

**Don't** go into the technical details.

**Do** focus on existing components that have to be reused because of certain business requirements (e.g. algorithm which is part of a standard, existing contracts, presence on a certain digital market place, etc.). **Consider** describing the reasoning behind it.

**Consider** adding a [system context diagram](https://en.wikipedia.org/wiki/System_context_diagram) to describe the necessary interactions with existing, external systems.

**Consider** adding references to documentation and/or persons that could be useful during a more detailed, technical analysis.

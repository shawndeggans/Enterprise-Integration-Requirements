# Enterprise-Integration-Requirements
The Enterprise Integration Requirements is a set of documents and tools to help an integration team consider, plan, and execute a medium to large scale integration project. 

## Higher-level Integration Goal
*Overall Goal of the Integration*

State the goal of the overall integration using your favorite user story format.

Example: To achieve the business goal of seamlessly moving geological survey data from the Azure Data Lake to Salesforce, the exploration team needs an integration between the two systems with guaranteed delivery of event data in the form of JSON. Additionally, the mobile development team needs a REST API that provides access to the exploration team's geological summary report. 

*Enterprise Architecture Decision for Integration*

State the defense for architectural choices.

Example: Because of its built-in connectors and ease-of-use, the Integration Team has selected Mulesoft as the primary technology to help deliver data from the Azure Data Lake to Salesforce. Mulesoft will provide REST API in the form of a process layer and an experience layer for the mobile development team. The integration team will also make use of Azure Data Factory to transform and extract geological survey data, and the integration team will build microservices to facilitate data enrichment for the experience layer. 

*High-level Business Requirements*

Gather basic business requirements in the form of Assert must, shall, will, will not.

Integration shall align geological survey data to the correct salesforce account of the geologist.

Integration Mechanisms
======================

Event-driven Mechanisms
-----------------------

[Enterprise Integration Patterns - Event Driven Consumer](http://www.enterpriseintegrationpatterns.com/patterns/messaging/EventDrivenConsumer.html "Event Driven Consumer")
[Event Collaboration - Martin Fowler]
(https://martinfowler.com/eaaDev/EventCollaboration.html)

Triggering frequency

Cadence

Performance Feasibility

Synchronous / Asynchronous Response Types
-----------------------------------------

Maximum possible size of response

Maximum possible response time

Performance Feasibility

Batch Processing
----------------

Batch Size

Batch Update Frequency

Performance Feasibility

Routing/Transformations/Composite Services
==========================================

Message Delivery
----------------

Message loss acceptance

Message loss exception strategy

SLA
---

Service Level Agreement Parameters

Message Integrity
-----------------

Duplication and Idempotent strategy

Single Message or Message Sequence

Message Sequence Order of Operation and Order of Delivery

Conflict Resolution Strategy for Multiple Sources of Truth

Availability
------------

Required Quality of Service

Inbound Services
================

Service Contract
----------------

Define the Inbound Service Contracts

Mapping
-------

API to Entity

Transaction Boundaries
----------------------

Transactional or Non-Transactional Steps

Inbound Message
---------------

Corrupt / Bad Message Response

Handling

Entity Creation
---------------

Identifier handling

System of Record

Attribute level mapping

Outbound Services/Event Publishers
==================================

Service Contract
----------------

Define the Outbound Service Contract

Outbound Transformation
-----------------------

Outbound Contract Verification

Events
------

Event Contract

Trigger definition

Loop handling

Quality of Service
------------------

Promised Contract

Canonical Data Model / Integration Model
========================================

CDM Identifiers
---------------

Mappings

Source Systems

Master System Attributes

Attribute/Value Representation
------------------------------

Meta-attributes

Value Patterns

Formal and Informal Attribute Structures

CDM Vocabulary
--------------

Definitions

Application Mappings

Mapping Maintenance Procedures

Enumerations
------------

Concrete Values

Schema Validation

Artifact Vocabulary 
--------------------

Context mapping

Noun/Action Mapping

Error Handling
==============

Feature Set
-----------

Integration Exceptions

Incident Process

API Exceptions
--------------

Exception Taxonomy Definition

Error Messaging
---------------

Error Explanations

Error Notification Plan

Machine Handling
----------------

Status Codes

Business Events Handling
========================

Primary Business Events
-----------------------

Business events for telemetry

Business events for tracking

Business events to Publish for Subscribers

Key Processes
-------------

Tracking key processes

Transactions
------------

Before and after states

Meaningful transaction ids

Replay
------

Business event transactional replay

Security
========

Credentials
-----------

Inbound / Outbound Credential Requirements

Encryption
----------

Message Encryption

Password storage

NPI Transport

Log obfuscation

DevOps / Maintenance
====================

Incident Taxonomy
-----------------

Reaction to Incident Scenarios

Operation procedures

Logging
-------

DevOps logs

Log management policy

Outages
-------

Emergency loss handling

Monitoring 
-----------

Considerations

Context

Incidents

HealthCheck API / Flows

Mulesoft Microservice Environments
==================================

Development
-----------

Dev details

Quality Assurance
-----------------

QA details

Production
----------

Prod details

General
=======

Big Picture
-----------

Clear Definition

Open Issues

Assumptions Checked

Dependencies Known

Compliance

Requirements Met

Delivery Team
=============

-   EIS contacts

-   Partner contacts

-   Enterprise solution contacts

-   Product owner contacts

-   QA contacts

-   BA contacts

-   Security contacts

-   DevOps contacts

Sign-off 
=========

System and Architectural Stakeholders agree to the accuracy of the information
in this document and accept it as the integration scope-of-work.

| **Approver Name** | **Department** | **Signature** | **Date** |
|-------------------|----------------|---------------|----------|
|                   |                |               |          |
|                   |                |               |          |
|                   |                |               |          |
|                   |                |               |          |
|                   |                |               |          |

Credits
==========
I've built this document from the original work of Peter Rajsky. Peter's "Personal Checklist of Integration Architect," was
instrumental in helping to guide me through my first few large integrations. [Personal Checklist of Integration Architect](https://it.toolbox.com/blogs/peterrajsky/personal-checklist-of-integration-architect-121708, "Personal Checklist of Integration Architect")

The Bible of Enterprise Integration (http://www.enterpriseintegrationpatterns.com, "Enterprise Integration Patterns by Gregor Hohpe and Bobby Woolf")

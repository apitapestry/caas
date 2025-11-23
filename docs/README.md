# Contract as a Service (CaaS)

Contract-as-a-Service (CaaS) is a **runtime engine that reads an OpenAPI contract and turns it into a fully functional CRUD API**.
Instead of generating code from the contract ("contract-first") or documenting code after the fact ("code-first"), the
contract itself becomes the product: a single source of truth that the platform executes.

You provide a well designed openapi contract. The CaaS runtime reads that contract and provides a functional API. 
Your development team spends less time implementing endpoints and more time designing clear, consistent contracts and 
focusing on business logic.

## What is Contract as a Service?

**Contract-as-a-Service (CaaS)** is an architecture in which a generic runtime engine interprets an API contract (typically an OpenAPI document) at runtime to expose a production-ready API, with most behavior specified declaratively in the contract.

Instead of generating code from the contract or documenting code after the fact, the contract itself becomes the executable specification that drives the runtime.

## Key Principles

1. **Contract is the primary source of truth** - The OpenAPI contract defines resources, operations, schemas, validations, and runtime behavior
2. **Runtime is contract-agnostic** - A single, reusable runtime can host many APIs across different teams and domains
3. **Business logic lives at the edges** - Complex workflows are moved to event-driven services, not embedded in API controllers

## Why CaaS?

Most organizations struggle with:

- **API sprawl** – dozens or hundreds of services, each slightly different
- **High maintenance cost** – every service re-implements the same security, logging, and database interactions
- **Slow time-to-market** – weeks or months to stand up a "simple" CRUD API

CaaS solves these problems by moving behavior into the contract and centralizing the runtime. When all repetitive boilerplate is handled once in the platform, teams can ship new APIs dramatically faster.

## Benefits

- **Time-to-market** - Go from idea to working API in minutes instead of weeks
- **Lower maintenance** - Evolve contracts, not scattered service code
- **Consistency by design** - Security, logging, monitoring applied consistently to every API
- **Clear separation of concerns** - CRUD operations in the runtime, business logic in event-driven services

## Getting Started

- [Problem & Motivation](problem.md) - Understand the challenges CaaS addresses
- [Core Concepts](core-concept.md) - Learn the fundamental ideas behind CaaS
- [Overview](overview.md) - High-level introduction to CaaS

## Design & Implementation

- [Contract Design](contract-design.md) - How to design contracts for CaaS
- [Business Logic Patterns](business-logic.md) - Where business logic fits in the CaaS model
- [Architecture & Runtime](architecture.md) - How CaaS fits into your system
- [Adoption](adoption.md) - How to adopt CaaS in your organization

## Implementations

CaaS is a design pattern and architecture. Multiple implementations can exist:

- **[APIstry](https://github.com/apitapestry/apistry)** - A Node.js/Fastify-based CaaS runtime with MongoDB integration


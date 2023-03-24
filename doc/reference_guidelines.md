# Reference guidelines

Status: **DRAFT**

## Design criteria

What does make a good design? Here is a set of quality criteria.

ID | Name | Description
--- | --- | ---
QC-1 | Readability | A self-documented design that makes the architecture layers, patterns, and principles explicit.
QC-2 | Sustainability | A design which foundations can survive the continuous changes caused by the flow of new functionalities.
QC-3 | Maintainability | A design that allows for corrections and improvements at low cost.
QC-4 | Extendability | A flexible design that can be extended to support new functionality at low cost.
QC-5 | Testability | A component design that allows testing in isolation at low cost.

These quality criteria are supported by a set of standard design principles and standard design patterns.

## Design principles

A design principle is a standard design rule or guideline that has to be applied consistently. It aims to guide the designer towards building a good design.

ID | Name | Description
--- | --- | ---
P-1 | Single responsibility | SRP: One component should have only one reason to change; To increase the cohesion between components that change for the same reasons, and to decrease the coupling between those components that change for different reasons.
P-2 | Open-Close | OPC: In Object-Oriented Programming, one class' behaviour should be extended without being modified; One component class should be open for extension but closed to modification.
P-3 | Interface segregation | ISP: To define fine grained interfaces that are client specific; No client should be forced to depend on methods it does not use.
P-4 | Dependency inversion | DIP: One component should only depend on abstractions of its dependent components.
P-5 | Inversion of control | The resolution of the references to the dependent components is delegated to a specific framework.
P-6 | Low coupling | To minimize the impact of changes applied to dependent components; To decrease the coupling between components that change for different reasons.
P-7 | High cohesion | To focus the interface and behaviour of one component on its one original intention; To increase the cohesion between components that change for the same reasons.
P-8 | Domain-driven | Intensive use of the domain language and concepts; Protection of local domain languages with anti-corruption boundaries.
P-9 | Logical models segregation | Every architecture layer should have its own object model.

## Design patterns

A design pattern is a standard, well-known, approved, reusable piece of design. It acts as a blueprint for solving similarly structured problems. It focuses on a structural or a behavioural aspect.

ID | Name | Solves
--- | --- | ---
PAT-1 | Hexagonal architecture | Provides a clear separation between core and infrastructure logic; Organises the architecture layers like an onion with the domain layer at its centre.
PAT-2 | Ports and adapters | Integration of the architecture layers in an onion-like organisation with centre-oriented dependencies; definition of ports as APIs, and adapters following the dependency inversion principle.
PAT-3 | Dependency injection | Implements the Inversion of control principle; Defers and delegates the resolution of dependent components at runtime.
PAT-4 | Proxy | Integration of an aspect onto an existing component keeping its interface.
PAT-5 | Adapter | Translates a concept of an external domain language into the local one.
PAT-6 | Repository | Tactical DDD pattern for designing a storage abstraction dedicated to a given domain entity.
PAT-7 | Application service | To design an orchestration at the use case level.
PAT-8 | Domain service | To design an orchestration at the domain level.
PAT-9 | Domain entity | To design a domain object with its identity, state, behavior, and lifecycle.
PAT-10 | Value object | To design an immutable and volatile object as a domain or application concept.
PAT-11 | Data transfert object | To design a value object that vehicles data when communicating with a user or an external system.
PAT-12 | Client | Integration and communication with an external system.
PAT-13 | Listener | Reception of events or commands from a message broker.
PAT-14 | Handler | Handling of events or commands from a client.
PAT-15 | Publisher | Sending of events or commands to a message broker.
PAT-16 | Command | To conceptualize the intent of changing the state of a certain context; To decouple a caller and a callee.
PAT-17 | Event | To conceptualize a state change in a certain context; To decouple a caller and a callee; To promote the reactive paradigm.
PAT-18 | Controller | To route an upfront request to downstream application services.
PAT-19 | Strategy | To abstract a familly of algorithms or to encapsulate a specific algorithm.

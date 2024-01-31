<h1>Notes about Microservices</h1>

<h3>What is a Monolithic application?</h3>

A monolith contains all the Routing, Middlewares, Business Logic, and Database Access to implement all the features of the app.

Microservices:

A single microservice contains all the Routing, Middlewares, Business Logic, and Database Access to implement ONE FEATURE of the app.

Communication between different Services:

Syncronis vs Asyncronis

Sync - Services communicate with each other using direct requests (HTTP, JSON, etc.)
Async - Services communicate with each other using events

	- Method 1: Events are stored in an Event Bus. The event bus is accessable by multiple services and send and receives events to the different services to retrieve all needed information.
	- Method 2: Have a DB for each service which duplicates data from other services if that information is needed to complete the service's tasks. To populate the DB, events are automatically emitted by the original service to the Event Bus for retrieval by any other services that care.
	
Postman: Used for API calls (Get/Post).

Component: A web page, or part of a webpage that has a function


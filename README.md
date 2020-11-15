Period-2 Node, Express with TypeScript, JavaScript Backend Testing, MongoDB and Geo-location

## Explain Pros & Cons in using Node.js + Express to implement your Backend compared to a strategy using, for example, Java/JAX-RS/Tomcat

PROS:
- Same language in frontend and backend
- High performance and speed (event-driven, non-blocking IO)
- Great choice for microservices because it’s lightweight
- Easy to code share because of NPM packages
- Massive NPM library
- better efficiency and overall developer productivity
- It’s simpler and requires minimum setup to use.
CONS:
- Its not suited for CPU intensive tasks because it’s single threaded
- Harder to write good async code to avoid callback hell

## Explain the difference between Debug outputs and ApplicationLogging. What’s wrong with console.log(..) statements in our backend code.

TODO

## Demonstrate a system using application logging and environment controlled debug statements.

TODO

## Explain, using relevant examples, concepts related to testing a REST-API using Node/JavaScript/Typescript + relevant packages

TODO

## Explain a setup for Express/Node/Test/Mongo-DB development with Typescript, and how it handles "secret values",  debug and testing.

You can use environment variables to handle these. In Kubernetes I will use something called secrets which I can make available to the pods(applications) and when the application starts up it will check for env variables.

## Explain, preferably using an example, how you have deployed your node/Express applications, and which of the Express Production best practices you have followed.

I will use Argocd to deploy pods(node/express servers) on my Kubernetes cluster. It uses an approach called GitOps which means it will watch my Docker Repo for new changes, and will deploy a new pod  of my application if it detects a newer version.

## Explain possible steps to deploy many node/Express servers on the same droplet, how to deploy the code and how to ensure servers will continue to operate, even after a droplet restart.
The applications are each in their own pod, which is isolated from other processes, so you can deploy as many as you want without thinking of them using the same ports etc.

## Explain, your chosen strategy to deploy a Node/Express application including how to solve the following deployment problems:
- Ensure that you Node-process restarts after a (potential) exception that closed the application
- Ensure that you Node-process restarts after a server (Ubuntu) restart
- Ensure that you can run “many” node-applications on a single droplet on the same port (80)
If the pod crash Kubernetes will make sure to restart the pod automatically.
I use something called ingress which will direct http/https traffic to the right service (application) based on domain or subdomain or path or all.


## Explain, using relevant examples, the Express concept; middleware.

Middlewares are functions which have access to the request and response object. You can for example implement middleware which check that all the required data is in the request body and if not it throws an error.

## Explain, using relevant examples, your strategy for implementing a REST-API with Node/Express  + TypeScript and demonstrate how you have tested the API.

## Explain, using relevant examples, how to test JavaScript/Typescript Backend Code, relevant packages (Mocha, Chai etc.) and how to test asynchronous code.

# NoSQL and MongoDB 
## Explain, generally, what is meant by a NoSQL database.

In most cases it means that it’s a database which stores data in a format other than relational tables

## Explain Pros & Cons in using a NoSQL database like MongoDB as your data store, compared to a traditional Relational SQL Database like MySQL.

PROS:
- Easier to use because you don’t have to make object-relational mapping
- Flexible data model which can evolve with requirements
- Easier to scale with sharding
- Faster because the data is put in documents and not spread across multiple tables
- More natural syntax – especially if you already know JSON

CONS:
- Stores redundant data

## Explain about indexes in MongoDB, how to create them, and demonstrate how you have used them.
TODO

## Explain, using your own code examples, how you have used some of MongoDB's "special" indexes like TTL and 2dsphere and perhaps also the Unique Index.
Demonstrate, using a REST-API designed by you, how to perform all CRUD operations on a MongoDB

## Explain, using a relevant example, a full JavaScript backend including relevant test cases to test the REST-API (not on the production database)
      Demonstrate, using your own code-samples, decisions you have made regarding → normalization vs denormalization 
Geo-location and Geojson
## Explain and demonstrate basic Geo-JSON, involving as a minimum, Points and Polygons
TODO 
## Explain and demonstrate ways to create Geo-JSON test data
TODO
## Explain the typical order of longitude and latitude used by Server-Side APIs and Client-Side APIs
TODO
## Explain and demonstrate a REST API that implements geo-features, using a relevant geo-library and plain JavaScript
TODO 
## Explain and demonstrate a REST API that implements geo-features, using Mongodb’s geospatial queries and indexes.
TODO 
## Explain and demonstrate how you have tested the gameFacade and gameAPI for the game-related parts of the period exercises


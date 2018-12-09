# Notes on GraphQL

GraphQL is independent on any specific database management system
It has single URL for data procurement and alteration. User can request a dataset from the server by altering query string.
`REST` is more about API's durability. It is structural conceptualization for network-centric software and there is no specification and not definite set of tools. It is an architectural style for developing web services.
On the other hand, `GraphQL` is only a query language. It supports declarative data fetching. The user can only get what they actually need. It rebounds only the data that's needed so recent facilities can be included through latest types and fields without triggering a breaking change. It is easier to deprecate a field in GraphQL.

Dataloader is a utility that can be used to read the data and make it accessible to the GraphQL functions. It uses blend of cachking and batching. It also cache the responses and provides them for consecutive queries for similar requests.

GraphQL exposes single endpoint to enable the client to determine what it prefers.

Mutations include `create`, `update` (combination of them would be named as `upsert`) and `delete`.

## Links

- [GraphQL Docs](https://neo4j.com/)
- [FreeCodeCamp](https://medium.freecodecamp.org/so-whats-this-graphql-thing-i-keep-hearing-about-baf4d36c20cf)
- [World Cup GraphQL](https://medium.freecodecamp.org/building-the-2018-world-cup-graphql-api-fab40ccecb9e)

## Further Research

- [Graph DBs](https://neo4j.com/)

[![Open in CodeSandbox](https://img.shields.io/badge/Open%20in-CodeSandbox-blue?style=flat-square&logo=codesandbox)](https://codesandbox.io/s/github/neo4j-contrib/training-v3/modules/graphql-apis/supplemental/code/02-graphql-apis-overview-of-neo4j-graphql/begin?file=/schema.graphql)

# Bookstore GraphQL API

This directory contains a Node.js GraphQL API application using [`@neo4j/graphql`](https://www.npmjs.com/package/@neo4j/graphql).

Try it live on CodeSandbox [here](https://codesandbox.io/s/github/neo4j-contrib/training-v3/modules/graphql-apis/supplemental/code/02-graphql-apis-overview-of-neo4j-graphql?file=/schema.graphql)

## Setup

First, edit `.env`, replacing the defaults with your database connection string, user, and database (optional):

```
NEO4J_URI=
NEO4J_USER=
NEO4J_PASSWORD=
```

Next, install dependencies.

```
npm install
```

Then start the API application,

```
npm run start
```

This will start a local GraphQL API server at `localhost:4000`.

## Example GraphQL Queries

```GraphQL
{
  books {
    title
    reviews {
      rating
      text
      author {
        username
      }
    }
  }
}
```

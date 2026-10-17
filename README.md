# GraphQl-Api-Testing-with-Postman-javaScript-

# GraphQL API Testing — Postman

Postman collection for practicing GraphQL queries and mutations with dynamic variables.

## API

- Endpoint: `https://rahulshettyacademy.com/gq/graphql`
- Existing requests: `mutationReq`, `QueryReq`, `createEpisode`
- Scenarios: create a location, fetch it by its returned ID, create a character linked to that location, and verify the response.

Use **POST → Body → GraphQL** for mutations. Read-only queries can use GET with `query` and `variables` parameters. Tests check the GraphQL `errors` field as well as the HTTP status.

## Run with Newman

Requirements: Node.js/npm, Newman, and the HTML reporter.

```cmd
npm install --global newman newman-reporter-htmlextra


**Newman command alag se:**

```cmd
newman run ".\GraphQL.postman_collection.json" -r cli,htmlextra --reporter-htmlextra-export ".\graphql-report.html" --reporter-htmlextra-skipSensitiveData

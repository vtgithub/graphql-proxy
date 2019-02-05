# graphql-proxy
A custom springboot proxy implemented by zuul for sending graphql batch request to multiple microservices.

* Change application.yml file and set you microservice config. Here is a sample config:
  --- 
  server:
  port: 5050
zuul:
  routes:
    graphql:
      path: "/graphql/**"
graphql:
  microList[0]:
    url: "http://localhost:4041/graphql"
    schemaFilePath: "path-to-schema"
  microList[1]:
    url: "http://localhost:4042/graphql"
    schemaFilePath: "C:/Users/v.tavakolpour/Downloads/graphql-schema/schema_micro2.graphql"
    
  ---

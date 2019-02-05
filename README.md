# graphql-proxy
A custom springboot proxy implemented by zuul for sending graphql batch request to multiple microservices.

* Change application.yml file and set you microservice config. Here is a sample config:
  ``` 
  server:
    port: 5050
  zuul:
    routes:
      graphql:
        path: "/graphql/**"
  graphql:
    microList[0]:
      url: "microservice-url"
      schemaFilePath: "path-to-schema"
  ```


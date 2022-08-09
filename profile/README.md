The purpose of this Organziation is to function as a single source for bootstrapping an entire web application.
This organization is divided up into repositories as follows: Api, Gui, Artifactory, Schema, Db, Artifact Repository Manager.

The Web Application leverages OpenApi, Spring, Maven, React, Restless, Postman, Newman, Docker, Jenkins, Jest, and Storybook.

OpenApi and the subsequent YAML files defined within the Schema repo sets the ground work for how all the repositories are interconnected. A single YAML with the use of openapi-generator-cli will create both the server-side and client-side API's for all the endpoints defined in such YAML file. Furthermore, this same yaml file will be used to generate the Postman Collections that developers can use for both development purposes as well as for testing. Within the Postman application developers will then be able to construct unit/integration tests against a live server. This will then be exported back into the source code to be played within the CI/CD as defined within Jenkins. 

Frontend developer will have procedurially generated API's for each of their endpoints. Hooks provided will enable testers the ability to cut into the internals of the fetching API and inject assertions before, after, or on error. The implementation of Restless allows frontend developers to simulate a backend for which unit/integration tests can be accurately and rigurously hardened. Storybook will also be able to leverage the mock endpoints for the purposes of imitating a real application, without the burden of building and deploying external dependencies. 

Jenkins will be used for CI/CD and the artifacts created from such process will later be stored in Nexus.

Each component is developed such to be compatible within a microservice ecosystem.

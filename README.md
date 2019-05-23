# AWSIoTProject

This repo is for the collection of information and progress tracking of the 10mi2 AWS IoT Project

# Documentation

Please see the [wiki](https://github.com/10mi2/AWSIoTProject/wiki) for documentation.

# Milestones

- [x] AWS [IoT Writeup](https://docs.google.com/document/d/1sBggp7f5gFwUyEXlZdw8z2d6sxHFrxzkvh7kkr5OD_M/edit?usp=sharing) (readable to all of 10mi2, outside of 10mi2 needs permission to read)

- [x] Node-based GraphQL Server (with in-memory database) - using Apollo Server, business logic <200 lines of code
- [x] [Configurator](https://github.com/synthetos/fabmo-g2core-config) converted to use GraphQL for schema and backend instead of REST + custom schema DSL
  - Updated to latest Angular (8)
  - Repo name needs to be changed
- [x] Configurator project configured to enable and use VSCode extensions for live debug, editing with static-analysis and autoformatting
  - More automated testing work needed
- [x] Inital testing installing and activating GreenGrass on a Raspbery Pi, and pushing an active and functioning lambda to it
- [x] Automated provisioning of GreenGrass cloud components with CloudFormation
- [ ] Create a Lambda that has a physical action (light blinks, button-push shows change on AWS IoT dashboard)
- [ ] Wire AWS Cognito into GraphQL server and Configurator for Auth
- [ ] Create GreenGrass Lambda form of GraphQL Server for local control, *and* cloud GraphQL server on device shadow. 
  - [ ] Wire Configurator to be able to connect either way
- [ ] Complete GraphQL server functionality to talk to physical G2 hardware, and add IoT Job handling functionality
- [ ] Handle provisioning and packaging for productized hardware for these four scenarios:
  - Primary concern is security, where the product is effectively open to the customer, while still providing easy onboarding
  - [ ] Direct-to-consumer product - manufacturer is also the service provider to many customers
  - [ ] OEM - multiple manufacturers are sharing the same service provider to many customers
  - [ ] Enterprise - the manufacturer is the service provider and the customers
  - [ ] OEM with enterprise customer - the customer will also be the service provider, but not the product manufacturer

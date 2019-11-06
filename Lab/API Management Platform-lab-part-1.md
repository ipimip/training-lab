# API Management Platform Hands-On Lab - Part 1

You will have been assigned a particular service to work on for the following exercises, throughout this document it will be referred to as `your API`.

The following exercises are designed to provide a basic understanding of how the API Management Platform works at IPIM-IP, the end of this lab links your new API Policy to the mock server hosted by Apiary, in order to do this please ensure you have a set of working endpoints from the [Apiary lab](https://git.build.ingka.ikea.com/IPIM-IP/training-lab/blob/master/Lab/Apiary-lab.md).

If you encounter any issues during the following exercises please ask one of the on-site support team for help.

## Table of Contents

- [API Management Platform Hands-On Lab - Part 1](#api-management-platform-hands-on-lab---part-1)
  - [Table of Contents](#table-of-contents)
  - [Setup](#setup)
    - [Required Tools](#required-tools)
    - [Useful URLs](#useful-urls)
  - [Section 1 - Introduction to API Management Platform](#section-1---introduction-to-api-management-platform)
    - [Exercise 1: API Management Platform](#exercise-1-api-management-platform)
      - [Exercise 1 - Required Tools](#exercise-1---required-tools)
      - [Exercise 1 - Task](#exercise-1---task)
        - [API](#api)
        - [Plan](#plan)
        - [Application](#application)
      - [Exercise 1 - Success Criteria](#exercise-1---success-criteria)
  - [Section 2 - Creating API Policies](#section-2---creating-api-policies)
    - [Exercise 2: Creating a Policy](#exercise-2-creating-a-policy)
      - [Exercise 2 - Required Tools](#exercise-2---required-tools)
      - [Exercise 2 - Task](#exercise-2---task)
      - [Exercise 2 - Success Criteria](#exercise-2---success-criteria)
  - [Section 3 - Creating a plan](#section-3---creating-a-plan)
    - [Exercise 3: Creating a plan](#exercise-3-creating-a-plan)
      - [Exercise 3 - Required Tools](#exercise-3---required-tools)
      - [Exercise 3 - Task](#exercise-3---task)
      - [Exercise 3 - Success Criteria](#exercise-3---success-criteria)
  - [Section 4 - Creating an Application](#section-4---creating-an-application)
    - [Exercise 4: Creating an Application](#exercise-4-creating-an-application)
      - [Exercise 4 - Required Tools](#exercise-4---required-tools)
      - [Exercise 4 - Task](#exercise-4---task)
      - [Exercise 4 - Success Criteria](#exercise-4---success-criteria)
  - [Section 5 - Deploying an API](#section-5---deploying-an-api)
    - [Exercise 5: Deploying an API](#exercise-5-deploying-an-api)
      - [Exercise 5 - Required Tools](#exercise-5---required-tools)
      - [Exercise 5 - Task](#exercise-5---task)
      - [Exercise 5 - Success Criteria](#exercise-5---success-criteria)
  - [Section 6 - Developer Portal](#section-6---developer-portal)
    - [Exercise 6: Developer Portal](#exercise-6-developer-portal)
      - [Exercise 6 - Required Tools](#exercise-6---required-tools)
      - [Exercise 6 - Task](#exercise-6---task)
      - [Exercise 6 - Success Criteria](#exercise-6---success-criteria)

## Setup

After logging in to your provided virtual machine you should see your service downloaded to the machine along with the Oracle API Management Platform Cloud application which is an Internet Application bookmarked in your Internet Browser.

If the application is not bookmarked then it can be accessed at the below URL:

- [API Management Platform](https://primary-ikea.apiplatform.ocp.oraclecloud.com/apiplatform)

### Required Tools

For the following exercises, the following tools are required:

- Internet Browser (Google Chrome)

### Useful URLs

- [API Gateway Lab - Part 1 (This Document)](https://git.build.ingka.ikea.com/IPIM-IP/training-lab/blob/master/Lab/Gateway-lab-part-1.md)
- [API Management Platform](https://primary-ikea.apiplatform.ocp.oraclecloud.com/apiplatform)
- [Apiary](https://apiary.io/)
- [Microservices workbench](https://confluence.build.ingka.ikea.com/display/II/%28Micro%29services+Knowledge+Base)

> Apiary Services:
>
> - [Bedroom Service](https://traininglabbedroomservice.docs.apiary.io/)
> - [Kitchen Service](https://traininglabkitchenservice.docs.apiary.io/)
> - [Living Room Service](https://traininglablivingroomservice.docs.apiary.io/)
> - [Storage Service](https://traininglabstorageservice.docs.apiary.io/)
> - [Office Space Service](https://traininglabofficespaceservice.docs.apiary.io/)

## Section 1 - Introduction to API Management Platform

You should have received an invitation to create an account within the API management application, please follow the instructions in that email to finish creating your account.

### Exercise 1: API Management Platform

This exercise is designed to familiarise yourself with the API Management Platform - As further exercises require you to edit the API for your service, please use the below API, Plan and Application for this exercise:

- [IKEA Polls Example API](https://primary-ikea.apiplatform.ocp.oraclecloud.com/apiplatform/apis/api/249/implementations)
- [IKEA Polls Example Plan](https://primary-ikea.apiplatform.ocp.oraclecloud.com/apiplatform/plans/plan/169/general)
- [IKEA Polls Example Application](https://primary-ikea.apiplatform.ocp.oraclecloud.com/apiplatform/applications/application/185/general)

#### Exercise 1 - Required Tools

- Internet Browser

#### Exercise 1 - Task

This exercise comprises of three areas to explore:

- API
- Plan
- Application

##### API

Within the API Management Platform, select the `APIs` tab and navigate to the `IKEA Polls Example API` and inspect the various policies applied on the `API Implementation` tab.

Also look at the `Grants` tab for the example API.

> API:
>
> ![alt text][apimp_api_implementation]

##### Plan

Within the API Management Platform, select the `Plans` tab and navigate to the `IKEA Polls Example Plan` and inspect the `Settings` and `Entitlements` tabs.

Be sure to drill into the APIs on the `Entitlements` tab.

> Plan:
>
> ![alt text][apimp_plan_implementation]

##### Application

Within the API Management Platform, select the `Applications` tab and navigate to the `IKEA Polls Example Application` and inspect the `Settings` and `Subscriptions` tabs.

Be sure to pay attention to the `App Key` on the `Settings` tab.

> Application:
>
> ![alt text][apimp_application_implementation]

#### Exercise 1 - Success Criteria

- [ ] Explore the `IKEA Polls Example API`
- [ ] Explore the `IKEA Polls Example Plan`
- [ ] Explore the `IKEA Polls Example Application`

## Section 2 - Creating API Policies

Useful links for this exercise:

- [API Request Policy](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/implement-apis.html#GUID-CBCE0B5C-4B69-4FF9-B8EF-7F1B452CBD86)
- [Key Validation Policy](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/implement-apis.html#GUID-5CBFE528-A74E-4700-896E-154378818E3A)
- [Interface Filtering Policy](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/implement-apis.html#GUID-69B7BC21-416B-4262-9CE2-9896DEDF2144)
- [Logging Policy](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/implement-apis.html#GUID-8685475A-4088-4D1F-A5AD-1788531D0A80)
- [Gateway Based Routing Policy](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/implement-apis.html#GUID-B31BAD46-C670-47B1-8160-7C42840D35D0)

### Exercise 2: Creating a Policy

For this exercise you will need to switch to the `APIs` tab on the left.

This exercise will introduce you to the different policies you can apply to a particular API

> _Note: **Please use your particular API for this and subsequent exercises**:_

- IPIM-IP Training Bedroom Labs API
- IPIM-IP Training Kitchen Labs API
- IPIM-IP Training Living Room Labs API
- IPIM-IP Training Office Space Labs API
- IPIM-IP Training Storage Labs API

#### Exercise 2 - Required Tools

- Internet Browser

#### Exercise 2 - Task

Currently your API only includes the Service Request policy, your task is to add/update the following policies to the API:

- API Request
- Key Validation
- Interface Filtering
- Logging
- Gateway Based Routing

#### Exercise 2 - Success Criteria

- [ ] Update `API Request` policy
- [ ] Add `Key Validation` policy
- [ ] Add `Interface Filtering` policy
- [ ] Add `Logging` policy
- [ ] Add `Gateway Based Routing` policy

## Section 3 - Creating a plan

For this exercise you will need to switch to the `Plans` tab on the left.

Useful links for this exercise:

- [Creating a Plan](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/create-plan.html#GUID-B2E28591-D009-4EBA-83A1-8FC5CBF85196)

### Exercise 3: Creating a plan

Now that you have created an API, you need to create a `Plan`, a plan is created so that a group of users can be entitled to call one or multiple APIs associated with the corresponding Plan.

Other benefits often associated with a plan are:

- Access Control - Different levels of access
- Corporate - Different bundles of APIs
- Monetization - Different levels of cost

#### Exercise 3 - Required Tools

- Internet Browser

#### Exercise 3 - Task

You need to create a new `Plan` and add an `Entitlement` for the new `API` you created in the previous exercise.

#### Exercise 3 - Success Criteria

- [ ] Create a new `Plan`
- [ ] Add a new `Entitlement` for the `API` from the previous exercise

## Section 4 - Creating an Application

For this exercise you will need to switch to the `Applications` tab on the left.

Useful links for this exercise:

- [Creating an Application](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/create-application.html#GUID-4E9B44B3-DDDE-43CF-9843-5DF710C977C5)

### Exercise 4: Creating an Application

Now that you have created an API, you need to create an Application for a particular consumer, this is done so that each specific consumer has their own relevant application and also the metrics can be tracked per application thus giving greater insight into the API statistics.

#### Exercise 4 - Required Tools

- Internet Browser

#### Exercise 4 - Task

You need to create a new `Application` and subscribe the newly created application to the `Plan` you created during the previous exercise.

#### Exercise 4 - Success Criteria

- [ ] Create a new `Application`
- [ ] Subscribe the new `Application` to the `Plan` from the previous exercise

## Section 5 - Deploying an API

For this exercise you will need to switch to the `APIs` tab on the left.

Useful links for this exercise:

- [Deploying an API](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/deploy-endpoints.html#GUID-91D6C3B1-7357-43F6-813E-2BD67FE4E251)

### Exercise 5: Deploying an API

Now that you have created your `API`, `Plan` and `Application`, it is time to deploy your `API`, deploying the `API` means that it is available for people to consume.

#### Exercise 5 - Required Tools

- Internet Browser

#### Exercise 5 - Task

For this exercise, you need to deploy your `API` to the development environment.

Within the API Management Platform, the development environment is called `PTE`.

#### Exercise 5 - Success Criteria

- [ ] Deploy `API` to PTE

## Section 6 - Developer Portal

For this exercise you will be using the `APIs` and `Plans` tabs on the left.

Useful links for this exercise:

- [Publishing APIs](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/publish-apis.html#GUID-A03CE2F9-C2B7-4976-AA32-8E95DA76F41A)
- [Publishing Plans](https://docs.oracle.com/en/cloud/paas/api-platform-cloud-um/apfad/publish-plans.html#GUID-A58CAF09-070B-4979-8A22-AFB26218EEE1)

### Exercise 6: Developer Portal

Now that you have created your `API`, `Plan`, `Application` and deployed the `API`, it is time to expose your `API` to the developers consuming from you, this is achieved by publishing the `API` and `Plan` to the `Developer Portal`.

#### Exercise 6 - Required Tools

- Internet Browser

#### Exercise 6 - Task

For this exercise, you need to publish your `API` and `Plan` to the developer portal.

#### Exercise 6 - Success Criteria

- [ ] Publish `API` to the developer portal
- [ ] Publish `Plan` to the developer portal

<!-- ## Appendix

TODO

## Frequently Asked Questions

The section below contains a list of common questions along with their corresponding answers people often ask whilst working with the tools used in this lab.

- [TODO](#todo)
- [TODO 2](#todo-2)

---

### Q: TODO

A: TODO

---

### Q: TODO 2

A: TODO -->

[apimp_api_implementation]: images/apimp_api_implementation.png "API Management Platform - API Implementation"
[apimp_plan_implementation]: images/apimp_plan_implementation.png "API Management Platform - Plan Implementation"
[apimp_application_implementation]: images/apimp_application_implementation.png "API Management Platform - Application Implementation"

# Table of content
- [Table of content](#table-of-content)
  - [Setup](#setup)
    - [Required Tools](#required-tools)
    - [Useful URLs](#useful-urls)
  - [Remote-Desktop](#remote-desktop)
  - [Introduction to (Micro)services](#introduction-to-microservices)
  - [Exercise 1: Run Service](#exercise-1-run-service)
    - [Exercise 1: Required Tools](#exercise-1-required-tools)
    - [Exercise 1: Task](#exercise-1-task)
    - [Exercise 1: Success Criteria](#exercise-1-success-criteria)
  - [Exercise 1: ASDF](#exercise-1-asdf)
    - [Exercise 1: Required Tools](#exercise-1-required-tools-1)
    - [Exercise 1: Task](#exercise-1-task-1)
    - [Exercise 1: Success Criteria](#exercise-1-success-criteria-1)
  - [Exercise 1: ASDF](#exercise-1-asdf-1)
    - [Exercise 1: Required Tools](#exercise-1-required-tools-2)
    - [Exercise 1: Task](#exercise-1-task-2)
    - [Exercise 1: Success Criteria](#exercise-1-success-criteria-2)
  - [Exercise 2: Update existing endpoints to Apiary changes](#exercise-2-update-existing-endpoints-to-apiary-changes)
  - [Exercise 3: Update with new endpoint to Apiary changes](#exercise-3-update-with-new-endpoint-to-apiary-changes)
- [BACKUP - TO BE MOVED](#backup---to-be-moved)
  - [Exercise 2: Extend Microservice](#exercise-2-extend-microservice)
    - [Model class](#model-class)
    - [Service class](#service-class)
    - [Controller](#controller)
    - [Router](#router)
  - [Exercise 3: Write Unit Tests](#exercise-3-write-unit-tests)
    - [Add Tests](#add-tests)
- [CICD Lab](#cicd-lab)
  - [Exercise 1: Push to develop](#exercise-1-push-to-develop)
  - [Exercise 2: Test service](#exercise-2-test-service)

## Setup

### Required Tools
For the following exercises, the following tools are required and available in the provided remote VM:

- Internet Browser (Google Chrome)
- API Client (Postman)
- IDE (VS-Code)
- GIT

### Useful URLs
- [Git-repo for training lab](https://git.build.ingka.ikea.com/IPIM-IP/training-lab)
- [APIary](https://traininglabbedroomservice.docs.apiary.io/)
- [Confluence Knowledge Base](https://confluence.build.ingka.ikea.com/display/II/IPIM-IP+-+Knowledgehttps://confluence.build.ingka.ikea.com/display/II/IPIM-IP+-+Knowledge)
- [Microservices workbench](https://confluence.build.ingka.ikea.com/display/II/%28Micro%29services+Knowledge+Base)
- [CICD workbench](https://confluence.build.ingka.ikea.com/display/II/CICD+Knowledge+Base)
- [Jenkins](https://jenkins.westeurope.svc.hip.red.cdtapps.com/)

## Remote-Desktop 
Remote desktop to server: XXX
Username: ipim\beedromUser
Password: XXX

On your Remote-desktop virtual machien, you will find tools like:
- Postman
- VS Code
- Git
- Notepad++

## Introduction to (Micro)services

Now that your Apiary document is updated with a new endpoint, it's time to adjust the existing Microservice!

<p>
Login to your remote desktop, and open up VS Code. <br />

Click on `File -> Open Folder -> C:\Users\Administrator\"YourLabService"`

</p>
"YourLabService" should be the lab you have been assigned, for example the bedroom-service

<p>

Click on the two folders overlapping eachothers in the top-left corner to view the explorer again. 

Navigate to `"src\main\java\com\ikea\ipim\training\web\router"` and view the Router-class. 

Check the API resource-path and open up postman to make example queries to: `http://localhost:8080/<resource-path>`.

</p>

## Exercise 1: Run Service
The exercise is designed to understand how to start the service and the functionality it contains.

### Exercise 1: Required Tools
- VS Code
- Postman

### Exercise 1: Task
Click on `"Debug" -> "Start Debugging"` (or press F5) to compile and run application. 
You'll see the service starts building in the terminal in the bottom. Once it says:

```
"Started TrainingLabBedRoomRoomApplication in 13.059 seconds (JVM running for 19.056" the service is started.
```

### Exercise 1: Success Criteria
- [ ] Start service successfully
- [ ] Test API - Get All
- [ ] Test API - Get by Id
- [ ] Test API - POST
- [ ] Test API - Health
- [ ] Test API - Info

## Exercise 1: ASDF
TODO

### Exercise 1: Required Tools
TODO

### Exercise 1: Task
TODO

### Exercise 1: Success Criteria
TODO

## Exercise 1: ASDF
TODO

### Exercise 1: Required Tools
TODO

### Exercise 1: Task
TODO

### Exercise 1: Success Criteria
TODO

## Exercise 2: Update existing endpoints to Apiary changes
asdf

## Exercise 3: Update with new endpoint to Apiary changes
asdasd




# BACKUP - TO BE MOVED

## Exercise 2: Extend Microservice
To extend the microservice with your new endpoint previously designed in Apiary, three steps are required:
- Add a new Model-classes under `..\training\model` which should be equal to your Data structures added in Apiary.
- Add a new service under `..\training\service`
- Add a new controller under `..\training\web\controller`
- Adjust the Router-class under `..\training\web\router` with a new endpoint.

### Model class

### Service class

### Controller

### Router
For the router updates, a new method is required. You could have a look at the existing method, and make a new one, but names and classes adjusted to your previously added classes.

## Exercise 3: Write Unit Tests
To be able to verify that your method is working as intended, it's required to write unit tests. The CICD pipeline have checks in place to verify that each microservice, has a minimum test coverage of 70%. If this is not achieved, the pipeline will fail.

### Add Tests
Add a new test class under `src\test\java\com\ikea\ipim\training.`

Write test cases for all your controller method. Make sure to also write testcases for expected errors. For example, that a 404 should be returned if a resource is not find in a get by id.

# CICD Lab
Your service is developed and tested locally, now it's time to push it up development. 

## Exercise 1: Push to develop
Normally, we would have a feature branch that we would work towards, and then use a pull request to develop. But for this case, we will push directly to the develop branch.

Open up Powershell or Git Bash and change directory to your service root path. 

```git
git add .
```

```git
git commit -m "your commit message"
```

```git
git push
```

Once logged in, navigate to Jenkins that should be bookmarked in Chrome on your remote-desktop vm.

Your service should be building, or in queue to be built. Find it in the down-left side. 
- Click on the service. 
- Click on "Open Blue Ocean". 
- Check and await the build status.

## Exercise 2: Test service
asdf




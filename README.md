[![Python application test with Github Actions](https://github.com/philbier/building-cicd-pipeline/actions/workflows/pythonapp.yml/badge.svg?branch=main)](https://github.com/philbier/building-cicd-pipeline/actions/workflows/pythonapp.yml)

# building-cicd-pipeline
This is the final project for the course "Building a CI/CD pipeline" as part of of the Udacity Cloud DevOps Nanodegree

![Set up Azure Cloud Shell](./img/set_up_az_shell.png)



![Succesfull test of hello.py](./img/test_hello.PNG)



![Configure GitHub Actions](./img/configure_github_actions.png)

![GitHub Actions UI - Succesful build](./img/github_actions_ui.PNG)

![Continuous Delivery on Azure](./img/cd_on_azure.png)

# Overview

<TODO: complete this with an overview of your project>

## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project
* A link to a spreadsheet that includes the original and final project plan>

## Instructions

<TODO:  
* Architectural Diagram (Shows how key parts of the system work)>

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:



* Project running on Azure App Service

X. Clone the GitHub repository in your Azure Cloud
`git clone git@github.com:philbier/building-cicd-pipeline.git`
![Git repo cloned in Azure shell](./img/git_clone_az_shell.PNG)

* Passing tests that are displayed after running the `make all` command from the `Makefile`
X. Navigate into the cloned rep and ocally test the code
    a. Run `make setup` to set up virtual environment
    b. Run `source ~/.building-cicd-pipeline/bin/activate the command` to source into the virtual environment
    c. Run `make all` to install requirements as well as run linting and testing

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>



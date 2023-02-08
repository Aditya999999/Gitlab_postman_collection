# Gitlab_postman_collection
 This repository contains gitlab postman collection exported from POSTMAN after forking the collection from marketplace.
 Goal is to integrate this collection in Azure DevOps pipeline.

Step 1: Export collection from postman in json format.

Step 2: Push the collection in Github repository under any created folder in your repo.

Step 3: Create a project in Azure DevOps.

Step 4: Create a CI pipeline by taking suitable agent.

Step 5: Now add tasks that are following for running postman_collection:
	
	a. Install Newman - Newman is a command-line collection runner for Postman.
			    It allows you to effortlessly run and test a Postman collection directly from the command-line.
			    It is built with extensibility in mind so that you can easily integrate it with your continuous integration servers and build systems.
        
	b. Run API- Tests - Script for running tests {newman run Gitlab.postman_collection.json --reporters cli,json,junit --reporter-junit-export   	Results\junitReport.xml }
			  - Navigate to your folder which is containing collection under 'Working Directory'. 
	
	c. Publish Tests Results - Choose your test results format and the location where your resulted test files are under 'Tests Files Here'.


Link for pipeline- https://dev.azure.com/adityad13/Postman-API-Testing/_apps/hub/ms.vss-ciworkflow.build-ci-hub?_a=edit-build-definition&id=18

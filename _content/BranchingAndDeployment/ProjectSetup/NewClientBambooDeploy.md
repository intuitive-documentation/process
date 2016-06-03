---
title: "New Client - Bamboo Deploy"
status: TODO
---

NB - This will only cover Core and SQL deployments.  Web deployments are more custom depending on the type of web project.

## Pre-requisites
- *New Client - Bamboo Build* has been completed.
- The **Infrastructure Team** have completed the checklist before handing over the server environment before handing over to the development team.
- The Project Team has confirmed what applications the client needs to be set up.

## 1. Clone an existing SQL deployment project
- It is much easier to clone an existing project than set one up from scratch.
- Once created change the build plan to point to the SQL artefact build.
- Under release versioning set it to deploy release-1 next.
- Add this deployment Project to the dedicated list for the Agent.

## 2. Change the variables for the Test SQL Deployment
- Deployment.Host details should reflect Athena.
- Deployment.{variable}.1 should refelect the test server.

## 3. Edit the tasks for the Test SQL deployment
- The only thing to do here is ensure that the artefacts being downloaded are iVector.snp and IntuitiveSQL.sql.

## 4. Change the variables for the Live SQL Deployment
- Deployment.{variable}.1 should refelect the test server.
- Deployment.{variable}.2 should refelect the live server.

## 5. Edit the tasks for the Test SQL deployment
- The only thing to do here is ensure that the artefact being downloaded is IntuitiveSQL.sql.

## 6. Test the deployment
- Run the deployments to ensure they work
	- NB Test deployment needs to complete first

## 7. Clone an existing CORE deployment project
- Once created change the build plan to point to the Core artefact build.
- Under release versioning set it to deploy release-1 next.
- Add this deployment Project to the dedicated list for the Agent.

## 8. Change the variables for the Test and Live CORE deployment
- The only variable is the jira.project.key.

## 9. Edit the tasks for the Test and Live CORE deployment
- Ensure each artefect that is going to be deployed is referenced in the first stage.
- For each task task where they are used change the Host, Username and Password to what has been supplied to the Infrastructure Team.
- Edit the file paths to reference the new client in the SCP and SSH tasks.
- There needs to be an SCP Task for each artefact.
- To confirm the destination of the applications - jump onto the server using the credentials that have been supplied by the indrastructure team.

## 10. Test the build deploymeny
- Keep an eye on the destination folders to ensure they deploy to the correct location
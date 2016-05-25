---
title: "New Client - Bamboo Build"
status: TODO
---

## Pre-requisites
- JIRA project for the customer has been set up.

## 1. Create Branches
- In Bamboo under the *Release Management* project run the *Create Release Branch* build.
- Overide the variables
	- jira.key
		- The JIRA project code
	- release.number
		- 1
	- source.branch
		- master
- Wait for this to complete.

## 2. Create Linked Repositories
- In Bamboo click on the cog in the top right and click on *Linked Repositories*
- We will need to add a linked repository for each of the below repositories which point at the newly created branch (the naming convention is {JIRAprojectkey}.{StashProject}.{StashRepository}).
	- Core / CLR Deployment Task
	- Core / Intuitive
	- Core / Intuitive.Domain
	- Database / iVectorDB
	- Intuitive / Core
	- Intuitive / DLL Repository
	- Intuitive / Flight Provider Base
	- Intuitive / Interfaces
	- Intuitive / Outer Core
	- Intuitive / Web

## 3. Create Shell Project
- In Bamboo click on *Create* at the top then *Create New Plan*.
- Under Project select *New Project*.
- The Project Name should be the customer name.
- Keep a note of the Project Key that is generated.
- Insert dummy data for the Plan (We will be deleting this later).
- Select *Configure Plan*.
- Ensure that the plan is not enabled then click *Create*.

## 4. Copy over Plans
- Under the *Release Management* project kick off the *Copy plans to* build.
- You will need to input the variable of the Project Key from the the previous step.
- Wait for this to complete.
- Delete the dummy plan.

## 5. Amend plans
- For each plan the following needs to be changed.
	- Name
	- Repositories 
		- Link these to the *Linked Repositories* created earlier
	- Variables

## 6. Test Build
- Build each of the projects to verify that the builds succeed.
- These need to be built in dependency order.
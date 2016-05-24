---
title: "New Client - Bamboo Build"
status: TODO
---

## Pre-requisites
- JIRA project for the customer has been set up

## 1. Create Branches
- In Bamboo under the Release Management project run the "Create Release Branch" build.  
- Overide the variables
	- jira.key
		- The JIRA project code
	- release.number
		- 1
	- source.branch
		- master
- Wait for this to complete

## 2. Create Linked Repositories
- In Bamboo click on the cog in the top right and click on linked repositories
- We will need to add a linked repository for each of the below repositories which point at the newly created branch (the naming convention is {JIRAprojectkey}.{StashProject}.{StashRepository})
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
- In Bamboo click on "Create" at the top then "Create New Plan"
- 

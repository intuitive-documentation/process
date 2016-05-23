---
title: "Specification Writing"
status: TODO
---

## Purpose
- To create a complete specification for the work desired. This should:
	- Outline the chosen soultion
	- Define the criteria for success
	- Define the technical approach for the development

## Roles
- **Project Manager**
	- The project manager for the specific client
- **Technical Lead**
	- The technical owner of the part of the system which is to be changed (if the development is wide ranging multiple technical leads may be required)
- **QA Tester**
	- A member of the QA team (ideally someone who is familiar with the area of the system being changed)
- **Customer**
	- The stakeholder at the client's business for the required changes

## Entry Criteria
- A completed requirements document as per the [Requirements Gathering Process][1]
- All parties to have clear understanding of requirements and motivations for the proposed development as per the [Ballparking Process][2]

![Specification writing Process](/DevelopmentTeamProcess/images/SpecificationWriting/SpecificationWritingFlow.png)

## Tasks
T1a. 	Descriptive Specification: **Project Manager** to provide a descriptive overview of the problem and the agreed solution. This should contain visual aids where possible (eg screenshots/mockups and/or workflow diagrams).

T1b. 	Technical Solution: **Technical Lead** to provide a list of technical changes required to complete the development. This should allow any developer to pick up the development with very little outside input. Ideally this should be sufficiently detailed that any developer picking up the ticket could write almost the same code as any other developer, this should therefore contain class diagrams etc where appropriate.

T1c. 	BDD Specification: **QA Tester** to provide a comprehensive list of test cases (success criteria) in BDD format. This should also include a brief dexcription of the method by which the cases will be tested (where appropriate)

T2. 	Group Review: **Project Manager**, **Technical Lead** and **QA Tester** should meet to review the finalised specification. The sections should be collated into a single specification ([see template][3]) and all parties should check that none of the sections are contradictory and all meet the solution discussed.

T3. Quote: **Technical Lead** provides a final development effort for the ticket. **Project Manager** adds development days and billing details to the JIRA ticket, the ticket is then moved into *Quoted* status

T4. 	Sign Off: **Customer** reviews the finalised specification to ensure that all requirements are met to their satisfcation and that they understand what will be delivered. **Customer** also verifies that the defined criteria for success match with how they intent to ultimately test the development. **Customer** confirms they are happy with the quoted price of development. **Customer** moves the ticket into *Development Approved*

## Verification
N/A

## Exit Criteria
- All parties are satisfied that the specification document contains contradictions
- All parties are satisfied that the specification document contains no ambiguity
- All parties are satisfied that the specification document is not missing any success criteria
- **Technical Lead** is happy that any developer could pick up the job based on the information in the specification alone
- A development effort and billing details have been added to the JIRA ticket
- The status of the JIRA ticket is *Development Approved*

## Deliverables
D1. A finalised specification document which meets with the provided template

## Quality Records 
N/A

[1]:/DevelopmentTeamProcess/content/SoftwareDevelopment-subtopics/RequirementsGathering
[2]:/DevelopmentTeamProcess/content/SoftwareDevelopment-subtopics/Ballparking
[3]:https://drive.google.com/a/intuitivesystems.co.uk/previewtemplate?id=1Lo4hlFOcppqybZnfW6clsMPSR0dirWC9HdPhntb3jKw&mode=domain